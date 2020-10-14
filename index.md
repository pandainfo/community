<p align="center">
  <a href="https://github.com/pandainfo/panda">
    <img alt="Panda" src="https://avatars2.githubusercontent.com/u/48161788?s=200&v=4" height="100">
  </a>
</p>

<p align="center">
  <strong>stay radical!  🐼  read books!  📚</strong>
  <br />
  Built in Vienna with ❤️
</p>

> **ATTENTION: This project is in early alpha stage, so things may change quickly.**

<!--
[![AGPL-3.0 License](https://flat.badgen.net/github/license/pandainfo/panda)](LICENSE.md)
[![Latest Version](https://flat.badgen.net/packagist/v/pandainfo/panda)](https://packagist.org/packages/pandainfo/panda)
[![Build Status](https://flat.badgen.net/github/checks/pandainfo/panda?label=build&icon=github)](https://github.com/pandainfo/panda/actions)
[![Monthly Downloads](https://flat.badgen.net/packagist/dm/pandainfo/panda)](https://packagist.org/packages/pandainfo/panda/stats)
 -->
[![PHP Composer](https://github.com/pandainfo/panda/workflows/PHP%20Composer/badge.svg)](https://github.com/pandainfo/panda/actions?query=workflow%3A%22PHP+Composer%22)
[![Publish Panda Docs](https://github.com/pandainfo/panda/workflows/Publish%20Panda%20Docs/badge.svg)](https://github.com/pandainfo/panda/actions?query=workflow%3A%22Publish+Panda+Docs%22)
[![Follow @redtux](https://flat.badgen.net//twitter/follow/redtux)](https://twitter.com/redtux)

# Welcome to Panda

**[Panda](https://github.com/pandainfo/panda)** aims to provide a modern new generation CRM, ERP and CMS with [ONIX] and [EANCOM] support
for selling, merchandising and searching books and digital media.

[ONIX]: https://en.wikipedia.org/wiki/ONIX_for_Books "ONIX for Books on Wikipedia"
[EANCOM]: https://en.wikipedia.org/wiki/XML/EDIFACT "XML/EDIFACT on Wikipedia"

> **Powered by**

* [![Build Status](https://img.shields.io/github/stars/ampproject/amp-wp.svg?style=flat-square)](https://github.com/ampproject/amp-wp) [**AMP Framework**](https://github.com/ampproject/amp-wp)
* [![Build Status](https://img.shields.io/github/stars/roots/bedrock.svg?style=flat-square)](https://github.com/roots/bedrock) [**Bedrock**](https://roots.io/bedrock/)
* [![Build Status](https://img.shields.io/github/stars/composer/composer.svg?style=flat-square)](https://github.com/composer/composer) [**Composer**](https://getcomposer.org)
* [![Build Status](https://img.shields.io/github/stars/moby/moby.svg?style=flat-square)](https://github.com/moby/moby) [**Docker Engine**](https://docs.docker.com/engine/)
* [![Build Status](https://img.shields.io/github/stars/tomusborne/GeneratePress.svg?style=flat-square)](https://github.com/tomusborne/GeneratePress) [**GeneratePress**](https://github.com/tomusborne/GeneratePress)
* [![Build Status](https://img.shields.io/github/stars/squidfunk/mkdocs-material.svg?style=flat-square)](https://github.com/squidfunk/mkdocs-material) [**Material for MkDocs**](https://github.com/squidfunk/mkdocs-material)
* [![Build Status](https://img.shields.io/github/stars/WordPress/WordPress.svg?style=flat-square)](https://github.com/WordPress/WordPress) [**WordPress Core**](https://make.wordpress.org/core/components/)

For full documentation visit the [docs](docs) pages.

<!-- Abbreviations used by MkDocs for building a glossary -->
<!-- https://squidfunk.github.io/mkdocs-material/reference/abbreviations/ -->
--8<-- "mkdocs/abbreviations.md"

---

> **Table of contents**

1. [About](#about)
2. [TODOs](#todos)
3. [Authors](#authors)
4. [Licensing](#licensing)

## About

> **PANDA – NEXT GENERATION E-COMMERCE PLATFORM**

Panda integrates several components in one system.

* [ ] **Website Builder:** Creating secure and fast Panda Landing Pages in static HTML
* [ ] **ActivityPub:** Running booksellers associations using Panda Fediverse Social Networks
* [ ] **CMS:** Writing publications in teams powered by the Panda Editorial Board
* [ ] **DMS:** Organizing all paperwork with Panda Document Management
* [ ] **eCommerce:** Buying and searching books on the Panda Store
* [ ] **Library:** Organizing titles and bibliographies in the Panda Book Catalog with ONIX & OPAC
* [ ] **Accounting:** Maintaining control over all business assets with Panda Finances
* [ ] **ERP:** Controlling the warehouse with Panda Merchandise Management
* [ ] **SCM:** Planning warehouse logistics through the Panda Supply-Chain-Management with dispatch lists and EDIFACT/EANCOM
* [ ] **CRM:** Simplifying marketing and guest care with Panda Customer Management
* [ ] **HRM:** Coordinating shifts, working hours and responsibilities of co-workers and teams with Panda Staff
* [ ] **Customizations:** Fulfilling your wishes with Panda Custom Solutions
* [ ] **Panda Stack:** Deploying Productive & Test Environments
* [ ] **Support:** Assisting with Discussion Boards, Trainings, Webinars, Documentation & Tutorials

The Panda platform is primarily being developed and supported
by Pablo Hörtner for Panda IT Solutions
with contributions from the community.

Like many other projects nowadays, Panda IT Solutions have
a [Code of Conduct], comparable to the old days' [Netiquette].

The project is licensed under the [GNU AGPL, Version 3.0][agpl].
It may be used only in compliance with this license.
For details [see below](#️licensing).

**Happy hacking!** 💜🤓

[code of conduct]: CODE_OF_CONDUCT.md "Contributor Covenant Code of Conduct"
[Netiquette]: https://tools.ietf.org/html/rfc1855 "Netiquette Guidelines from October 1995"
[agpl]: https://www.gnu.org/licenses/agpl-3.0.html "GNU Affero General Public License"

## TODOs

* [ ] Add features described above as plugins and via WP-CLI
  * [ ] Static Site Builder
  * [ ] ActivityPub
  * [x] CMS Creator
  * [ ] WooCommerce
  * [ ] ONIX Import
  * [ ] CRM
  * [ ] Newsletter management
  * [ ] ERP
  * [ ] SCP incl. EDIFACT support
  * [ ] DMS
  * [ ] Accounting (FinanzOnline)
  * [ ] HRM
* [ ] Test Panda scripts in `bin/` with more OSes (Ubuntu only so far)
* [x] Add PhpMyAdmin to Panda Services
* [x] Rename `README.md` title to **NEXT GENERATION E-COMMERCE PLATFORM**
  * [ ] Explain markdown and new generation e-commerce
  * [ ] Explain separation of content and presentation
  * [ ] Explain micro-services and dependency management
  * [ ] Explain automation, clouds, CI/CD, CDN, etc.
* [x] Move quickstart instructions from `README.md` to `docs/`
* [x] Move copyright information from `README.md` to `docs/`
* [x] Move `LICENSE.md` to `docs/`
* [x] Move `AUTHORS.md` to `docs/`
* [x] Move `CODE_OF_CONDUCT.md` to `docs/code-of-conduct.md`
* [ ] Add EDIFACT page to `docs/`
* [ ] Add ONIX page to `docs/`
* [ ] Include Panda Core docs
* [x] Add `.env` to GitHub secrets
* [x] Create WP instance on sprit.org
* [x] Create deploy GitHub Actions for
  * [ ] development
  * [ ] staging
  * [ ] production
* [x] Deploy to Hetzner via sftp

## Authors

- **Pablo Hörtner** - _Initial work_ - [🐼 Team panda!](https://github.com/orgs/pandainfo/teams/panda)

See also the [AUTHORS.md](docs/AUTHORS.md) file and the [full list of contributors](https://github.com/pandainfo/panda/contributors) who participated in this project.

## Licensing

    PANDA – NEXT GENERATION E-COMMERCE PLATFORM
    COPYRIGHT (c) 2020  PABLO HÖRTNER <REDTUX@PM.ME>

Unless explicitly noted otherwise, all the content on this site is released under the following terms.

For further information see [copyright.md](docs/copyright.md).

This project is free software: you can redistribute it and/or modify it under the terms of the **GNU Affero General Public License** as published by the Free Software Foundation, either version 3 of the License, or (at your option) any later version.

    Unless required by applicable law or agreed to in writing, software
    distributed under the License is distributed on an "AS IS" BASIS,
    WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
    See the License for the specific language governing permissions and
    limitations under the License.

You may obtain a copy of the License [here](LICENSE) or at

    https://www.gnu.org/licenses/agpl-3.0.html
