# PON_Sim

This project simulates the upstream transmission performance of a 50G-PON system using Fixed Dynamic Bandwidth Allocation (DBA). The simulation focuses on:

How buffer size impacts packet delay and packet loss rate

The effect of traffic load ranging from 5 Gbps to 50 Gbps

Fixed DBA: each ONU is allocated equal bandwidth in every DBA cycle (2 ms and 1 ms cycles considered)


├── scratch/
│   └── pon_fixed_dba.cc           # Main NS-3 simulation source code

Example Run for All Buffer Sizes (Bash loop)
bash
Copy
Edit
for buf in 10000 20000 30000 50000 100000 500000000 1000000000; do
    ./waf --run "pon_fixed_dba --bufferSize=$buf --cycleLength=2"
done
