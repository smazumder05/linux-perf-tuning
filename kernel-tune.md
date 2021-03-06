## Kernel sysctl configuration file for Red Hat Linux

#### For binary values, 0 is disabled, 1 is enabled.  See sysctl(8) and
#### sysctl.conf(5) for more details.

#### Controls source route verification
`net.ipv4.conf.default.rp_filter = 1`

#### Do not accept source routing
`net.ipv4.conf.default.accept_source_route = 0`

#### Controls the System Request debugging functionality of the kernel
`kernel.sysrq = 0`

#### Controls whether core dumps will append the PID to the core filename.
#### Useful for debugging multi-threaded applications.
`kernel.core_uses_pid = 1`

#### Disable netfilter on bridges.
```
#net.bridge.bridge-nf-call-ip6tables = 0
#net.bridge.bridge-nf-call-iptables = 0
#net.bridge.bridge-nf-call-arptables = 0

net.ipv4.ip_forward = 1

net.ipv4.neigh.default.gc_thresh1 = 4096
net.ipv4.neigh.default.gc_thresh2 = 8192
net.ipv4.neigh.default.gc_thresh3 = 16384
net.ipv4.neigh.default.gc_interval = 5

net.ipv4.neigh.default.base_reachable_time = 120
net.ipv4.neigh.default.gc_stale_time = 120
net.ipv4.neigh.default.base_reachable_time = 120
net.ipv4.neigh.default.gc_stale_time = 120

net.core.netdev_max_backlog = 262144
#net.core.rmem_default = 16777216
net.core.rmem_max = 108544
net.core.somaxconn = 262144
net.core.wmem_max = 108544

net.netfilter.nf_conntrack_max = 10000000
net.netfilter.nf_conntrack_tcp_timeout_established = 40

net.netfilter.nf_conntrack_tcp_timeout_close = 10
net.netfilter.nf_conntrack_tcp_timeout_close_wait = 10
net.netfilter.nf_conntrack_tcp_timeout_fin_wait = 10
net.netfilter.nf_conntrack_tcp_timeout_last_ack = 10
net.netfilter.nf_conntrack_tcp_timeout_syn_recv = 10
net.netfilter.nf_conntrack_tcp_timeout_syn_sent = 10
net.netfilter.nf_conntrack_tcp_timeout_time_wait = 10

net.ipv4.tcp_fin_timeout = 1
net.ipv4.tcp_max_orphans = 262144
net.ipv4.tcp_max_syn_backlog = 16384
net.ipv4.tcp_max_syn_backlog = 262144
net.ipv4.tcp_rmem = 4096 87380 16777216
net.ipv4.tcp_sack = 0
net.ipv4.tcp_syn_retries = 2
net.ipv4.tcp_synack_retries = 2
net.ipv4.tcp_syncookies = 0
net.ipv4.tcp_timestamps = 0
net.ipv4.tcp_tw_recycle = 1
net.ipv4.tcp_wmem = 4096 16384 16777216
```
