---
title: "Open-Source Licenses: MIT, Apache 2.0, GPL and the Rules Behind the Code"
date: 2026-10-29
permalink: /posts/open-source-licenses/
tags:
  - open-source
  - software-engineering
  - licensing
  - developer-career
categories:
  - software-engineering
excerpt: "A practical guide to popular software licenses, why they exist, and how developers should choose and respect them."
header:
  image: /images/open-source-licenses-graphic.svg
  teaser: /images/open-source-licenses-graphic.svg
---

## Why software licenses exist

Software is protected by copyright as soon as someone creates it. That means you generally need permission from the copyright holder before copying, modifying, distributing, or selling the software.

An open-source license gives you that permission under clearly defined conditions.

For example, a license might allow commercial use but require attribution. Another might require derivative works to use the same license. Without a license, code that appears in a public repository should not automatically be treated as free to reuse. It is simply publicly visible.

This matters because modern applications are assembled from thousands of dependencies. Choosing or ignoring a license without understanding it can affect attribution, redistribution, patents, or source-code obligations.

> This article provides general engineering guidance, not legal advice. For important commercial products, consult a qualified lawyer.

---

## MIT License

The MIT License is short, permissive, and easy to understand. It allows people to use, copy, modify, merge, publish, distribute, sublicense, and sell the software.

The main requirement is to include the copyright notice and license text in copies or substantial portions of the software.

It is designed for projects that want to encourage broad adoption with very few restrictions.

**Common examples:** React, Python libraries, Node.js packages, and many personal and open-source projects.

**Choose MIT when:** you want a permissive library or developer tool to be used in almost any application.

**The tradeoff:** users can place MIT-licensed code inside closed-source software, and they do not have to share their improvements.

---

## Apache License 2.0

Apache 2.0 is also permissive, but it is longer and more detailed than MIT. It explicitly grants a patent license from contributors to users and includes language about patent retaliation if someone files patent claims against the project.

It also asks redistributors to preserve notices and include a copy of the license. If a project includes an Apache-licensed `NOTICE` file, that information must generally be preserved where required by the license.

**Common examples:** Kubernetes, TensorFlow, Apache Kafka, and many cloud-native projects.

**Choose Apache 2.0 when:** your project is used by companies, involves patents, or needs clearer legal language for enterprise adoption.

**The tradeoff:** Apache 2.0 is somewhat more complex than MIT and may require a more complete compliance process.

---

## BSD Licenses

BSD licenses are permissive family licenses, originally associated with the Berkeley Software Distribution operating system. Their exact terms vary by version, but modern BSD licenses usually require copyright and license notices when redistributing source or binaries.

The 2-Clause BSD License and 3-Clause BSD License are common. The additional clause in the three-clause version includes restrictions on using the names of contributors for endorsement.

**Common examples:** FreeBSD, components of macOS, Go-related projects, and research software.

**Choose BSD when:** you want a permissive license with slightly more explicit redistribution terms.

---

## GNU GPL and LGPL

The GNU General Public License is a **copyleft** license. If GPL-covered software is distributed, derivative works generally must also be distributed under the GPL and must provide corresponding source code under the GPL terms.

This model does not prevent commercial sales. Instead, it requires downstream redistribution to preserve the same freedom for users.

GPL can be strong protection for an open-source project, but it can discourage use in proprietary products because teams may worry that it creates source-disclosure obligations.

**LGPL** usually allows libraries under the LGPL to be linked by non-LGPL applications, with additional requirements depending on how the library is linked and distributed.

The exact GPL version and surrounding facts matter, so consult legal guidance if distribution terms are important to your project.

**Common examples:** Linux uses GPLv2, while components such as Git and many GNU tools use GNU licenses.

---

## Mozilla Public License 2.0

The Mozilla Public License is a **file-level** copyleft license. Changes to MPL-covered files must remain under MPL when redistributed, while larger applications can combine them with proprietary code.

It also provides a patent license and defines source-code distribution requirements.

**Common example:** Mozilla Firefox.

**Choose MPL when:** you want stronger sharing requirements than permissive licenses, but less broad copyleft than GPL.

---

## 0BSD and CC0

The zero-clause BSD License, or **0BSD**, removes most attribution and redistribution conditions and allows the software to be used without legal strings.

The Creative Commons **CC0 1.0 Universal** tool is a way for creators to waive copyright where legally possible. It is commonly used for data, documentation, and other creative works rather than a substitute for a software license unless the project owner understands the distinction.

**Choose 0BSD when:** you want to maximize reuse while keeping code covered as software.

**Choose CC0 when:** your goal is to dedicate data or a non-code creative work to the public domain as widely as the applicable law allows.

The choice between "public domain" and "licensed for no restrictions" depends on local copyright law, so it is worth checking carefully.

---

## Why developers use licenses

Licenses protect three groups:

- **Creators**: retain authorship while explaining what others may do.
- **Users**: receive predictable permission instead of uncertain informal usage.
- **Businesses**: reduce legal uncertainty before shipping or distributing a product.

A license cannot prevent every misuse, but it gives everyone a shared rulebook.

---

## How a new developer should choose a license

Ask six questions before adding a license:

1. Do you own or have permission to distribute every contribution?
2. Do you want proprietary products to use the code freely?
3. Do you want improvements returned to the community?
4. Is patent protection important?
5. Is the project a library, an application, documentation, or data?
6. Can your employer or collaborators agree on the same license?

For many small libraries, MIT is the simple default. For infrastructure and company-backed projects, Apache 2.0 is often attractive. For projects seeking strong source-sharing obligations, GPL may fit. For data and documentation, review dedicated options instead of automatically using a software license.

A project should always contain the license file and avoid contradictory license choices in source files.

---

## How to respect another developer's code

License compliance is about more than avoiding a lawsuit. It is respect for the people whose work is in the product.

A responsible developer should:

- **Read the license before copying dependencies or snippets.**
- **Preserve copyright notices and license text.**
- **Record third-party licenses in your application or repository.**
- **Follow source, attribution, and distribution requirements.**
- **Do not change or remove code headers just to hide its origin.**
- **Review transitive dependencies, not only direct packages.**
- **Do not upload someone else's private code to a public repository.**
- **Check your employer's policies before contributing upstream.**
- **Give credit where the license and community norms request it.**

For package managers, use an automated license inventory or supply-chain tool. Add license checks to CI when possible, and involve your legal or security team if terms are unclear.

---

## The simpler workflow

A clean workflow for software reuse is:

```text
1. Identify the dependency and its license.
2. Check whether your product distributes source, binaries, or a hosted service.
3. Verify attribution and notice requirements.
4. Keep an approved dependency inventory.
5. Use the license text in releases and source distributions.
6. Review conflicts or weakly licensed dependencies.
```

The fact that code is available on GitHub does not make it open source unless the repository clearly includes an applicable license.

---

## Popular license comparison

| License | Restrictions | Copyleft | Patent clause | Typical choice |
|---|---:|---:|---:|---|
| MIT | Attribution | No | No explicit clause | Small libraries and tools |
| Apache 2.0 | Notices, license inclusion | No | Yes | Enterprise and infrastructure |
| BSD | Copyright and notices | No | Depends on version | Permissive projects |
| GPL | Source-sharing requirements | Yes, broad | License includes terms | Strong open-source sharing |
| LGPL | Library and distribution terms | Limited | License includes terms | Libraries |
| MPL 2.0 | Source-sharing for MPL files | Yes, file-level | Yes | Codebases mixing proprietary and open code |
| 0BSD | Almost none | No | No explicit clause | Maximum reuse |

License compatibility is not guaranteed just because two licenses are permissive. When combining libraries or distributing modified software, inspect the full license texts and project policies.

---

## Final takeaway

Licenses are not paperwork that appears after engineering is finished. They are part of how software is designed, shared, distributed, and respected.

As a new developer, your goal is not to memorize every legal clause. It is to know that code has rules, check those rules early, preserve the contributions of others, and give maintainers the same care you would want for your own work.

When choosing a license for your project, make the decision deliberately. Add the license file. Explain the choice in your documentation. If the project grows into a company or commercial product, seek qualified legal advice.

**Good code can be reused. Good developers make sure it is reused responsibly.**
