---
layout: page
title: Proxmox Setup
permalink: /proxmox-setup
categories:
  - proxmox
tags:
  - config
---

This page will describe how to get started with Proxmox.

These steps will need to be taken on each server.

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
