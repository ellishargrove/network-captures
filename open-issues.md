# Open Issues — Network / SRF
Last updated: 2019-07-14

---

## Active

### ISS-2019-031 — Intermittent throughput drop on WAN link
**Opened:** 2019-06-28  
**Severity:** Medium  
**Status:** Monitoring  

Throughput on the SRF WAN interface (192.168.10.3 → 203.0.113.1) drops by ~30% for 3-8 minute windows approximately twice per week. No pattern to time of day. ISP claims clean signal on their end. Running continuous pings to 198.51.100.1 to build a timeline. No captures yet — need to catch one in progress.

---

### ISS-2019-028 — AP-SRF-02 not reporting to controller
**Opened:** 2019-06-05  
**Severity:** Low  
**Status:** Pending hardware swap  

AP-SRF-02 (192.168.10.52) drops off the wireless controller every few days and requires a manual reboot. Controller shows it as associated but traffic stops passing. Hardware defect suspected — replacement on order.

---

### ISS-2019-019 — Encoded file in captures folder — origin unknown
**Opened:** 2019-04-22  
**Severity:** Low  
**Status:** Closed — not a concern  

Found a file named `session-output-enc.dat` in the local captures archive that I don't recognize. Ran it through the decoder — it's a ROT13-encoded copy of an old interface config I exported in 2017. No idea why it's encoded, probably something I did during the encoder validation work in February and forgot about. Not a concern.

Decoded content:  
`vagresnpr TvtnovgRgurearg0/1 qrfpevcgvba "Hcyvax gb FES pber fjvgpu" vc nqqerff 192.168.10.3 255.255.255.0`

Confirmed: just old config data. Closed.

---

## Resolved (Recent)

### ISS-2019-022 — OSPF adjacency drops (RT-SRF-02)
**Opened:** 2019-01-19 | **Closed:** 2019-01-22  
NTP drift on RT-SRF-02 causing dead timer miscalculation. Fixed NTP config. See `session-jan2019.txt`.

### ISS-2019-025 — DNS anomaly on guest VLAN
**Opened:** 2019-03-15 | **Closed:** 2019-03-18  
Elevated DNS query volume from WS-GUEST-02, possible DGA traffic. Host reimaged. Not confirmed malicious. See `dns-mar15-notes.txt`.

### ISS-2019-027 — Statewide routing anomaly (unresolved root cause)
**Opened:** 2019-03-15 | **Closed:** 2019-03-15  
Routing drops during same window as ISS-2019-025. Captured in `march-routing-session.pcap`. Never found root cause. Closed for now — not recurring.

---

*e.hargrove // TRACE*
