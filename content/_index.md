+++
title = "Lightning Klump"
outputs = ["Reveal"]
+++

### The Lingering Promise of the Semantic Web as a Modern Application Platform

Drake Talley

<small><i class="fab fa-github"></i>axylos</small><br />
<small><i class="fab fa-twitter"></i> axylos</small>

---
### Who am I?

---

### What is the Semantic Web?

{{% fragment %}}
A set of technologies intended to make internet data "machine-readable"
{{% /fragment %}}

{{% fragment %}}
- A schema design language + serialization formats (RDF and friends)
- A query language with built-in logical inference capabilities (SPARQL)
- Set a of protocols to coordinate server-server interactions (Linked Data Protocol)
{{% /fragment %}}

---

### Unrealized Potential

{{% fragment %}}
- Required high up-front design cost
- Full benefit only available in niche domains or alongside mass deployments
- Too little bang for the buck for early adopters
{{% /fragment %}}

---

### Centralization

---

### SaaS

{{% fragment %}}
- There are many scenarios that require easy discovery from a large dataset or community followed by close interactions among a relatively very small cluster of actors.
{{% /fragment %}}

---

{{% fragment %}}
SaaS businesses meet this need by enforcing a consistent data domain for all participants and centrally hosting that data alongside application servers
{{% /fragment %}}

{{% fragment %}}
The rise of cloud computing lowered the cost of building new and focused services for addressing particular problems.
{{% /fragment %}}

---

### Where to go from here?

- Federated Services?
- Blockchain?

---
Contemporary Social Protocols
  - Solid
  - Trellis LDP
  - Activity Streams
  
---

### What are we trying to solve?

{{% fragment %}}
A primary though underemphasized challenge is to expand access to highly available compute and network resources
{{% /fragment %}}

{{% fragment %}}
We can correct the power imbalance between "client" users and server administrators by adjusting the technical comptency required to "own" a server to the same level as what is required to install and use a smartphone app.
{{% /fragment %}}

---

### A return to the Semantic Web (on the cloud)

{{% fragment %}}
- Leverage RDF at the "edge" of p2p interactions
- "Glue" together data from disparate sources/apps via SPARQL
- Focus less on standards, more on building working prototypes that suit a particular need.
- Expose cloud-based server "pods" that communicate with each other via these channels
- QUIC as a transport layer

---


```mermaid
graph LR
      FriendPod((Friend's Pod)) --> SocialApp
      OtherFriend((Other Friend's Pod)) --> SocialApp
      UnknownPublicPod((Unknown Pod)) --> MicroBloggingApp
      AdminClient --> AdminApp
      subgraph Pod
      SocialApp --> Datastore[(Triplestore)]
      MicroBloggingApp --> Datastore
      AdminApp --> Datastore
      end
```

---
```mermaid
graph LR
      PodA --> PodB{Bob's Pod}
      PodB --> PodA{Alice's Pod}
      Agg[/Aggregator/] --> PodA
      Agg --> PodB
      ClientGary((Gary)) --> Agg
      Mila((Mila)) --> MilaPod{Mila's Pod}
      MilaPod --> Agg
```

---

what it's like trying to adopt Semantic Web Tech

![tech](mess.jpeg)

---

The root problem targeted by proposed "decentralized" schemes is accessible and reliable networked compute resources.

{{% note %}}
this also holds for things like IPFS and other distributed data stores
since servers run the world, it seems we've tried to elevate a network of home PC's into a substrate for buildilng a new web.

this will not work.
{{% /note %}}

---

Cloud computing is the confluence of [the] four revolutions:

- The Internet
- Distributed Version Control
- Open Source
- Moore's Law

---

There is currently a bounty of "free" interesting software tools...

{{% fragment %}}but they all are targeted towards developers {{% /fragment %}}

{{% fragment %}}We should begin to design for anyone capable of downloading and using "apps" on a smart phone {{% /fragment %}}

{{% note %}}
Cloud computing as a service allows web developers to forget about system administration and only focus on producing and deploying application-specific behavior

Users are plenty "technical"!  We as developers and product designers just need to prioritize that community as well.
{{% /note %}}

---

### A New Goal

Empower users with the ability and responsibility of managing their own cloud resources.

<small>
What if administering an application web server was as easy as installing and using a smartphone app?
</small>

{{% note %}}
The division between user "client" software and "server administration" is largely artificial.  While it may have made sense in a particular set of circumstances, we should not treat this application design as immutable or unique
{{% /note %}}

---

# Mermaid Sample

```mermaid
graph LR
  A --> B
  B --> C
```
