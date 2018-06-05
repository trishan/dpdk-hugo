+++
identifier = "home"
+++

<section class="main-hero">
  <h2>DPDK is a set of libraries and drivers for fast packet processing</h2>
  <p class="tagline">
    DPDK is the Data Plane Development Kit that consists of libraries to accelerate packet processing workloads running on a wide variety of CPU architectures.
  </p>
</section>

#### Features:
---
- Designed to run on any processor
- Runs mostly in Linux userland
- DPDK is an Open Source BSD licensed project

<center>{{< button href="{{ .Site.BaseURL }}/download" >}} Download Now {{< /button >}}
</center>

##### Sample Architecture
----

{{<mermaid align="center">}}
graph LR;
    A[Hard edge] -->|Link| B(Round edge)
    B --> C{Decision}
    C -->|One| D[Result one]
    C -->|Two| E[Result two]
{{< /mermaid >}}
