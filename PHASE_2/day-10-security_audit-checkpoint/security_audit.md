# Security Audit 

System Security Audit — Shiro (trippy)
Kernel: 5.15.167.4-micro · Date: 2026-08-19 · Uptime: 1h16m · Users: 1 (trippy, local console pts/1) · Load: 0.03

## Findings
1. Reboot Pattern (HIGH visibility)

- System reboots ~daily between 14:33–21:18; two reboots on Aug 13 within 2 hours. This frequency suggests crashes (kernel/OOM), hardware issues, or an automated reboot schedule — not malicious per se, but warrants review of kernel logs (journalctl -b -1, dmesg).

2. Audit Trail Degraded (MEDIUM)

- lastlog reports all accounts, including active user trippy and root, as "Never logged in." The lastlog database is not being maintained — login accounting is effectively broken, weakening forensic value.
No remote logins observed (FROM = -); activity is single-console-user.

3. Privileged Activity (MEDIUM–HIGH)

- Extensive sudo use; sudo -i, sudo -u root, and sudo -l confirm root-equivalent access is exercised routinely.
Password-adjacent commands: cat /etc/passwd, cat /etc/passwd-, passwd -S trippy, chage -l trippy — reading the password database and aging metadata.
strace -p 649 — tracing a live process; potential debugging or credential harvesting. PID 649 should be identified.
chmod g+s projects/shared_projects/ — setgid on a shared directory; verify ownership/permissions to avoid privilege/group-write risk.
chattr +i / chattr -i experiments on file and note.gpg — immutable-flag toggling; confirm intent.
Broad filesystem recon: find / -type p/s/b/c, find /var/log -mtime, du -sh /.

4. Firewall / Network (MEDIUM)

- UFW enabled; allowances: SSH, HTTP, HTTPS, and port 53 (DNS). An open 53/UDP rule is a classic DNS-tunneling/exfiltration vector — recommend removal unless DNS is explicitly hosted here.
Rule churn: rules 1–6 added then deleted (incl. a allow hhtps typo) — final config should be re-validated with ufw status numbered.

5. Software (LOW)

- Post-install tooling: net-tools, wireless-tools, traceroute, ndisc6, bind9-dnsutils, whois, strace, postgresql-client-16, plocate. postgresql-client-16 implies external DB connectivity — confirm legitimacy.

6. Failed Logins

- lastb was queried — check /var/log/btmp for brute-force attempts; output not captured here.

## Recommendations

- Investigate reboot cause (cron/systemd timers, crash logs).
- Restore login accounting; enable auditd and persistent sudo/command logging.
- Harden sudoers (require password, restrict command set); review /etc/sudoers/visudo output.
- Re-evaluate UFW rule 53; finalize and document the rule set.
- Audit shared_projects ownership/SGID; consider sticky bit and ACLs.
- Remove unneeded recon/client tools; inventory installed packages.
- Identify PID 649 and confirm the chattr targets were intentional.
- Review /var/log/btmp for failed-login activity.