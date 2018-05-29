+++
title = "FAQ"
url = "/doc/guides/faq/"
weight = 18
+++

{{%expand "1. What does “EAL: map_all_hugepages(): open failed: Permission denied Cannot init memory” mean?" %}}
This is most likely due to the test application not being run with sudo to promote the user to a superuser. Alternatively, applications can also be run as regular user. For more information, please refer to [DPDK Getting Started Guide](https://www.google.com).
{{% /expand%}}

{{%expand "2. If I want to change the number of hugepages allocated, how do I remove the original pages allocated?" %}}
### CONTENT
{{% /expand%}}

{{%expand "3. If I execute “l2fwd -l 0-3 -m 64 -n 3 – -p 3”, I get the following output, indicating that there are no socket 0 hugepages to allocate the mbuf and ring structures to?" %}}
### CONTENT
{{% /expand%}}

{{%expand "4. I am running a 32-bit DPDK application on a NUMA system, and sometimes the application initializes fine but cannot allocate memory. Why is that happening?" %}}
### CONTENT
{{% /expand%}}

{{%expand "5. On application startup, there is a lot of EAL information printed. Is there any way to reduce this?" %}}
### CONTENT
{{% /expand%}}

{{%expand "6. How can I tune my network application to achieve lower latency?" %}}
### CONTENT
{{% /expand%}}

{{%expand "7. Without NUMA enabled, my network throughput is low, why?" %}}
### CONTENT
{{% /expand%}}

{{%expand "8. I am getting errors about not being able to open files. Why?" %}}
### CONTENT
{{% /expand%}}

{{%expand "9. VF driver for IXGBE devices cannot be initialized" %}}
### CONTENT
{{% /expand%}}

{{%expand "10. Is it safe to add an entry to the hash table while running?" %}}
### CONTENT
{{% /expand%}}

{{%expand "11. What is the purpose of setting iommu=pt?" %}}
### CONTENT
{{% /expand%}}

{{%expand "12. When trying to send packets from an application to itself, meaning smac==dmac, using Intel(R) 82599 VF packets are lost." %}}
### CONTENT
{{% /expand%}}

{{%expand "13. Can I split packet RX to use DPDK and have an application’s higher order functions continue using Linux pthread?" %}}
### CONTENT
{{% /expand%}}

{{%expand "14. Is it possible to exchange data between DPDK processes and regular userspace processes via some shared memory or IPC mechanism?" %}}
### CONTENT
{{% /expand%}}

{{%expand "15. Can the multiple queues in Intel(R) I350 be used with DPDK?" %}}
### CONTENT
{{% /expand%}}

{{%expand "16. How can hugepage-backed memory be shared among multiple processes?" %}}
### CONTENT
{{% /expand%}}

{{%expand "17. Why can’t my application receive packets on my system with UEFI Secure Boot enabled?" %}}
### CONTENT
{{% /expand%}}
