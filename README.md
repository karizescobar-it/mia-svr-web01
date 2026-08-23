# Home Server for Information Technology Experimentation

## Overview
This homelab is a home server used to practice sysadmin and IT Help Desk activities. It runs 2 Docker containers and 2 instances of Simple Web Server. Each container and instance is set to be connected to remotely through Tailscale's VPN client. 

## Purpose
- Practice Junior Sysadmin tasks; server administration, basic monitoring and log review, networking, database operations
- Practice tasks of IT Help Desk tiers 1 and 2; remote desktop, simple networking concepts, software error troubleshooting
- Practice with command line interfaces; WSL, Powershell, CMD, SSH

## General Information

* Network Access
Local IP Address: 10.0.0.195
Tailscale IP Address: 100.71.101.11
Hostname (Local and Tailscale): mia-svr-web01/

* Docker Container Ports
Jellyfin (media server) — port 8096
Zammad Ticketing System — port 8080
* Simple Web Server Ports
Hello World! — port 591
KJV Bible — port 80

## Troubleshooting Checklist
If a service is unreachable
* Docker
1. docker ps — is the container running?
2. docker logs <container> or docker-compose logs <service> — look for errors
3. docker inspect <container> — check port bindings & network mode
4. Check volume mounts for permission errors
* Simple Web Server
1. Check with GUI if Server is toggled on with yellow switch
2. Check if port matches the correct setting (e.g. port 80 with HTTPS disabled, port 443 with HTTPS enabled)

## Security
Tailscale encrypts every connection to this server.



