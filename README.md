# xmpp-example
An attempt to learn the xmpp protocol

## Resources
[Specifications](https://tools.ietf.org/html/rfc3920)
[Main Site](https://xmpp.org/about/technology-overview.html)

## Notes
### What is XMPP?
- Stands for Extensible Messaging and Presence Protocol
- For streaming XML over a network
- Commonly used for IM, multi-part chat, calls
- Similar to Email
- Can be isolated from the public internet

### XML?
- Stands for Extensivle Markup Language
- Used to Markup or describe data
- DTD (Document Type Definition) tells the receiving side to understand the format it is in.
- Like HTML except you create your own building blocks

### Why not JSON?
- XML allows more complexity
- XML allows same namespace usage in the same level, which makes it tolerate extensibility

### XMPP Architecture
- generally uses client-server architecture over a TCP connection
- Servers manage connections/sessions and their XML streams
- Servers route XML stanzas over the XML streams
- Client connections typically connect at port 5222
- Gateways translate XMPP to other protocols
- Network connections are generally on port 5269

### Addressing
- entities are any network endpoint
- all entities are uniquely addressable by a Jabber Identifier (JID)
- JID syntax is defined using the Augmented Backus-Naur Form ("<user@host/resource>")
- domain/host is the primary identifier, and the only one that is required, representing the network gateway
- domain identifiers must be internationalized
- node identifier generally represents the entity making requests

### XML streaming
XML streaming involves two main concepts:

#### XML streams
- starts with an opening xml `<stream>` tag and ended by `</stream>`
- entity initiating it sends XML stanzas

#### XML stanzas 
- discrete semantic unit sent over XML stream
- direct child of `<stream/>`
- start of any stanza is denoted by the start of an element start tag at depth=1 of the XML stream
- stanzas may contain child elements
- default namespace involves `<message/>`, `<presence/>` and `<iq/>` elements






