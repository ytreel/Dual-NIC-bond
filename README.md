Dual-NIC-bond
=============

the method bond the NIC eth0 eth2 to one virtual NIC bond0, and bond the NIC eth1 eth3 to virtual NIC bond1.
文档中将网卡eth0和eth2绑定为一个虚拟网卡bond0，将网卡eth2和eth3绑定为一个虚拟网卡bond1.

bond-mode表示工作模式，常用的工作模式有两种：
Mode 0(balance-rr)
Round-robin policy: Transmit packets in sequential order from the first available slave through the last. This mode provides load balancing and fault tolerance.
Mode 1(active-backup)
Active-backup policy: Only one slave in the bond is active. A different slave becomes active if, and only if, the active slave fails. The bond's MAC address is externally visible on only one port (network adapter) to avoid confusing the switch. This mode provides fault tolerance. The primary option affects the behavior of this mode.

bond-miimon表示系统每100ms监测一次链路连接状态

