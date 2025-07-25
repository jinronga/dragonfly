# Dragonfly

![alt][logo-linear]

[![GitHub release](https://img.shields.io/github/release/dragonflyoss/dragonfly.svg)](https://github.com/dragonflyoss/dragonfly/releases)
[![Artifact Hub](https://img.shields.io/endpoint?url=https://artifacthub.io/badge/repository/dragonfly)](https://artifacthub.io/packages/search?repo=dragonfly)
[![OpenSSF Scorecard](https://api.scorecard.dev/projects/github.com/dragonflyoss/dragonfly/badge)](https://scorecard.dev/viewer/?uri=github.com/dragonflyoss/dragonfly)
[![CI](https://github.com/dragonflyoss/dragonfly/actions/workflows/ci.yml/badge.svg?branch=main)](https://github.com/dragonflyoss/dragonfly/actions/workflows/ci.yml)
[![Go Report Card](https://goreportcard.com/badge/github.com/dragonflyoss/dragonfly?style=flat-square)](https://goreportcard.com/report/github.com/dragonflyoss/dragonfly)
[![Discussions](https://img.shields.io/badge/discussions-on%20github-blue?style=flat-square)](https://github.com/dragonflyoss/dragonfly/discussions)
[![OpenSSF Best Practices](https://www.bestpractices.dev/projects/10432/badge)](https://www.bestpractices.dev/projects/10432)
[![Twitter](https://img.shields.io/twitter/url?style=social&url=https%3A%2F%2Ftwitter.com%2Fdragonfly_oss)](https://twitter.com/dragonfly_oss)
[![LICENSE](https://img.shields.io/github/license/dragonflyoss/dragonfly.svg?style=flat-square)](https://github.com/dragonflyoss/dragonfly/blob/main/LICENSE)
[![FOSSA Status](https://app.fossa.com/api/projects/git%2Bgithub.com%2Fdragonflyoss%2Fdragonfly.svg?type=shield&issueType=license)](https://app.fossa.com/projects/git%2Bgithub.com%2Fdragonflyoss%2Fdragonfly?ref=badge_shield&issueType=license)
[![LFX Health Score](https://img.shields.io/static/v1?label=Health%20Score&message=Healthy&color=A7F3D0&logo=linuxfoundation&logoColor=white&style=flat)](https://insights.linuxfoundation.org/project/d7y)
[![CLOMonitor](https://img.shields.io/endpoint?url=https://clomonitor.io/api/projects/cncf/dragonfly/badge)](https://clomonitor.io/projects/cncf/dragonfly)

Provide efficient, stable and secure file distribution and image acceleration
based on p2p technology to be the best practice and
standard solution in cloud native architectures.

## Introduction

Dragonfly is an open source P2P-based file distribution and
image acceleration system. It is hosted by the
Cloud Native Computing Foundation ([CNCF](https://cncf.io/)) as
an Incubating Level Project.
Its goal is to tackle all distribution problems in cloud native architectures.
Currently Dragonfly focuses on being:

- **Simple**: Well-defined user-facing API (HTTP), non-invasive to all container engines;
- **Efficient**: Seed peer support, P2P based file distribution to save enterprise bandwidth;
- **Intelligent**: Host-level speed limit, intelligent flow control due to host detection;
- **Secure**: Block transmission encryption, HTTPS connection support.

## Architecture

![alt][arch]

**Manager:** Maintain the relationship between each P2P cluster, dynamic configuration management and RBAC.
It also includes a front-end console, which is convenient for users to visually operate the cluster.

**Scheduler:** Select the optimal download parent peer for the download peer. Exceptions control Dfdaemon's back-to-source.

**Seed Peer**: Dfdaemon turns on the Seed Peer mode can be used as
a back-to-source download peer in a P2P cluster,
which is the root peer for download in the entire cluster.

**Peer**: Deploy with dfdaemon, based on the C/S architecture, it provides the `dfget` command download tool,
and the `dfget daemon` running daemon to provide task download capabilities.

## Documentation

You can find the full documentation on the [d7y.io][d7y.io].

## Security

### Security Audit

A third party security audit was performed by Trail of Bits,
you can see the [full report](docs/security/dragonfly-comprehensive-report-2023.pdf).

### Security Policy

If you discover a security vulnerability within Dragonfly, please report it according to our [Security Policy](https://github.com/dragonflyoss/community/blob/master/SECURITY.md).

### Security Insights

You can find the security insights on the [SECURITY-INSIGHTS.yml](SECURITY-INSIGHTS.yml) file.

## Community

Join the conversation and help the community. We have a number of ways for you to get involved:

- **Slack Channel**: [#dragonfly](https://cloud-native.slack.com/messages/dragonfly/) on [CNCF Slack](https://slack.cncf.io/)
- **Github Discussions**: [Dragonfly Discussion Forum][discussion]
- **Developer Group**: <dragonfly-developers@googlegroups.com>
- **Maintainer Group**: <dragonfly-maintainers@googlegroups.com>
- **Twitter**: [@dragonfly_oss](https://twitter.com/dragonfly_oss)
- **DingTalk**: [22880028764](https://qr.dingtalk.com/action/joingroup?code=v1,k1,pkV9IbsSyDusFQdByPSK3HfCG61ZCLeb8b/lpQ3uUqI=&_dt_no_comment=1&origin=11)

and you can also seek the main community information in the [community repository](https://github.com/dragonflyoss/community).
In this repository, you can find the [community meeting minutes, community meeting notes, and more](https://github.com/dragonflyoss/community/tree/master/meetings).

We wonderinng if you have any questions or suggestions, please feel free to feedback to us through the above channels.

## Roadmap

You can find the [roadmap](https://github.com/dragonflyoss/community/blob/master/ROADMAP.md)
in the [community repository](https://github.com/dragonflyoss/community).
Dragonfly is a community-driven project, and we welcome contributions from everyone.

## Contributing

You should check out our
[CONTRIBUTING][contributing] and develop the project together.

## Code of Conduct

Please refer to our [Code of Conduct][codeconduct] which applies to all Dragonfly community members.

## Software bill of materials

SBOMs for the following categories are produced by the Dragonfly Project:

- Considering the source code repository
- For the dragonfly project's sub-project

The SBOMs can be downloaded from the following places:
Github Release/Tag Resources Github workflow resources for more process executions.

[arch]: docs/images/arch.png
[logo-linear]: docs/images/logo/dragonfly-linear.svg
[discussion]: https://github.com/dragonflyoss/dragonfly/discussions
[contributing]: https://github.com/dragonflyoss/community/blob/master/CONTRIBUTING.md
[codeconduct]: https://github.com/dragonflyoss/community/blob/master/CODE_OF_CONDUCT.md
[d7y.io]: https://d7y.io/
