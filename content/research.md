---
title: "Research Papers"
description: "Academic papers I have written and papers I have found worth reading."
hidemeta: true
showToc: false
---

<div class="research-section">

## Written

<div class="paper-card">
  <div class="paper-meta">
    <span class="paper-year">2018</span>
    <span class="paper-venue">ICIoTCT 2018 · Elsevier-SSRN</span>
  </div>
  <h3 class="paper-title">
    <a href="https://ssrn.com/abstract=3171519" target="_blank" rel="noopener">
      A Hénon Map based Cryptosystem for VQ based Compressed Video Data
    </a>
  </h3>
  <p class="paper-authors">Vandana Rathore, Ashish Verma, Aashish Kumar, Arup Kumar Pal</p>
  <p class="paper-abstract">Proposes a video cryptosystem built on top of Vector Quantization (VQ) based compression. I frames are compressed via codebook generation, while P and B frames are handled through a motion estimation scheme without compensation. The compressed data is then encrypted using a 2-D Hénon chaotic map, yielding high entropy in encrypted frames and no perceptible information leakage.</p>
</div>

</div>

<div class="research-section">

## Read

<p class="empty-state">Nothing here yet — check back soon.</p>

</div>

<style>
.research-section {
  margin-bottom: 3rem;
}

.research-section h2 {
  font-size: 1.1rem;
  font-weight: 700;
  letter-spacing: 0.06em;
  text-transform: uppercase;
  color: var(--secondary);
  border-bottom: 1px solid var(--border);
  padding-bottom: 0.5rem;
  margin-bottom: 1.5rem;
}

.paper-card {
  padding: 1.25rem 1.5rem;
  border: 1px solid var(--border);
  border-radius: 8px;
  background: var(--entry);
  margin-bottom: 1.25rem;
}

.paper-meta {
  display: flex;
  align-items: center;
  gap: 0.75rem;
  margin-bottom: 0.5rem;
}

.paper-year {
  font-size: 0.8rem;
  font-weight: 600;
  color: var(--primary);
  background: var(--border);
  padding: 0.15rem 0.5rem;
  border-radius: 4px;
}

.paper-venue {
  font-size: 0.82rem;
  color: var(--secondary);
}

.paper-title {
  font-size: 1rem;
  font-weight: 600;
  margin: 0 0 0.4rem 0;
  line-height: 1.4;
}

.paper-title a {
  color: var(--primary);
  text-decoration: none;
  border-bottom: 1px solid transparent;
  transition: border-color 0.15s ease;
}

.paper-title a:hover {
  border-bottom-color: var(--primary);
}

.paper-authors {
  font-size: 0.85rem;
  color: var(--secondary);
  margin: 0 0 0.75rem 0;
}

.paper-abstract {
  font-size: 0.88rem;
  color: var(--secondary);
  line-height: 1.65;
  margin: 0;
}

.empty-state {
  font-size: 0.9rem;
  color: var(--secondary);
  font-style: italic;
}
</style>
