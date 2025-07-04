#  VPN Technical Report  
`4th July 2025 | Proton VPN Free Tier Audit`  

## Connection Overview
**Test Server**: Netherlands  
**Client Config**:  
- Protocol: OpenVPN UDP  
- Encryption: AES-256-GCM  
- Kill Switch: Enabled  

## Performance Metrics
### Speed Degradation
![Speed Comparison](assets/speed_comparison.png)  
*Fig 1. Notable download speed reduction (-28.6%)*

### Latency Impact
| Condition   | Ping (ms) | Jitter |
|-------------|----------|--------|
| Direct      | 12       | 1.2    |
| VPN         | 47       | 4.8    |

## Security Analysis
### DNS Leak Test
![DNS Test Results](assets/dns_test.png)  
*Fig 2. Zero leaks detected - all requests routed through VPN*

### Encryption Verification
- HTTPS Padlock: ✅ Present on all test sites
- WebRTC Leak: ❌ Not detected

## Observed Limitations
1. **Speed**: Consistent ~30% throughput reduction
2. **Servers**: Only 3 free locations available
3. **Reliability**: Occasional connection drops during testing

## Work Log
- [x] 2025-07-04 09:30: Baseline speed tests
- [x] 2025-07-04 10:15: VPN connection established
- [x] 2025-07-04 11:00: DNS leak validation
- [x] 2025-07-04 11:45: Encryption verification
- [x] 2025-07-04 12:30: Data sanitization

## Conclusion
Proton VPN's free tier provides:  
✓ Adequate security for casual use  
✗ Unreliable performance for bandwidth-sensitive tasks  
