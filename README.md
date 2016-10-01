# vaquero

[vaquero docs](https://ciscocloud.github.io/vaquero-docs)

[vaquro repo](https://github.com/ciscocloud/vaquero)

## integration notes
### vaquero host
`192.168.4.10/24`

`sa-config.yaml` goes in `/var/lib/vaquero/`

`vaquero.service` goes in `/etc/systemd/system/`

enable unit via `systemctl enable vaquero`

commands to make sure vaquero is serving files

- check ipxe chainload `curl "10.54.213.134:8080/boot-ipxe"`
- check ipxe boot `curl "10.54.213.134:8080/ipxe?mac=00:25:b5:36:0a:ef"`
- check cloud-config `curl "10.54.213.134:8080/cloud-config?mac=00:25:b5:36:0a:ef"`

### Container used
`vaquero:v0.6.6`
