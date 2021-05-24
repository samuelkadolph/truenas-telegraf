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

### Tested With

Confirmed to work with:

* FreeNAS-11.3-U4.1
* TrueNAS-12.0-RELEASE
* TrueNAS-12.0-U1.1
* TrueNAS-12.0-U3

### cputemp

I've included a small script that will correctly report CPU temperatures. Add this to your config.

```
[[inputs.exec]]
  commands = ["/mnt/tank/telegraf/cputemp"]
  data_format = "influx"
```
