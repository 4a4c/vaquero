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

- check ipxe chainload `curl "192.168.4.10:8080/boot-ipxe"`
- check ipxe boot `curl "192.168.4.10:8080/ipxe?mac=00:0c:29:31:8f:14"`
- check cloud-config `curl "192.168.4.10:8080/cloud-config?mac=00:0c:29:31:8f:14"`

### Container used
`vaquero:v0.6.6`
