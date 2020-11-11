## truenas-telegraf

### Installation

You should install this inside a dataset so it won't get blown away by any
TrueNAS updates.

```
zfs create tank/telegraf
cd /mnt/tank/telegraf
git clone https://github.com/samuelkadolph/truenas-telegraf .
./install
```

### cputemp

```
[[inputs.exec]]
  commands = ["/mnt/tank/telegraf/cputemp"]
  data_format = "influx"
```
