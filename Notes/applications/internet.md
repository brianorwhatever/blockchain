## Mesh Networking
**Client**

Imagine you are downtown and you want to watch a YouTube video. Rather than your request hitting a Telus/Bell/Rogers cell tower which may be quite far away, it hits a few nearby cell phones and routers.

Those devices check whether they have the video, or whether they know a device that does. If one of them has the video they reply with a $/kb offer which your device may or may not accept depending on your chosen balance between cheapness and network speed. Or perhaps your request is sent with a threshold $/kb rate which if it can find it will automatically accept.

If your device accepts the cost then the transmission will begin and your device will pay the sender some small amount of wi-fi coin for each X kb chunk delivered.

If the price is too high then the request will continue to propagate outward, and perhaps some miniscule fee will be paid out to all these nodes just for listening to your request.

Eventually your request will hit a node which offers an acceptable price for the video and it will be returned to you. If the node holding the file is several hops away then each intermediary hop will get some piece of the fee.

**Server**

Every node in this network can act as both client and server. If you have enough free storage, that video you requested may sit on your phone for a while. Then if someone nearby requests the same video your phone will be able to serve it to them for some $/kb rate. It then earns back some of the cost that was incurred in obtaining the video in the first place. You might end up serving the video to a bunch of people and not only covering the cost of obtaining it, but also profiting.

**Market**

The most powerful aspect of a system like this is that the network becomes a market.

Suppose you have an apartment downtown in a high traffic area. You need a new router so you buy one that is set up to be a mesh node in this network market. All you do is enter your wi-fi coin wallet address and plug in the rouer.

Your router will now intelligently sell bandwidth at prices set to maximize your profit, while also ensuring that your traffic takes priority.

If some big event is going on downtown and thousands of people are demanding bandwidth then your router will charge as high a price as possible while still saturating it's available bandwidth.

However all nodes in the network will be doing the same thing, so free market competition will prevent gouging. The market will naturally find the correct price for that point in time.

When demand is low and nodes have plenty of unused bandwidth the cost per kb will approach the cost of electricity. As long as there is some profit to be made, even a tiny amount nodes will sell their bandwidth. If some nodes decide to stop selling then the bandwidth supply drops and therefore the price can increase slightly.

This being a market means that nodes will organically emerge to serve high traffic areas. Any area with poor Internet/wireless speeds but sufficient demand will attract nodes looking to profit. Thus the network naturally strengthens weak spots.

## Centralised Internet
**Cost**

The cost of a centralised Internet is very high for a few reasons.

The most obvious being the inefficiency in routing. Data necessarily takes much longer routes than it would in a decentralised network.

Centralisation also allows gatekeepers to price gouge and create monopolies. The most egregious example of this is cellular network data where 1GB can cost $20 while the actual network cost of that data is several orders of magnitude less.

**Scaling**

The current Internet is centralised. The entirety of requests for a given small website may be the responsibility of a few computers in a single location.

If demand suddenly spikes then the servers will likely fall over. So huge portions of the Internet are fragile and inflexible.

**Routing**

If I make a request for a YouTube video the data may come from many 100's of km's away. If someone right next to me requests the same video their data will likely also come from 100's of km's away. This is clearly inefficient.

This kind of problem is inherent to a centralised network.

**Availability**

The major websites rarely have downtime these days, though it can still happen. Everyone thought AWS was rock solid until some engineer typoed half the Internet into darkness in early 2017.

**Resiliency**

While most major websites have redundancy across many data centers in different regions and so on, this is stil not the case for large portions of the Internet.

## Decentralised Internet
**Cost**

The cost savings of routing efficiency would be tremendous. Due to the market nature of this network, traffic would be routed around choke points and traffic flow would become smooth and cost optimized.

The bandwidth cost in low-demand times and areas would approach the cost of electricity, which would probably be on the order of fractions of a cent per GB.

In high-demand times the price would increase but competition would keep prices fair. Since nodes can easily enter the network and 'mine' wi-fi coin, the costs would probably still be on the order of 1 cent per GB or so.

**Scaling**

Imagine some YouTube video is going viral and is just hitting a University. Instead of the Youtube servers getting hit with a request for every single view, the servers could fulfill one request which could then spread like a virus across the campus. The video could bounce from cell phone to laptop to router exponentially expanding to meet demand without slamming any single node.

**Routing**

Traffic could not only take the cheapest, most direct route to it's destination, but the massive redundancy of sending the same content repeatedly to a given area could be eliminated.

Network capacity might improve thousands of times without any infrastructure cost.

**Availability**

With nodes caching and sharing data, not relient on any particular node or path, uptime could approach 100%.

Routing would also be self-healing. If nodes along some path go down the network would discover new routes. If a portion of the network becomes physically disconnected from the rest of the network then nodes will rapidly appear to capitalize on this profit opportunity.

**Resiliency**

With the current Internet if a server hosting a file goes down then that file is no longer available. In a decentralised mesh network the only way a resource truly dissappears is if literally no node has a copy. For anything of value or interest this would likely never happen.

Such a network could also sustain huge node loss with minimal effect. Since most resources would be randomly distributed across the whole network, the network could sustain massive loss of nodes either randomly or in geographic location with minimal data loss. 
