# AeryxIQ On-Premises Edition

**The Drone PACS platform for aerial inspection.** Free to download, free to run, on your own hardware.

AeryxIQ is a Drone Picture Archiving and Communication System. Drop an SD card dump on an asset and it reads each frame's capture time and GPS position, splits the dump into flights, and files each flight as its own inspection study. Readers annotate and grade defects, sign the report, and next year's flight is read against this year's.

The On-Premises Edition is the full product. There is no account, no licence key and no call home. Imagery and flight data never leave the building.

An Amhage Technology Group LLC product.

## Download

Current release: **[1.0.0](https://github.com/Amhage-Technology-Group/aeryxiq-releases/releases/latest)**

| You have | Download |
|---|---|
| Windows 10 or 11 with Docker Desktop | [AeryxIQ-Setup.exe](https://github.com/Amhage-Technology-Group/aeryxiq-releases/releases/latest/download/AeryxIQ-Setup.exe) |
| Linux, macOS or a server with Docker | [aeryxiq-onprem-1.0.0.zip](https://github.com/Amhage-Technology-Group/aeryxiq-releases/releases/latest/download/aeryxiq-onprem-1.0.0.zip) |
| VMware, VirtualBox, Proxmox or Hyper-V | [AeryxIQ-Appliance-1.0.0.ova](https://github.com/Amhage-Technology-Group/aeryxiq-releases/releases/latest/download/AeryxIQ-Appliance-1.0.0.ova) |

Manuals: [Quick Start](https://github.com/Amhage-Technology-Group/aeryxiq-releases/releases/latest/download/AeryxIQ-Quick-Start-Guide-1.0.0.pdf) · [Installation Guide](https://github.com/Amhage-Technology-Group/aeryxiq-releases/releases/latest/download/AeryxIQ-Installation-Guide-1.0.0.pdf) · [Administrator Guide](https://github.com/Amhage-Technology-Group/aeryxiq-releases/releases/latest/download/AeryxIQ-Administrator-Guide-1.0.0.pdf)

Also mirrored on SourceForge.

## What is included

| Area | In the free edition |
|---|---|
| Asset registry | 62 asset types, from wind turbines and facades to bridges, fields and incident scenes, each with its own component vocabulary |
| Flight import | SD-card folders split into flights by EXIF capture time, every frame geolocated |
| Missions | 46 mission types, nine media kinds: photo, video, thermal, multispectral, orthomosaic, elevation model, point cloud, document |
| Reading room | Filmstrip, frame viewer, flight track on a map, drag-to-annotate findings |
| Grading | 72 finding categories, grades G1 Minor to G5 Critical, comparison against the prior study |
| Facade ordinances | SAFE, SWARMP and UNSAFE classification from recorded findings, on a five-year cycle |
| Reports | Drafted and finalised reports, branded PDF, public evidence verification link |
| Sharing | Single-study share links that expire, no account needed to view |
| Follow-through | Work orders, alerts, pilot credentials, capital planning export |
| Security | Argon2 passwords, account lockout, RFC 6238 two-factor sign-in, organisations isolated from each other, nothing contacts the internet |

There is no user, asset, study or storage limit.

## Requirements

Docker Desktop (Windows, macOS) or Docker Engine (Linux), 4 CPU cores, 8 GB memory, and disk for your imagery. Internet access is needed once, to download the container images; the Installation Guide covers fully offline installation.

## Install

Windows: run `AeryxIQ-Setup.exe`, then Start AeryxIQ from the Start Menu.

Linux or macOS:

```
unzip aeryxiq-onprem-1.0.0.zip
cd aeryxiq-1.0.0
./up.sh --with-demo
```

Open `https://aeryxiq.localhost`. The browser warns about the certificate on the first visit: the installation issues its own, so that it works in a building with no internet connection. `trust-certificate` removes the warning.

Appliance: import the OVA, give it 4 vCPU, 8 GB and a bridged network adapter, and boot. The console shows the address to open.

## Verify your download

Every asset is listed with its SHA-256 in `SHA256SUMS.txt` on the release.

```
# Windows
Get-FileHash .\AeryxIQ-Setup.exe -Algorithm SHA256
# Linux, macOS
sha256sum -c SHA256SUMS.txt --ignore-missing
```

The Windows installer is not code signed yet. SmartScreen will say it does not recognise the publisher: choose More info, then Run anyway, after checking the hash.

## Support and services

The software is free. Help with it is not, and the prices are public.

| | Price |
|---|---|
| On-Premises Edition | Free |
| Support Plan: business-hours support, upgrade guidance, configuration review | $199 per month |
| Professional Install: remote installation and first-day configuration | $499 one time |
| Archive Migration: we ingest your historical flights | from $1,500 one time |
| Hosted, Pilot: we run it for you | $1,490 per year |
| Hosted, Team: multi-user with roles | $4,990 per year |

[aeryxiq.com/services](https://aeryxiq.com/services/) · support@aeryxiq.com

## Licence

Two parts, two licences, both texts in every download:

| Part | Licence |
|---|---|
| Deployment files: Windows installer, Compose bundle, scripts, appliance configuration | [Apache License 2.0](https://www.apache.org/licenses/LICENSE-2.0) |
| The AeryxIQ application, downloaded as container images on first start | AeryxIQ On-Premises Licence: free to install and run for any purpose, commercial use included; not to be redistributed or resold |

Full terms: [TERMS.md](TERMS.md).

AeryxIQ holds no engineering, surveying or inspection certification. Its automated assistance is assistance. Every determination and signature stays with the qualified person who makes it.

## About

Amhage Technology Group LLC, Rochester, New York. AeryxIQ is a trademark of Amhage Technology Group LLC: see [TRADEMARKS.md](TRADEMARKS.md).
