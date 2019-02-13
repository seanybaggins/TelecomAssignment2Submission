# TelecomAssignment2Submission - Internet and Transport Layer Packets and Routing

## See Xcel Chart to see captured data

## Answer the following questions

1. For packets that are coming from the same host, are the IP header’s packet ID numbers in order? Are they consecutive? Why or why not (speculate if you don’t know)?

The IP header packets coming from the host are in consecutive order. **Why Does this matter again?**

2. How many packets were in the entire stream? Where any packets retransmitted?

There were 43 packets in the entire stream. No packets needed to be retransmitted.

3. For the same site, use Traceroute (tracert) to map out the hops between here and there. Show the entire route (including sites that don’t report).

![FirstTracert](ImageAssets/FirstTracert.png)

![SecondTracert](ImageAssets/SecondTracert.png)

- How many hops are there?

As seen in the tracert figures in 3e there are 14 hops for a packet to travel from the client to the server or vice versa.

- How does this number compare with the ttl count in the message stream?

Since there is only 8 bits for the the time to live portion of the header and the number of hops plus time to live reported at the client is greater than 255 then I have reason to believe that the captured packets are not taking the exact same path notated in the tracert window or the ttl is not being decremented at some routers along the tracert path.

- Are there major Internet Exchange Points in the route? Which ones, where, and which networks are exchanging traffic?

Yes, there is a major Internet Exchange Point. Packets are passing from an Internet Exchange Point that goes from Phoenix to London. The internet exchange point was created by layer 3 communications. The company was later bought by century link. This information was obtained by doing an IP lookup using wolfram alpha and the results of the lookup can be seen in the following images.

![IPLookup1](ImageAssets/IPLookup1.png)

![IPLookup2](ImageAssets/IPLookup2.png)

- Compared to an airplane trip, how direct is the route (explain)?

The route is very indirect relative to an airplane trip. If I where to take an airplane trip to Ireland (the source destination of the requested packets) then I would probably only need two flights to transport myself to my end destination. Phoenix Sky Harbor to JFK followed by JFK to Dublin. As seen in the tracert capture in question 3 there are 14 hops (flights) until a packet is received by the server or client.

- Try the same Traceroute request, but on different days and different times of day. How do the two routes compare?

As seen in question 3 the paths of the packets are the same.