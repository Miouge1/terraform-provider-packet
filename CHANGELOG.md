## 1.4.0 (Unreleased)
## 1.3.2 (February 06, 2019)

IMPROVEMENTS:

- [#95](https://github.com/terraform-providers/terraform-provider-packet/pull/95) Hotfix - facility df2 was missing from API lib listing

## 1.3.1 (February 04, 2019)

IMPROVEMENTS:

- [#92](https://github.com/terraform-providers/terraform-provider-packet/pull/92) Hotfix of device network order, back to: 0. Public IPv4, 1. IPv6, 2. Private IPv4

## 1.3.0 (February 01, 2019)

FEATURES:

* [#88](https://github.com/terraform-providers/terraform-provider-packet/pull/88) Support for BGP resources
* [#87](https://github.com/terraform-providers/terraform-provider-packet/pull/87) Upgrade to Go 1.11
* [#85](https://github.com/terraform-providers/terraform-provider-packet/pull/85) resource/packet_vlan: New resource for VLANs

IMPROVEMENTS:

* [#89](https://github.com/terraform-providers/terraform-provider-packet/pull/89) Impose explicit order on network configurations in device resource

## 1.2.5 (September 28, 2018)

FEATURES:

* [#72](https://github.com/terraform-providers/terraform-provider-packet/pull/72) resource/packet_spot_market_request: New resource for Spot Market Request for devices.
* [#71](https://github.com/terraform-providers/terraform-provider-packet/pull/71) datasource/packet_spot_market_price: New datasource for lookup of current hourly spot market price of devices based on location and plan
* [#70](https://github.com/terraform-providers/terraform-provider-packet/pull/70) datasource/packet_operating_system: New datasource for OS lookup

IMPROVEMENTS:

- [#73](https://github.com/terraform-providers/terraform-provider-packet/pull/73) - devices, projects and volumes are now importable (see `terraform import` doc)
- [#69](https://github.com/terraform-providers/terraform-provider-packet/pull/69) - in Device docs, explain how to get OS slugs

BUG FIXES:

- [#74](https://github.com/terraform-providers/terraform-provider-packet/issues/74) fix of broken links in device and ip_attachment docs


## 1.2.4 (May 31, 2018)

BUG FIXES:

- `r/packet_ip_attachment` - handling IP attachments being deleted outside of Terraform ([#68](https://github.com/terraform-providers/terraform-provider-packet/issues/68))

## 1.2.3 (April 27, 2018)

- [#61](https://github.com/terraform-providers/terraform-provider-packet/issues/61), fix volume resource update
- [#63](https://https://github.com/terraform-providers/terraform-provider-packet/pull/63), add Organization resource, add org attirbute to project resource

## 1.2.2 (April 17, 2018)

IMPROVEMENTS:

- [#58](https://github.com/terraform-providers/terraform-provider-packet/issues/58), properly fix resource updates

## 1.2.1 (April 16, 2018)

IMPROVEMENTS:

- [#57](https://github.com/terraform-providers/terraform-provider-packet/issues/57), fix for update of PXE attributes of device resource
- [#52](https://github.com/terraform-providers/terraform-provider-packet/issues/52) fix for project resource update
- [#49](https://github.com/terraform-providers/terraform-provider-packet/issues/49) fix for crash on SSH key update
- [#50](https://github.com/terraform-providers/terraform-provider-packet/issues/50) fix for device update, adds `description` attribute


## 1.2.0 (January 23, 2018)

BACKWARDS INCOMPATIBILITIES / NOTES:

* [#37](https://github.com/terraform-providers/terraform-provider-packet/issues/37), changes computation of packet_reserved_ip_block.cidr_notation. In case you use that attribute down the chain, you will need to refresh and recreate the resource in which you use it.

IMPROVEMENTS:

* datasource/packet_precreated_ip_block: Add Datasource for precreated IP blocks, so that users can assign subnets from those ([#36](https://github.com/terraform-providers/terraform-provider-packet/issues/36))
* mark device userdata as ForceNew, fixing ([#42](https://github.com/terraform-providers/terraform-provider-packet/issues/42))
* Add support for CPR (custom partitioning and RAID)([#35](https://github.com/terraform-providers/terraform-provider-packet/pull/35))

## 1.1.0 (October 09, 2017)

INTERNAL:

* Capture breaking change in the Packet API ((https://github.com/packethost/packngo/pull/47))

## 1.0.0 (September 28, 2017)

INTERNAL:

* provider: Add logging transport for HTTP client (`DEBUG` log now contains all HTTP requests & responses) ([#25](https://github.com/terraform-providers/terraform-provider-packet/issues/25))

IMPROVEMENTS:

* resource/packet_device: Add `public_ipv4_subnet_size` field ([#7](https://github.com/terraform-providers/terraform-provider-packet/issues/7))
* resource/packet_device: Add `hardware_reservation_id` field ([#14](https://github.com/terraform-providers/terraform-provider-packet/issues/14))
* resource/packet_device: Add `root_password` attribute ([#15](https://github.com/terraform-providers/terraform-provider-packet/issues/15))
* resource/packet_volume_attachment: Add resource for attaching volumes ([#9](https://github.com/terraform-providers/terraform-provider-packet/issues/9))
* resource/packet_reserved_ip_block: Add resource for reserving blocks of IP addresses ([#21](https://github.com/terraform-providers/terraform-provider-packet/issues/21))
* resource/packet_ip_attachment: Add resource for attaching floating IP addresses to devices ([#21](https://github.com/terraform-providers/terraform-provider-packet/issues/21))
* resource/packet_devce: Allow to use next-available hardware reservation ([#26](https://github.com/terraform-providers/terraform-provider-packet/issues/26))
* resource/packet_reserved_ip_block: Make reserved IP block resource importable ([#29](https://github.com/terraform-providers/terraform-provider-packet/issues/29))


## 0.1.0 (June 21, 2017)

NOTES:

* Same functionality as that of Terraform 0.9.8. Repacked as part of [Provider Splitout](https://www.hashicorp.com/blog/upcoming-provider-changes-in-terraform-0-10/)
