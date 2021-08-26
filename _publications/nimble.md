---
layout: article

type: conference
year: 2021
month: 07

title: 'Nimble: Scalable TCP-Friendly Programmable In-Network Rate-Limiting'
authors: ['Vineeth Sagar Thapeta','[Komal Shinde]','[Mojtaba Malekpourshahraki]', '[Darius Grassi]', '[Brent E. Stephens]','[Balajee Vamanan]']

DOI:
  target: ACM
  number: 10.1145/3482898.3483361

tweet: 'We define _overfitting_ in the context of CEGIS-based SyGuS,
        and show that there exists a tradeoff between expressiveness and performance.
        We present two mitigation strategies:
        **<small>(1)</small>** a black-box approach that any existing tool can use,
        and **<small>(2)</small>** a white-box technique called _hybrid enumeration_.'

target:
  short: SOSR
  full: 'ACM SIGCOMM Symposium on SDN Research (SOSR)'
  link: 'https://conferences.sigcomm.org/sosr/2021/program.html'

links:
  PDF: '%BASE_URL%/assets/pdf/nimble21.pdf'
  Tool: ''
  Slides: ''
---

###### Abstract
There is an emerging need for scalable high-performance in-network
rate-limiting because rate-limiters can be used to provide performance
isolation. However, existing approaches to in-network rate-limiting are not
scalable or TCP-friendly.

This paper presents the design of Nimble, a new approach to in-network
rate-limiting that is scalable, high performance, and TCP-friendly. Nimble uses
meters to scalably provide hardware rate-limiting without any dedicated queuing
or buffering resources, and Nimble uses ECN-Shaping for TCP-friendly rate-limit
enforcement. Nimble also introduces the first algorithm for configuring
in-network rate-limiters to enforce network-wide isolation policies.

Through a P4 implementation and experiments with a 100Gbps Barefoot Tofino
switch, we find that Nimble is immediately usable and can operate even with
high bandwidth rate-limits without needing to recirculate packets or rely on
hardware packet generators to generate token refill packets. This overcomes the
scalability limitations of prior approaches. Experiments with Apache and Redis
show that Nimble can reduce application-level latency by an order of magnitude
when compared to not using in-network rate-limiting, and ns-3 simulations
demonstrate that Nimble behaves well in larger clusters. We find that Nimble
can scale to 100K rate-limiters per-switch when implemented on a Barefoot
Tofino switch, and our new rate allocation algorithm reduces rate-limiter
updates by a factor of 10x–24x and improves network utilization by 24%.

###### BibTeX Citation

``` TBA ```
