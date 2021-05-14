---
title: "Five design principles"
slug: "five-design-principles"
date: 2021-05-11T10:41:49+01:00
authors: ["Tom Dyson"]
tags:
- architecture
- systems
- digital stage
---

We're building a new 'Digital Stage' for the Royal Opera House, responding to and preparing for a new world where the majority of our growing audience is no longer in our [cherished theatres](https://www.roh.org.uk/about/history), but in cinemas, homes, schools, on the train. We want to do justice to the spectacular opera and ballet performances that are recorded and streamed from Covent Garden, by focusing hard on quality (audio and video capture and encoding; low latency streaming; player optimisations) and by reducing as much friction as possible between our passionate audience and our wonderful content.

![Content flow diagram](/images/ds2-map.png)

But -- just like live productions on our physical stage -- a seamless experience for our users requires a lot of joining up behind the scenes. We have many sources of content, many interlocking systems, many technicians, writers, lawyers and performers who contribute to the final product. To steer our way towards building a digital stage which meets our stringent quality tests, we're adopting a set of straightforward systems design principles:

## 1. Use existing services to their full extent

Understand and take full use of our existing tools: our CMS, our cast data platform, our CRM, our encoding platform, our CDN. Be wary of introducing new, overlapping tools that need support, maintenance and training. Fill in any gaps with the least code possible.

## 2. Reduce points of failure for end-users

Public-facing interfaces should rely on as few end-points as possible, and only end-points that auto-scale in the cloud.

## 3. No copy paste

No-one should have to input the same content twice. It's undesirable, but acceptable, that some content may exist in two places, but we'll always be clear about the ultimate source of truth, and any duplication of content should be carried out by code, not humans.

## 4. Make all key services swappable

Future versions of the platform may substitute key components: as the volume of our content grows, we may switch to a dedicated video CMS, or run FFmpeg in-house, or negotiate with a new CDN provider. All our integrations should be designed with swappability in mind, so we can choose best-in-class tools when they become available.

## 5. Prefer known technologies

Our current expertise is in Typescript, React, relational databases, AWS. Wherever possible we'll choose technologies that play to these strengths; delivering this product takes priority over learning shiny new tools, at least for the next few months!
