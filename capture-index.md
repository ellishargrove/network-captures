# network-captures

Session captures from sites and incidents. Some resolved, some not.

Captures are named by site and date where possible. Anything marked `[local]` was not uploaded — file size or sensitivity. Notes files are in the same directory as the capture when they exist.

---

## Index

| Filename | Site | Date | Size | Notes | Status |
|---|---|---|---|---|---|
| `lacue-site-survey-2018.pcap` | TRACE HQ | 2018-11-04 | 41.2 KB | Pre-deployment survey, nothing unusual | `[local]` |
| `dhcp-storm-dec2018.pcap` | TRACE HQ | 2018-12-17 | 112.4 KB | DHCP storm from rogue device on VLAN 20, resolved | `[local]` |
| `routing-anomaly-jan2019.pcap` | TRACE HQ | 2019-01-22 | 28.8 KB | Intermittent OSPF adjacency drops, see `session-jan2019.txt` | `[local]` |
| `march-routing-session.pcap` | TRACE HQ | 2019-03-15 | 33.4 KB | Statewide routing anomaly, never found root cause | **uploaded** |
| `wireless-survey-apr2019.pcap` | Client site | 2019-04-03 | 19.1 KB | Channel interference survey, AP placement rec delivered | `[local]` |
| `dns-poisoning-suspect-jun2019.pcap` | TRACE HQ | 2019-06-11 | 47.6 KB | Flagged by IDS, false positive confirmed after review | `[local]` |

---

## Notes

Most of these stay local. The march session is up because I need to reference it elsewhere and the file is clean — no credentials, no PII, all RFC ranges.

The june capture has the IDS alert context in it and I don't want that sitting on a public repo even redacted.

---

*ellishargrove // last updated 2019-07-02*
