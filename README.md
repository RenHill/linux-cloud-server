[README(1).md](https://github.com/user-attachments/files/28301360/README.1.md)
<img src="https://cdn.prod.website-files.com/677c400686e724409a5a7409/6790ad949cf622dc8dcd9fe4_nextwork-logo-leather.svg" alt="NextWork" width="300" />

# Manage a Cloud Server with Linux

**Project Link:** [View Project](https://learn.nextwork.org/projects/482db1d3-598e-4599-8256-34aca2dbea28)

**Author:** shanmhill@gmail.com  
**Email:** shanmhill@gmail.com

---

![Image](https://learn.nextwork.org/soothed_turquoise_calm_dewberry/uploads/482db1d3-598e-4599-8256-34aca2dbea28_ezfxpto0)

## Project Overview: Simulating a Cloud Engineer's First Day

### What this project builds

In this project, I'm building a project directory structure mimicking a real server environment to practice investigating logs, fixing permissions, and managing services. This simulates being a cloud engineer who just got access to a Linux server that needs attention.

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

## Setting Up the Server Environment

### Verifying WSL 2 and systemd

In this step, I'm verifying that my WSL 2 instance is running and systemd is enabled so that I can investigate logs and write scripts.

![Image](https://learn.nextwork.org/soothed_turquoise_calm_dewberry/uploads/482db1d3-598e-4599-8256-34aca2dbea28_q80dxqlc)

## Reflections and Key Takeaways

### Tools and concepts mastered

The key tools I used include WSL. Key concepts I learnt include bash cloud administration and scripting.

### Time and challenges

This project took me approximately an hour. The most challenging part was learning how to navigate nano.

### What's next

I did this project today to learn how to use Linux in a cloud production environment.

---

*Built with [NextWork](https://learn.nextwork.org) - [View this project](https://learn.nextwork.org/projects/482db1d3-598e-4599-8256-34aca2dbea28)*
