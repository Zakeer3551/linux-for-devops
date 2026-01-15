# Linux Filesystem Structure

Understanding the Linux filesystem is critical for system administration, troubleshooting, containerization, and DevOps workflows. Linux follows a **hierarchical directory structure**, where each directory has a well-defined purpose.

---

## High-Level View

Linux uses a **single-root filesystem**, starting at `/`, unlike Windows which uses drive letters (C:, D:).

All files, directories, devices, and processes are represented within this hierarchy.

---

## Symbolic Links (Less Significant for Daily Use)

In modern Linux systems, some directories are symbolic links pointing to `/usr`.

| Directory | Linked To | Description |
|---------|----------|-------------|
| `/bin`  | `/usr/bin` | Essential user command binaries |
| `/sbin` | `/usr/sbin` | System and administrative binaries |
| `/lib`  | `/usr/lib` | Shared libraries and kernel modules |

> These links exist mainly for backward compatibility.

---

## Important System Directories

| Directory | Description |
|---------|-------------|
| `/boot` | Files required to boot the system (not relevant in containers) |
| `/usr`  | User-installed applications, binaries, and libraries |
| `/var`  | Variable data such as logs, caches, and spool files |
| `/etc`  | System-wide configuration files |

---

## User & Application-Specific Directories

| Directory | Description |
|---------|-------------|
| `/home` | Default location for user home directories |
| `/root` | Home directory for the root user |
| `/opt`  | Optional or third-party application installations |
| `/srv`  | Data served by system services (rare in containers) |

---

## Temporary & Virtual Filesystems

| Directory | Description |
|---------|-------------|
| `/tmp`  | Temporary files (usually cleared on reboot) |
| `/run`  | Runtime data for active processes |
| `/proc` | Virtual filesystem exposing process & kernel info |
| `/sys`  | Kernel and hardware information |
| `/dev`  | Device files (e.g., disks, null devices) |

> `/proc`, `/sys`, and `/dev` are **virtual filesystems**, not real files on disk.

---

## Mount Points

| Directory | Description |
|---------|-------------|
| `/mnt`  | Temporary mount point for filesystems |
| `/media` | Mount point for removable media (USB, CD-ROM) |
| `/data` | User-defined mount (e.g., Docker bind mount from host) |

In container-based setups, `/data` is commonly used for **persistent storage** mapped from the host system.

---

## Why This Matters for DevOps

- Knowing **where configs live** (`/etc`)
- Understanding **logs and state** (`/var`)
- Working with **containers and mounts** (`/data`, `/mnt`)
- Debugging system behavior via `/proc` and `/sys`

Mastering the Linux filesystem is foundational for automation, troubleshooting, and production reliability.
