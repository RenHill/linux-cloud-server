# Manage a Cloud Server with Linux

**Author:** shanmhill@gmail.com  

---

## Project Overview: Simulating a Cloud Engineer's First Day

### What this project builds

In this project, I'm building a project directory structure mimicking a real server environment to practice investigating logs, fixing permissions, and managing services. This simulates being a cloud engineer who just got access to a Linux server that needs attention.

## Setting Up the Server Environment

### Verifying WSL 2 and systemd

In this step, I'm verifying that my WSL 2 instance is running and systemd is enabled so that I can investigate logs and write scripts.

![Image](https://learn.nextwork.org/soothed_turquoise_calm_dewberry/uploads/482db1d3-598e-4599-8256-34aca2dbea28_q80dxqlc)

## Investigating Application Logs

### Log analysis with grep, awk, and pipes

In this step, I'm investigating application logs so that I can use grep, awk, sort, uniq, and pipes to find errors.

![Image](https://learn.nextwork.org/soothed_turquoise_calm_dewberry/uploads/482db1d3-598e-4599-8256-34aca2dbea28_p02unkym)

### Identifying the top error source

The service with the most errors was auth with a count of 3.

## Mastering File Permissions

### chmod and chown in practice

In this step, I'm setting up file permissions so that I can control who can read, write, and execute files.

![Image](https://learn.nextwork.org/soothed_turquoise_calm_dewberry/uploads/482db1d3-598e-4599-8256-34aca2dbea28_1xan5qz0)

### Why 600 matters for secrets

The permission 600 means the owner can read and write and that group and others have no permissions. It's used for secrets because SSH will refuse to use a private key if others can read it.

## Managing Processes and Services

### systemctl, ps, and kill

In this step, I'm learning to use ps, df, free, and top so that I can check processes, memory, and disk usage.

![Image](https://learn.nextwork.org/soothed_turquoise_calm_dewberry/uploads/482db1d3-598e-4599-8256-34aca2dbea28_bgedoh8c)

### Diagnosing a slow server

I would run df -h to check if the disk is full and free -m to check if the memory is exhausted.

## Running the Health Check Script

### Building the automation tool

In this step, I'm setting up a bash script so that I can automatically check the system's health and log a report.

![Image](https://learn.nextwork.org/soothed_turquoise_calm_dewberry/uploads/482db1d3-598e-4599-8256-34aca2dbea28_ezfxpto0)

### Production-grade error handling

I learned that set -euo pipefail makes the script exit immediately if any command fails, if an undefined variable is used, or if a pipe fails. This matters because this is production best practice for error handling.

## Extending the Script: Multi-Service Monitoring and Warning Aggregation

![Image](https://learn.nextwork.org/soothed_turquoise_calm_dewberry/uploads/482db1d3-598e-4599-8256-34aca2dbea28_muhw1osk)

### Testing failure detection

In this project extension, when I stopped cron the output showed [FAIL] cron is NOT running.

## Reflections and Key Takeaways

### Tools and concepts

I built an automated server health-check script while practicing the Linux fundamentals that cloud engineers use.

Investigated application logs using grep, awk, sort, uniq, and pipes to extract error patterns and generate filtered reports.

Managed file permissions with chmod and chown, and controlled processes and services with ps, kill, and systemctl.

Wrote a production-style Bash script with variables, conditionals, loops, redirection, and tee for automated server health monitoring.

Extended my health-check script with journalctl, multi-service monitoring, and warning aggregation.

---

*Built with [NextWork](https://learn.nextwork.org) - [View this project](https://learn.nextwork.org/projects/482db1d3-598e-4599-8256-34aca2dbea28)*
