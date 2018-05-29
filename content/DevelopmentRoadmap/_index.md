+++
title = "Development Roadmap"
hidden = true
+++

{{% notice info %}}
Major known features and milestones may be noted here. This list is obviously neither complete nor guaranteed.
{{% /notice %}}

## Version 18.05 (2018 May)
- memory subsystem rework
- uevent support for hotplug
- new device specification (devargs) syntax
- secondary process support in virtual devices
- ethdev API for recommended descriptor ring sizes
- ethdev API to manage tunnel endpoints
- ethdev Rx/Tx offloads for various tunnels
- ethdev switch offloads
- ethdev port representor
- i40e PPPoE/PPPoL2Tv2
- mlx5 striding RQ (multi packets buffer)
- mlx5 tunnels offloads extended
- vhost interrupt mode
- selective datapath in vhost-user library
- new Intel driver (IFC VF) for accelerated virtio
- virtio-user for virtio-crypto
- tap TSO
- bonding support of flow API
- new API for hardware and software compression/decompression
- eventdev ordered and atomic queues for DPAA2
- eventdev crypto adapter
- eventdev timer adapter
- IP pipeline enhancements
- libedit integration

### Nice to have - Future
- multi-process rework
- automatic UIO/VFIO binding
- infiniband driver class (ibdev)
- BPF support
- default configuration from files
- generic white/blacklisting

#### Cycle model
A typical release should be done after 3 months.

It is designed to allow DPDK to keep evolving at a rapid pace while giving enough opportunity to review, discuss and improve the contributions.

The merge window will open once the previous release is complete. First version of a new feature must be submitted before the proposal deadline. Features that miss this first period will be deferred until the next release.

Updated versions of patches (v2, v3, etc.) will be submitted to address comments. The new features must be properly reviewed, tested and accepted before the integration deadline. Otherwise, they will be postponed to the next releases.

At the end of the merge window, the first release candidate is out.

The last period is 1 month long and is dedicated to bug fixing.

#### Scheduling

###### 18.05

- Proposal deadline: March 9, 2018
- Integration deadline: April 6, 2018
- Release: May 23, 2018

###### 18.08

- Proposal deadline: June 8, 2018
- Integration deadline: June 29, 2018
- Release: August 1, 2018

###### 18.11 (LTS)

- Proposal deadline: September 7, 2018
- Integration deadline: October 5, 2018
- Release: November 2, 2018

### Stable Releases

There is a documentation page describing the [guidelines of the stable releases](http://www.dpdk.org/doc/guides/contributing/stable.html).

Stable point releases follow mainline releases.

After each -rc tag and after the final version, relevant bug fixes get backported by the stable maintainers into the respective branches in "bursts".

Developers can provide stable-specific patches by sending them to stable@dpdk.org only (avoiding dev@dpdk.org).

After all the relevant bugfixes have been backported, regression tests are ran, and if clear, the stable release is announced.

Typically a new stable release version follows a mainline release by 1-2 weeks, depending on the test results.

| Next version  | Date | End of life | Maintainer |
|---|---|---|---|
| 16.11.7	 | June 8, 2018 | November 2018 (LTS) | Luca Boccassi |
| 17.11.3	 | June 8, 2018 | November 2019 (LTS) | Yuanhan Liu |
| 18.02.2	 | June 8, 2018 | June 2018 | Luca Boccassi |
| 18.05.1	 | August 24, 2018 | August 2018 | Christian Ehrhardt |
| 18.08.1	 | November 16, 2018 | November 2018 | Looking for volunteer |
| 18.11.1	 | January 11, 2019 | November 2020 (LTS) | Kevin Traynor |
