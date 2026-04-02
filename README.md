# Vedant P. Dubal

**DevOps · SRE · System Administrator**

> Hey, I'm Vedant — first-year B.Tech student.
> I spend my time breaking Linux installations, fixing them, and calling it learning. ¯\_(ツ)_/¯

I work on the layer between code and the metal it runs on — infrastructure automation, container orchestration, system reliability, and occasionally training AI models at 2 AM while laptop fans scream at 8000 RPM.

Not a tutorial follower. I pick something, break it badly enough that I *have* to understand it to fix it, then write about what actually happened — not the clean version.

---

## What I Actually Work On

```
infrastructure automation  →  containers & orchestration  →  keep systems alive
```

```bash
$ whoami
devops-in-progress | sysadmin | homelab guy | occasionally breaks things on purpose

$ uptime
1st year B.Tech @ Rai University, Ahmedabad — since 2024
```

---

## Skills

#### Infrastructure & DevOps
![Linux](https://img.shields.io/badge/Linux-Arch%20%7C%20Ubuntu%20%7C%20Debian-1793D1?style=flat-square&logo=archlinux&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)
![Kubernetes](https://img.shields.io/badge/Kubernetes-326CE5?style=flat-square&logo=kubernetes&logoColor=white)
![GitHub Actions](https://img.shields.io/badge/GitHub_Actions-2088FF?style=flat-square&logo=github-actions&logoColor=white)
![Jenkins](https://img.shields.io/badge/Jenkins-D24939?style=flat-square&logo=jenkins&logoColor=white)
 <!--  ![Nginx](https://img.shields.io/badge/Nginx-009639?style=flat-square&logo=nginx&logoColor=white) -->

#### Monitoring & Networking
<!-- ![Grafana](https://img.shields.io/badge/Grafana-F46800?style=flat-square&logo=grafana&logoColor=white) -->
<!-- ![Prometheus](https://img.shields.io/badge/Prometheus-E6522C?style=flat-square&logo=prometheus&logoColor=white) -->
![SSH](https://img.shields.io/badge/SSH-333?style=flat-square&logo=gnubash&logoColor=white)
![DNS](https://img.shields.io/badge/DNS%20%7C%20VLANs-333?style=flat-square&logo=gnubash&logoColor=white)

#### Languages
![Bash](https://img.shields.io/badge/Bash-4EAA25?style=flat-square&logo=gnubash&logoColor=white)
![C++](https://img.shields.io/badge/C++-00599C?style=flat-square&logo=cplusplus&logoColor=white)

#### AI / ML Infra
![CUDA](https://img.shields.io/badge/CUDA-76B900?style=flat-square&logo=nvidia&logoColor=white)
![PyTorch](https://img.shields.io/badge/PyTorch-EE4C2C?style=flat-square&logo=pytorch&logoColor=white)
![FFmpeg](https://img.shields.io/badge/FFmpeg-007808?style=flat-square&logo=ffmpeg&logoColor=white)

#### Tools
![Git](https://img.shields.io/badge/Git-F05032?style=flat-square&logo=git&logoColor=white)
![GitHub](https://img.shields.io/badge/GitHub-181717?style=flat-square&logo=github&logoColor=white)
![Postman](https://img.shields.io/badge/Postman-FF6C37?style=flat-square&logo=postman&logoColor=white)
![Figma](https://img.shields.io/badge/Figma-F24E1E?style=flat-square&logo=figma&logoColor=white)

#### Familiar With *(know enough to be dangerous)*
![Node.js](https://img.shields.io/badge/Node.js-339933?style=flat-square&logo=nodedotjs&logoColor=white)
![React](https://img.shields.io/badge/React-61DAFB?style=flat-square&logo=react&logoColor=black)
![Express](https://img.shields.io/badge/Express-000000?style=flat-square&logo=express&logoColor=white)
![Ansible](https://img.shields.io/badge/Ansible-EE0000?style=flat-square&logo=ansible&logoColor=white)

<!-- Uncomment when confident:
![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![Terraform](https://img.shields.io/badge/Terraform-7B42BC?style=flat-square&logo=terraform&logoColor=white)
-->

---

## Projects

### [DockForge](https://github.com/vedantdubal-141/dockyard)
> Docker environment automation — clone, run one command, done. (•̀ᴗ•́)و

![DockForge demo](https://vedantdubal-141.github.io/0xvoid/images/dockforge.gif)

Tired of "works on my machine." Built an automated setup that provisions full application stacks from a single command. Auto-discovers apps and Dockerfiles, builds containers, handles cleanup, and validates everything on every push via GitHub Actions CI.

- Bash automation engine with zero-config auto-discovery
- GitHub Actions CI/CD pipeline — catches build errors before deployment
- Docker auto-installer, cleanup scripts, full lifecycle automation

---

### Arch Linux Homelab + Android Chroot
> Running Linux without a second computer. ¯\(°_o)/¯

![chroot vs proot](https://vedantdubal-141.github.io/0xvoid/images/root.png)

Manually installed Arch Linux from scratch — partition tables, kernel selection (linux-zen for the latency wins), bootloader config, and a TUI display manager because ASCII art login screens are a valid life choice.

When I needed a second machine to experiment on and didn't have one, I rooted an Android phone with Magisk and set up a full chroot environment inside Termux. Real kernel interfaces, bind-mounted `/proc /sys /dev`, near-native performance — no proot overhead.

Also self-hosted: Nextcloud, Nginx with SSL, VLANs, reverse proxy.

---

### RVC Voice Model Training
> 8 hours of continuous GPU training on Arch Linux. What could go wrong. (ಠ_ಠ)

![RVC training](https://vedantdubal-141.github.io/0xvoid/images/rvc.gif)

Everything. Everything went wrong first.

Fought through Python 3.12 + PEP 668 restrictions, NVIDIA PyPI timeouts pulling 500MB+ CUDA packages, torch compatibility hell, and a mid-training power cut that killed the session at epoch 20.

Logs were still intact. Resumed from checkpoint. Finished at 200 epochs, 14,000 steps, RTX 4070 running at 7.7GB/8GB VRAM the whole time.

---

## Real-world Sysadmin Work

**Windows boot failure recovery** — bootrec, sfc, chkdsk all failed. Booted live Linux USB, ran SMART checks with `smartctl`, used `rsync` instead of `cp` for interruptible backup, clean UEFI reinstall, `diskpart` to fix NTFS partition letter. Worked. `(⌐■_■)`

**Git/SSH debugging during a hackathon** — teammate couldn't push. DNS tweaks, proxy checks, HTTP/1.1 forcing — all dead ends. Switched remote from HTTPS to SSH, generated ed25519 keypair, back online in 5 minutes.

---

## Writing

I document what I actually do on LinkedIn — not polished tutorials, just what broke and what fixed it.

- Linux boot process (UEFI → initramfs → systemd)
- Manual Arch Linux install walkthrough
- Running Linux chroot on Android without a second machine
- RVC voice model training on Linux (parts 1 & 2)
- Windows boot failure diagnosis and full recovery
- Git/SSH debugging under hackathon pressure

---

## Currently Exploring

- Kubernetes cluster management at scale
- Infrastructure as Code (Terraform / Ansible)
- SRE practices and incident response
- Linux kernel internals — going deeper `(。・_・。)`

---

## Find Me

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=flat-square&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/vedant-p-dubal-2107733a4)
[![GitHub](https://img.shields.io/badge/GitHub-181717?style=flat-square&logo=github&logoColor=white)](https://github.com/vedantdubal-141)
[![YouTube](https://img.shields.io/badge/YouTube-FF0000?style=flat-square&logo=youtube&logoColor=white)](https://youtube.com/@vedantdubal)
[![Twitter](https://img.shields.io/badge/Twitter-1DA1F2?style=flat-square&logo=twitter&logoColor=white)](https://x.com/vedantdubal)

---

## Contribution Graph

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/vedantdubal-141/vedantdubal-141/output/github-snake-dark.svg" />
  <source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/vedantdubal-141/vedantdubal-141/output/github-snake.svg" />
  <img alt="github-snake" src="https://raw.githubusercontent.com/vedantdubal-141/vedantdubal-141/output/github-snake.svg" />
</picture>

---

<sub>last updated when I should have been sleeping (~˘▾˘)~</sub>
