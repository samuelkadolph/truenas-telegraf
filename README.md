## truenas-telegraf

### Installation

You should install this inside a dataset so it won't get blown away by any
TrueNAS updates.

```
zfs create tank/telegraf
cd tank/telegraf
git clone https://github.com/samuelkadolph/truenas-telegraf .
./install
```
