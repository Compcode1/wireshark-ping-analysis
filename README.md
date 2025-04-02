**Key Interpretations:**

Echo Request/Reply Structure:
ICMPv6 packets maintain the same conceptual structure as IPv4 ICMP. A Type 128 is an echo request, and a Type 129 is an echo reply. Sequence numbers and identifiers allow tracking of individual requests and replies.

IPv6 In Use:
The ping to www.google.com resolved to an IPv6 address, showing that Google services prioritize IPv6 connectivity. This provides an opportunity to explore the differences in how IPv6 routes traffic.

Hop Limit Analysis:
The outbound Echo Request had a Hop Limit of 128, typical for Windows systems. The reply returned with a Hop Limit of 54, indicating that it traversed approximately 74 network hops on the return path (128 – 54 = 74).
This confirms the remote nature of the destination and illustrates how Hop Limits (like IPv4 TTL values) can be used for path tracing, routing diagnostics, and even spoofing detection in cybersecurity.

Security Analysis Context:
Relevance in Cybersecurity Workflows:
While ICMP Echo Requests are simple and often overlooked, analyzing them is a core part of understanding:

Basic network reachability

Routing paths

Detection of misconfigured or spoofed hosts

Network mapping in reconnaissance

Anomalies like ICMP floods or scanning activity

Hop Limit (TTL) Use in Threat Hunting:

Abnormal or inconsistent hop counts are sometimes used to:

Detect Man-in-the-Middle attacks

Uncover IP spoofing

Identify unauthorized routing changes

**Conclusion:**

This project demonstrated how a basic ping test, when combined with Wireshark analysis, reveals rich layers of networking insight. By capturing and analyzing just eight packets, we were able to confirm IPv6 communication, verify host identity through MAC and IP data, and evaluate route distance using hop limit values
