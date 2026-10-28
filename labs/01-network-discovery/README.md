
# Lab 01: Network Discovery

## Objective
Identify local network settings and test basic connectivity.

## Environment
- Operating system: Windows
- Tools: Command Prompt
- Network adapter: INTEL(R) Wireless-AC 9560
- Lab date: 10/28/2026

## Procedure
1. Inspect the active network adapter.
2. Record the IPv4 address and subnet mask.
    IPv4: 192.168.12.141
    Subnet Mask: 255.255.255.0
3. Identify the default gateway and DNS configuration.
    Default Gateway: 192.168.12.1
    DNS Configuration: 192.168.12.1
4. Test loopback connectivity; used 127.0.0.1
5. Test the default gateway.
6. Test an external IP address: 1.1.1.1

## Results
| Test             | Result | Interpretation                      |
|---               |---     |---                                  |
| Loopback ping    |PASSED  |Local IP stack responded             |
| Gateway ping     |PASSED  |Local gateway reachable              |
| External IP ping |PASSED  |External ICMP connectivity confirmed |

## Analysis
    1. The loopback test assesses my own computer's networking stack without sending traffic out to my router or onto my physical network. It proves that my computer can respond to basic local ICMP requests. This test does not prove that my Wi-Fi/Ethernet adapter, router or internet connection works as 127.0.0.1 lets my computer communicate with itself without needing to send the packets through my Wi-Fi or Ethernet adapter.
    2. The local gateway test assesses if the gateway is reachable and my local network connection is working. 
    3. The external IP test assesses if my connection can reach a specific external destination and return responses. Higher latency (response time) was observed to be consistent with traffic traveling beyond my local network.

## Limitations
    - Each ping test sent only four packets, providing a limited sample of network performance.
    - Successful ICMP responses do not guarantee that all network services, applications, or TCP/UDP ports are reachable.
    - The external IP test confirmed connectivity to `1.1.1.1`, but did not independently verify DNS resolution or access to other internet destinations.
    - Round-trip times can vary depending on network conditions, and the results represent only the conditions observed during this lab.

## Key Takeaways

    1. Loopback testing verifies local networking functionality. The address `127.0.0.1` allows a computer to test its own IP networking stack without relying on a physical network adapter, gateway, or internet connection.

    2. Testing the default gateway verifies local network reachability. A successful ping indicates that the gateway is reachable from my computer, providing evidence that local network communication is functioning.

    3. External connectivity tests verify communication beyond the local network. A successful ping to `1.1.1.1` confirms that my computer can exchange ICMP messages with an external destination. The higher round-trip time compared with the gateway is consistent with traffic traveling beyond the local network.
