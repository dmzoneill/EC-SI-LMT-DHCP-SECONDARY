# EC-SI-LMT-DHCP-SECONDARY

Scripts for the secondary DHCP server of an Intel lab management tool
(LMT). It is a smaller copy of
[EC-SI-LMT-DHCP-PRIMARY](https://github.com/dmzoneill/EC-SI-LMT-DHCP-PRIMARY)
that keeps a second DHCP server configured from the same IBM Rational
ClearQuest board data.

## What it does

- `dhcp.pl` generates the DHCP configuration from
  `templates/dhcpd.conf` and the board records in ClearQuest, keeping a
  backup of the last good file.
- `LMTCommon.pm` and `LMTEmailer.pm` provide the shared settings and
  email notifications, with HTML templates in `email`.
- `boards` lists the boards for each lab area, and `log` holds sample
  output.

## Tech

- Perl with ClearQuest's CQPerl and MIME::Lite
- ISC DHCP server

## Setup

The scripts expect to live in `/scripts` and read their settings from
`/scripts/config.ini`.

## License

Licensed under the Apache License 2.0. See [LICENSE](LICENSE).
