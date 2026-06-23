---
layout: default
title: "Integrating blockchain and Internet of Things systems — A Systematic Review on Objectives and Designs"
description: "An inductive systematic review of 120 peer-reviewed blockchain-IoT integration studies, organised into 10 archetypes."
---

<section class="hero">
  <div class="hero-inner">
    <p class="venue-badge">
      <span class="venue-name">Journal of Network and Computer Applications</span>
      <span class="venue-sep">·</span>
      <span>Vol. 173</span>
      <span class="venue-sep">·</span>
      <span>Article 102844</span>
      <span class="venue-sep">·</span>
      <span>2021</span>
    </p>

    <h1 class="paper-title">Integrating blockchain and Internet of Things systems</h1>
    <p class="paper-subtitle">A Systematic Review on Objectives and Designs</p>

    <p class="authors">
      <span><strong>Nguyen Khoi Tran</strong><sup>1,2</sup></span>
      <span class="dot">·</span>
      <span><strong>M. Ali Babar</strong><sup>1,2</sup></span>
      <span class="dot">·</span>
      <span><strong>Jonathan Boan</strong><sup>3</sup></span>
    </p>

    <p class="affiliations">
      <sup>1</sup> School of Computer Science, The University of Adelaide, Australia &nbsp;
      <sup>2</sup> Centre for Research on Engineering Software Technology (CREST) &nbsp;
      <sup>3</sup> Defence Science and Technology Group, Australia
    </p>

    <div class="hero-actions">
      <a class="btn btn-primary" href="{{ '/assets/pdf/BC_IoT_Survey.pdf' | relative_url }}">⬇ Download PDF</a>
      <a class="btn btn-ghost" href="https://doi.org/10.1016/j.jnca.2020.102844" rel="noopener">View on ScienceDirect ↗</a>
    </div>
  </div>
</section>

<section class="section section--alt">
  <div class="container">
    <h2>TL;DR</h2>
    <p>
      We systematically reviewed <strong>120 peer-reviewed studies</strong> on blockchain-enabled IoT
      systems and asked two questions: <em>why</em> do IoT systems integrate blockchain, and
      <em>how</em> is the integration actually done? We extracted 17 features, organised them into a
      multi-perspective framework, and synthesised the findings into
      <strong>10 archetypes</strong> that capture the recurring patterns of blockchain-IoT
      integration. We hope these archetypes will be useful for classifying existing systems and guiding new ones.
    </p>
  </div>
</section>

<section class="section">
  <div class="container">
    <h2>At a glance</h2>
    <div class="stat-grid">
      <div class="stat">
        <div class="stat-value">120</div>
        <div class="stat-label">primary studies analysed</div>
      </div>
      <div class="stat">
        <div class="stat-value">778</div>
        <div class="stat-label">candidate works screened</div>
      </div>
      <div class="stat">
        <div class="stat-value">17</div>
        <div class="stat-label">extraction features</div>
      </div>
      <div class="stat">
        <div class="stat-value">10</div>
        <div class="stat-label">BC-IoT archetypes</div>
      </div>
    </div>
  </div>
</section>

<section class="section section--alt">
  <div class="container">
    <h2>Research method</h2>
    <p>
      We ran a four-phase Systematic Literature Review following Kitchenham et al.'s protocol:
      (1) a structured query across Scopus, IEEE Xplore, and ACM Digital Library;
      (2) coarse-grained selection on titles and abstracts; (3) fine-grained selection on full
      text; and (4) quality filtering. We cross-validated among the authors to reduce selection bias,
      and automated the parts that didn't need human judgement (Python de-duplication, prototype
      selection algorithm). Literature identification concluded in January 2020.
    </p>
    <figure class="figure">
      <img src="{{ '/assets/figures/SLR_overview.png' | relative_url }}" alt="Overview of the SLR research questions, review process, and key findings">
      <figcaption>
        Overview of the research questions, the four-phase review process, and the key findings.
      </figcaption>
    </figure>
  </div>
</section>

<section class="section">
  <div class="container">
    <h2>Multi-perspective framework</h2>
    <p>
      BC-IoT systems are complex. They carry decisions, trade-offs, and technical debt from
      both sides. To capture this, we organise the 17 extraction features around four angles:
    </p>
    <ul class="framework-list">
      <li><strong>Why</strong>: improvement objectives (quality attributes, new functionality) and the technical problems driving the integration.</li>
      <li><strong>How (IoT side)</strong>: where BC fits (logical and physical position) and what IoT systems offload to BC (on-chain and off-chain data and logic).</li>
      <li><strong>How (BC side)</strong>: the configuration of the integrated BC networks, including number, permission model, consensus protocol, and development platform.</li>
      <li><strong>Optimisation</strong>: how BC was tuned to fit IoT's resource, throughput, and off-chain-verification constraints.</li>
    </ul>
    <figure class="figure">
      <img src="{{ '/assets/figures/framework.png' | relative_url }}" alt="The multi-perspective framework for analysing BC-IoT systems">
      <figcaption>
        The multi-perspective framework: motivation, architecture, content, and configuration.
      </figcaption>
    </figure>
  </div>
</section>

<section class="section section--alt">
  <div class="container">
    <h2>What the literature is actually doing</h2>
    <p>Here are some of the numbers we extracted from the 120 studies.</p>

    <div class="finding">
      <h3>Top improvement objectives</h3>
      <div class="finding-grid">
        <div class="finding-item"><span class="num">74</span><span class="lbl">targeting <strong>data and program integrity</strong></span></div>
        <div class="finding-item"><span class="num">48</span><span class="lbl">targeting <strong>accountability</strong></span></div>
        <div class="finding-item"><span class="num">37</span><span class="lbl">targeting <strong>non-repudiation</strong></span></div>
      </div>
    </div>

    <div class="finding">
      <h3>Where BC fits inside IoT (top roles)</h3>
      <figure class="figure figure--small">
        <img src="{{ '/assets/figures/RQ2_affected_modules.png' | relative_url }}" alt="Distribution of functional modules that BC adds or replaces in IoT systems">
      </figure>
    </div>

    <div class="finding">
      <h3>Where BC nodes are deployed</h3>
      <figure class="figure figure--small">
        <img src="{{ '/assets/figures/RQ2_deployment.png' | relative_url }}" alt="Distribution of BC deployment patterns across edge, fog, and cloud">
      </figure>
    </div>

    <div class="finding">
      <h3>Problem categories being addressed</h3>
      <figure class="figure figure--small">
        <img src="{{ '/assets/figures/RQ1_problem_categories.png' | relative_url }}" alt="Distribution of the five problem categories addressed by BC-IoT integration">
      </figure>
    </div>
  </div>
</section>

<section class="section">
  <div class="container">
    <h2>The 10 archetypes</h2>
    <p>
      We distilled these patterns from the literature. Most real BC-IoT systems combine multiple
      archetypes and adapt them to their context. These are the templates they draw from.
    </p>

    <div class="archetypes-grid">
      <div class="archetype">
        <div class="archetype-num">01</div>
        <h3>Facilitator of M2M trading</h3>
        <p>Records and directs the business processes that govern machine-to-machine exchanges of resources (energy, data, compute).</p>
      </div>

      <div class="archetype">
        <div class="archetype-num">02</div>
        <h3>Recorder of provenance</h3>
        <p>Improves interoperability between IoT systems to enable tracking of physical entities moving across organisational boundaries.</p>
      </div>

      <div class="archetype">
        <div class="archetype-num">03</div>
        <h3>Access control manager</h3>
        <p>Decentralised access control for incoming and outgoing requests of IoT devices, data, and services, including collaborative whitelisting.</p>
      </div>

      <div class="archetype">
        <div class="archetype-num">04</div>
        <h3>Authentication manager</h3>
        <p>Decentralised authentication for devices, services, and users, with tamper-proof identity records.</p>
      </div>

      <div class="archetype">
        <div class="archetype-num">05</div>
        <h3>Trust rating manager</h3>
        <p>Secure storage and update of trust and reputation ratings of participants in IoT systems.</p>
      </div>

      <div class="archetype">
        <div class="archetype-num">06</div>
        <h3>Update distribution infrastructure</h3>
        <p>Maintains integrity of security patches and incentivises peer-to-peer firmware distribution via smart contracts.</p>
      </div>

      <div class="archetype">
        <div class="archetype-num">07</div>
        <h3>Intra-system communication channel</h3>
        <p>Secure shared storage that devices within one IoT system use to exchange data and instructions.</p>
      </div>

      <div class="archetype">
        <div class="archetype-num">08</div>
        <h3>Inter-system communication channel</h3>
        <p>Secure shared storage linking devices in different trust domains (for example, distributed agents in collaborative DDoS detection).</p>
      </div>

      <div class="archetype">
        <div class="archetype-num">09</div>
        <h3>Secure data storage</h3>
        <p>Tamper-proof database of data entries, or of pointers (hashes) to off-chain data, with integrity guaranteed by consensus.</p>
      </div>

      <div class="archetype">
        <div class="archetype-num">10</div>
        <h3>Secure computing platform</h3>
        <p>Uses smart contracts to run trusted computations across the network's mutually distrustful IoT nodes.</p>
      </div>
    </div>
  </div>
</section>

<section class="section section--alt">
  <div class="container">
    <h2>Abstract</h2>
    <p>
      We have witnessed the emergence of the Internet of Things (IoT) systems that incorporate
      blockchain (BC) elements in their architecture. Discrepancies between the requirements of IoT
      systems and the characteristics of BC networks mean that the motivations and design of these
      blockchain-enabled IoT systems (BC-IoT) are not only intriguing from a research perspective
      but also invaluable in practice. In this paper we present an inductive study of the "why" and
      "how" of BC-IoT systems through a Systematic Literature Review of 120 peer-reviewed studies.
      To capture the diverse nature of BC-IoT integration, we proposed and applied a
      multi-perspective framework to analyse the existing systems. Regarding their motivations, we
      studied the improvement objectives and the technical problems that drive the integration of BC.
      Regarding the design, we captured the position of BC within IoT systems as well as the content
      and processes that IoT systems offload to BC. As these dimensions are not mutually exclusive,
      they constitute a rich and multi-angle view of BC-IoT integration. Based on these findings, we
      defined 10 archetypes of BC-IoT systems that embody the core patterns of usage and configuration
      of BC in IoT systems.
    </p>
  </div>
</section>

<section class="section">
  <div class="container">
    <h2>BibTeX</h2>
    <pre class="bibtex"><code>@article{Tran2021bc_iot_slr,
  author    = {Tran, Nguyen Khoi and Babar, M. Ali and Boan, Jonathan},
  title     = {Integrating Blockchain and Internet of Things Systems:
               A Systematic Review on Objectives and Designs},
  journal   = {Journal of Network and Computer Applications},
  volume    = {173},
  pages     = {102844},
  year      = {2021},
  issn      = {1084-8045},
  publisher = {Elsevier},
  address   = {Amsterdam, Netherlands},
  doi       = {10.1016/j.jnca.2020.102844},
  url       = {https://doi.org/10.1016/j.jnca.2020.102844},
  keywords  = {Blockchain, Distributed Ledger, Smart Contract,
               Web of Things, Internet of Things, Systematic Review}
}</code></pre>

    <p class="doi-line">
      DOI: <a href="https://doi.org/10.1016/j.jnca.2020.102844" rel="noopener">10.1016/j.jnca.2020.102844</a>
    </p>
  </div>
</section>