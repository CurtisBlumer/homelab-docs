---
layout: page
title: Proxmox Setup
permalink: /proxmox-setup
categories:
  - proxmox
tags:
  - config
apt-proxy: http://apt-proxy.svcs.hjem.cloud:3128
---

# Proxmox Setup

## Installation

### Advanced LVM Options

When configuring harddisk options, select `ext4` as the file system and use the following advanced options.

- hdsize: 64
- swapsize: 8
- maxroot: _unset_
- maxvz: 0
- minfree: _unset_

The remaining space will be used later for an LVM-thinpool or Ceph.

## Configuration

Next we will add `{{ site.apt-proxy-url }}` to cache apt packages.