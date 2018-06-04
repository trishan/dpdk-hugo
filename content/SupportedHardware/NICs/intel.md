+++
title = "Intel"
categories = ["NICs"]
hidden = true
type = "nic"
weight = "7"
+++

- [e1000](http://dpdk.org/doc/guides/nics/e1000em.html) (82540, 82545, 82546)
- [e1000e](http://dpdk.org/browse/dpdk/tree/drivers/net/e1000/) (82571, 82572, 82573, 82574, 82583, ICH8, ICH9, ICH10, PCH, PCH2, I217, I218, I219)
- [igb](http://dpdk.org/browse/dpdk/tree/drivers/net/e1000/) (82575, 82576, 82580, I210, I211, I350, I354, DH89xx)
- [ixgbe](http://dpdk.org/doc/guides/nics/ixgbe.html) (82598, 82599, X520, X540, X550)
- [i40e](http://dpdk.org/doc/guides/nics/i40e.html) (X710, XL710, X722)
- [fm10k](http://dpdk.org/doc/guides/nics/fm10k.html) (FM10420)

{{% notice note %}}
Note: The drivers e1000 and e1000e are also called em. The drivers em and igb are sometimes grouped in e1000 family.
{{% /notice %}}
