+++
title = "Quick Start Guide"
+++

{{% alert theme="info" %}}A simple forwarding test with pcap PMD which works with any NIC (with performance penalties){{% /alert %}}

Extract sources
```
tar xf dpdk.tar.gz
cd dpdk
```

Enable pcap (libpcap headers are required).

```
make config T=x86_64-native-linuxapp-gcc
sed -ri 's,(PMD_PCAP=).*,\1y,' build/.config
```

Build libraries and test application (Linux headers may be needed with default config).

```
make
```

Reserve huge pages memory

```
mkdir -p /mnt/huge
mount -t hugetlbfs nodev /mnt/huge
echo 64 > /sys/devices/system/node/node0/hugepages/hugepages-2048kB/nr_hugepages
```

Run poll-mode driver test (with a cable between ports).

```
build/app/testpmd -c7 -n3 --vdev=net_pcap0,iface=eth0 --vdev=net_pcap1,iface=eth1 --
                  -i --nb-cores=2 --nb-ports=2 --total-num-mbufs=2048

testpmd> show port stats all

  ######################## NIC statistics for port 0  ########################
  RX-packets: 0          RX-errors: 0         RX-bytes: 0
  TX-packets: 0          TX-errors: 0         TX-bytes: 0
  ############################################################################

  ######################## NIC statistics for port 1  ########################
  RX-packets: 0          RX-errors: 0         RX-bytes: 0
  TX-packets: 0          TX-errors: 0         TX-bytes: 0
  ############################################################################

testpmd> start tx_first

testpmd> stop

  ---------------------- Forward statistics for port 0  ----------------------
  RX-packets: 2377688        RX-dropped: 0             RX-total: 2377688
  TX-packets: 2007009        TX-dropped: 0             TX-total: 2007009
  ----------------------------------------------------------------------------

  ---------------------- Forward statistics for port 1  ----------------------
  RX-packets: 2006977        RX-dropped: 0             RX-total: 2006977
  TX-packets: 2377720        TX-dropped: 0             TX-total: 2377720
  ----------------------------------------------------------------------------

  +++++++++++++++ Accumulated forward statistics for all ports+++++++++++++++
  RX-packets: 4384665        RX-dropped: 0             RX-total: 4384665
  TX-packets: 4384729        TX-dropped: 0             TX-total: 4384729
  ++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++
```

Some sample applications can be tested after building them.

```
make -C examples RTE_SDK=$(pwd) RTE_TARGET=build O=$(pwd)/build/examples
```
