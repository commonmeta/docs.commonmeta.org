---
title: Commonmeta
layout: hextra-home
cascade:
  - target:
      kind: page
    type: docs
---

<div class="hx:mt-6 hx:mb-6">
{{< hextra/hero-headline >}}
  Commonmeta
{{< /hextra/hero-headline >}}
</div>

<div class="hx:mb-12">
{{< hextra/hero-subtitle >}}
  A metadata standard for scholarly metadata,&nbsp;<br class="hx:sm:block hx:hidden" />focused on converting between formats.
{{< /hextra/hero-subtitle >}}
</div>

<div class="hx:mb-6">
{{< hextra/hero-button text="Get Started" link="introduction/" >}}
</div>

<div class="hx:mt-6"></div>

{{< hextra/feature-grid >}}
  {{< hextra/feature-card
    title="JSON Schema v1.0"
    subtitle="A stable, testable specification for works, persons, organizations, and containers."
    link="schema/"
  >}}
  {{< hextra/feature-card
    title="Many formats"
    subtitle="Read and write Crossref, DataCite, Schema.org, CSL-JSON, BibTeX, RIS, and more."
    link="implementations/"
  >}}
  {{< hextra/feature-card
    title="Shared conformance tests"
    subtitle="The Rust and Python implementations validate against the same schema and fixtures."
    link="https://codeberg.org/front-matter/commonmeta-schema"
  >}}
{{< /hextra/feature-grid >}}
