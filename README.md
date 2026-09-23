# OCUDU snap

OCUDU is a free and open-source 5G software radio suite developed by the Linux
Foundation. It provides an integrated CU/DU gNodeB that can be used with USRP
software defined radios.

For application features, build instructions, and user guides, see the
[OCUDU documentation](https://docs.ocudu.org/).

## Usage

Install and connect the snap:

```bash
sudo snap install ocudu
sudo snap connect ocudu:kernel-module-observe
sudo snap connect ocudu:process-control
sudo snap connect ocudu:network-control
sudo snap connect ocudu:system-observe
sudo snap connect ocudu:raw-usb
```

To run the gNodeB, place a configuration file at
`/var/snap/ocudu/common/gnb.yml` and run:

```bash
sudo ocudu.gnb -c /var/snap/ocudu/common/gnb.yml
```

## Build

Build it with Snapcraft:

```bash
snapcraft
```
