# This Is The World Site

[![Build Status](https://travis-ci.org/scientific-defense-force/this-is-the-world-site.svg?branch=master)](https://travis-ci.org/scientific-defense-force/this-is-the-world-site) [![Join the chat at https://gitter.im/scientific-defense-force](https://badges.gitter.im/scientific-defense-force.svg)](https://gitter.im/scientific-defense-force/Lobby?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge&utm_content=badge)

## Introduction

This repo is for [thisistheworld.net](https://thisistheworld.net). The goal of this site is to communicate the level of economic inequality in the world. This includes the desperateness of the world's large majority of poor people and the first worlds parasitic relationship with them.

The target audience is the first world middle class.

## Why?

Capitalism and globalization are causing a lot of problems, but nothing will change unless the global middle class are aware of the issues. Currently they appear to be vaguely aware of the inequality but don't perceive the parasitism.

## Data

Data is produced by using the [Credit Suisse yearly global wealth report](https://www.credit-suisse.com/au/en/about-us/research/research-institute/global-wealth-report.html) and this code https://github.com/scientific-defense-force/this-is-the-world-ingestion .

## Technical

To run the site install [docker](https://www.docker.com/products/docker) (note: on linux you will also need to manually install [docker compose](https://docs.docker.com/compose/install)) and then

```bash
auto/run
```

Site can be accessed at http://localhost:4000

### Running in prod mode

```bash
auto/prod-environment
```

### Updating dependencies

```bash
auto/update/update-all
```

### Verifying changes

This currently checks:

- the links are valid with [html-proofer](https://github.com/gjtorikian/html-proofer)
- spelling mistakes via [hunspell](http://hunspell.github.io)
- yaml issues with [yamllint](https://yamllint.readthedocs.io)
- docker issues with [hadolint](https://github.com/hadolint/hadolint)
- shell issues with [shellcheck](https://github.com/koalaman/shellcheck)

```bash
auto/verify/verify-all
```

#### Adding new words to be skipped by the spell checker

Update the [custom dictionary](/custom-dict.dic) file. I don't understand [the format](https://www.elastic.co/guide/en/elasticsearch/guide/current/hunspell.html) very well..

### Browser Support

These browsers and versions http://browsehappy.com
