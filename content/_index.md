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

---


- {{< frag c="A schema design language + serialization formats (RDF and friends)" >}}
- {{< frag c="A query language with built-in logical inference capabilities (SPARQL)" >}}
- {{< frag c="Set a of protocols to coordinate server-server interactions (Linked Data Protocol)" >}}

---

### Unrealized Potential (Historically)

{{% fragment %}}
- Required high up-front design cost
- Full benefit only available in niche domains or with widespread adoption
- Too little bang for the buck for early adopters
{{% /fragment %}}

---

### SaaS

![keanu](keanu.jpg)

---

### Lessons to be Learned

Many Saas solutions enable low-effort discovery from massive datasets or communities followed by close interactions among a small group of participants.

---

### Ideas to Steal

{{% fragment %}}
SaaS meets enforces a consistent data schema for all participants which makes it possible to build efficient and predictable user interfaces.
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
A great deal of indirect attention is being directed to the under-appreciated problem of expanding access to cheap compute resources with highly reliable network connectivity.
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
{{% /fragment %}}

---

### Why cloud-backed p2p?

- Fine-grained and tweakable access controls
- Very cheap to handle more computationally intensive tasks
- All of a user's data across domains in one place and queryable

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

