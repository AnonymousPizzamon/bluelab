| Boot Profile         |                             VM |  vCPU |                                                  RAM |
| -------------------- | -----------------------------: | ----: | ---------------------------------------------------: |
| A (default)          |                        pfSense |     1 |                                                0.5 G |
|                      |  Windows Server 2022 Core (DC) |     2 |                                                  2 G |
|                      | Windows 11 Enterprise (Client) |     2 |                                                  3 G |
|                      |     Ubuntu SIEM (Elastic+Zeek) |     2 |                                                5.5 G |
|                      |                   **Subtotal** | **7** |                                             **11 G** |
| B (two-client tests) |                   +Windows 11b |    +2 |                                                 +3 G |
|                      |                     **Action** |       | Stop Kibana (`docker stop kibana`) & keep ES JVM 3 G |
|                      |                       **Peak** | **9** |           **≈14 G** (Kibana off; still ≤13 G active) |
