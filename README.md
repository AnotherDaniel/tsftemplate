<!--
 * Copyright (C) 2026 Eclipse Foundation and others. 
 * 
 * This program and the accompanying materials are made available under the
 * terms of the Eclipse Public License v. 2.0 which is available at
 * http://www.eclipse.org/legal/epl-2.0.
 * 
 * SPDX-FileType: DOCUMENTATION
 * SPDX-FileCopyrightText: 2026 Eclipse Foundation
 * SPDX-License-Identifier: EPL-2.0
-->

[![TSF Score](https://img.shields.io/badge/dynamic/json?url=https%3A%2F%2Fanotherdaniel.github.io%2Ftsftemplate%2Ftrustable%2Fscore.json&query=%24.scores%5B0%5D.score&label=TSF%20Score&color=blue)](https://anotherdaniel.github.io/tsftemplate/trustable/dashboard.html)
[![TSF Report](https://img.shields.io/github/v/release/AnotherDaniel/tsftemplate?label=TSF%20Report&color=green)](https://anotherdaniel.github.io/tsftemplate/trustable/trustable_report_for_tsftemplate.html)

---

<!--
`impl~project-readme~1`
Covers:
- req~project-readme~1
-->

# tsftemplate - a getting-started template for applying the Trustable Software Framework

The `tsftemplate` repository is a hello-world style template illustrating how to build CI pipelines that automate the linking and collection of [Trustable Software Framework (TSF)](https://gitlab.eclipse.org/eclipse/tsf/tsf) statement evidence, the scoring of the resulting TSF graph, and generation of a TSF report.

The heart of `tsftemplate` is a release workflow which serves to illustrate how [`tsffer` ("TSF transfer")](https://github.com/AnotherDaniel/tsffer) and [`tsflink`](https://github.com/AnotherDaniel/tsflink) GitHub actions can be used in CI pipelines to automate the process of collecting TSF evidence, linking it into an existing TSF argument, and performing the scoring and report generation as part of a release flow. The result of this automation is a detailed TSF report published alongside the project release artifacts, including links to follow up on any evidence that is used to support project TSF statements.

## Trustable Software Framework context

The [Eclipse Trustable Software Framework (TSF)](https://pages.eclipse.dev/eclipse/tsf/tsf/) approach is designed for consideration of software where factors such as safety, security, performance, availability and reliability are considered critical. TSF method asserts that any consideration of trust must be based on evidence.

TSF considers that delivery of software for critical systems must involve identification and management of the risks associated with the development, integration, release and maintenance of the software. In such contexts, software delivery is not complete without appropriate documentation and systems in place to review and mitigate these risks. The Eclipse Trustable Software Framework provides a method and tool consider supply chain and tooling risks as well as the risks inherent in pre-existing or newly developed software, and to apply statistical methods to measure confidence of the whole solution.

The TSF method places an emphasis on integrating well into a typical Open Source development process, by being built around versionable and bite-sized textual statements that get organized in a [DOT graph](https://en.wikipedia.org/wiki/DOT_(graph_description_language)) - thus immediately benefitting from the associated tooling ecosystem. It comes with cli tool for manipulating the TSF dot-graph (`trudag`), immediately suggesting application in CI/automation workflows.

## tsftemplate motivation

All Open Source projects typically share one challenge: [they are severely understaffed](https://xkcd.com/2347/ "xkcd 2347"). All idiosyncrasies and best practices pursued by Open Source projects result from this:

- any repetitive tasks must be automated
- developers hate to repeat themselves; all information relevant to the project must be easily accessible, within or very close to the source code repository
- work done for the project must have tangible and plausible benefits; there is no time for make-work and write-only documentation purely for the sake of process

The TSF method aims to be a viable software quality framework for such contexts, by being file-centric, openly available, conceptually simply, and automatable (to a degree). However, applying the method from scratch still comes with a non-trivial learning curve, especially for people who are new to the world of formalized software quality processes.

At the same time, open development models offer unique opportunities for crossing such hurdles, by community-sourcing method-tailoring for frequent scenarios, central touchpoints for related questions and advice, and providing best-practice getting-started templates that showcase how the method could be applied. `tsftemplate` aims to be such a template.

## tsftemplate goals

As a template for applying the TSF method, `tsftemplate` pursues three goals:

1. Be a hello-world style illustration of the overall approach - how is TSF supposed to be applied conceptually, what is the underlying idea?
2. Show how TSF can be integrated into a CI workflow - along with other related tools - to implement an automated pipeline around quality process artifacts.
3. Serve as a copy-paste template for setting up your own TSF-enabled quality process infrastructure.

## The 3 stages of quality process application

For the purposes of structuring TSF application in `tsftemplate`, we posit three activity stages:

1. Tailoring: the scope and extent of quality method application needs to be chosen, and a starting point found.
2. Engineering/application: the tailored method scope needs to be applied in the project, and related statements, evidences and artifacts created and identified.
3. Measuring and reporting: pulling together quality statements, code and documentation evidence and build artifacts, quality assessment and reporting can be done.

![tsftemplate helps to streamline the 3 stages of a TSF-driven software quality process.](docs/img/tsftemplate-vision.drawio.svg "tsftemplate Vision")

Each stage comprises a set of activities and related tools, that `tsftemplate` aims to provide a reference for, and that are described in greater detail below. By providing this starting point, `tsftemplate` wants to provide inspiration about how the approach might be streamlined and automated as much as possible.

Please have a look at the detailed [description of the 3 stages and their implementation](docs/three_stages.md)

## Hands-on - how one quality item flows through the `tsftemplate` process

To make the practical application of the `tsftemplate` approach to TSF more tangible, we offer a step-by-step description of how a [quality item flows through the three stages](docs/one_item.md), with references to implementation in this project as well as supporting tool documentation.

## Todos

- further thoughts; about safety engineering and that being before-scope, and about separation of tsftemplate guts from actual applying project
- README scope: what is this *NOT*?
