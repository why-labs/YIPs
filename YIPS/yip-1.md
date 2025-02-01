---
yip: 1
title: YIP Purpose and Guidelines
status: Living
type: Meta
author: AdeThorMiwa <adethormiwa1@gmail.com>, et al.
created: 2025-02-01
---

## What is an YIP?

YIP stands for Y Improvement Proposal. An YIP is a design document providing information to the Y Labs community, or describing a new feature or product for Y or its processes or environment. The YIP should provide a concise technical specification of the feature and a rationale for the feature. The YIP author is responsible for building consensus within the community and documenting dissenting opinions.

## YIP Rationale

We intend YIPs to be the primary mechanisms for proposing new features, proposing new product, for collecting community inputs on an issue, and for documenting the design decisions that have gone into Y Labs and it's product. Because the YIPs are maintained as text files in a versioned repository, their revision history is the historical record of the feature proposal.

For Y contributors, YIPs are a convenient way to track the progress of their work. Ideally each product maintainer would list the YIPs that they have worked on. This will give end users a convenient way to know the current status of a given product or feature.

## YIP Types


## YIP Work Flow

### Shepherding an YIP

Parties involved in the process are you, the champion or *YIP author*, the [*YIP editors*](#yip-editors), and ...

### YIP Process

The following is the standardization process for all YIPs in all tracks:

![YIP Status Diagram](../assets/yip-1/YIP-process-update.jpg)

**Idea** - An idea that is pre-draft. This is not tracked within the YIP Repository.

**Draft** - The first formally tracked stage of a YIP in development. A YIP is merged by a YIP Editor into the YIP repository when properly formatted.

**Review** - An YIP Author marks an YIP as ready for and requesting Peer Review.

**Last Call** - This is the final review window for a YIP before moving to `Final`. An YIP editor will assign `Last Call` status and set a review end date (`last-call-deadline`), typically 14 days later.

If this period results in necessary normative changes it will revert the YIP to `Review`.

**Final** - This YIP represents the final standard. A Final YIP exists in a state of finality and should only be updated to correct errata and add non-normative clarifications.

A PR moving an YIP from Last Call to Final SHOULD contain no changes other than the status update. Any content or editorial proposed change SHOULD be separate from this status-updating PR and committed prior to it.

**Stagnant** - Any YIP in `Draft` or `Review` or `Last Call` if inactive for a period of 6 months or greater is moved to `Stagnant`. An YIP may be resurrected from this state by Authors or YIP Editors through moving it back to `Draft` or its earlier status. If not resurrected, a proposal may stay forever in this status.

>*YIP Authors are notified of any algorithmic change to the status of their YIP*

**Withdrawn** - The YIP Author(s) have withdrawn the proposed YIP. This state has finality and can no longer be resurrected using this YIP number. If the idea is pursued at later date it is considered a new proposal.

**Living** - A special status for YIPs that are designed to be continually updated and not reach a state of finality. This includes most notably YIP-1.

## What belongs in a successful YIP?

Each YIP should have the following parts:


## YIP Formats and Templates

YIPs should be written in [markdown](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet) format. There is a [template](https://github.com/why-labs/YIPs/blob/master/yip-template.md) to follow.

## YIP Header Preamble

Each YIP must begin with an [RFC 822](https://www.ietf.org/rfc/rfc822.txt) style header preamble, preceded and followed by three hyphens (`---`). This header is also termed ["front matter" by Jekyll](https://jekyllrb.com/docs/front-matter/). The headers must appear in the following order.

`yip`: *YIP number*

`title`: *The YIP title is a few words, not a complete sentence*

`description`: *Description is one full (short) sentence*

`author`: *The list of the author's or authors' name(s) and/or username(s), or name(s) and email(s). Details are below.*

`discussions-to`: *The url pointing to the official discussion thread*

`status`: *Draft, Review, Last Call, Final, Stagnant, Withdrawn, Living*

`last-call-deadline`: *The date last call period ends on* (Optional field, only needed when status is `Last Call`)

`type`: *One of `Standards Track`, `Meta`, or `Informational`*

`category`: *One of `Product`, `Community`, or * (Optional field, only needed for `Standards Track` YIPs)

`created`: *Date the YIP was created on*

`requires`: *YIP number(s)* (Optional field)

`withdrawal-reason`: *A sentence explaining why the YIP was withdrawn.* (Optional field, only needed when status is `Withdrawn`)

Headers that permit lists must separate elements with commas.

Headers requiring dates will always do so in the format of ISO 8601 (yyyy-mm-dd).

### `author` header

The `author` header lists the names, email addresses or usernames of the authors/owners of the YIP. Those who prefer anonymity may use a username only, or a first name and a username. The format of the `author` header value must be:

> Random J. User &lt;address@dom.ain&gt;

or

> Random J. User (@username)

or

> Random J. User (@username) &lt;address@dom.ain&gt;

if the email address and/or GitHub username is included, and

> Random J. User

if neither the email address nor the GitHub username are given.

At least one author must use a GitHub username, in order to get notified on change requests and have the capability to approve or reject them.

### `discussions-to` header

While an YIP is a draft, a `discussions-to` header will indicate the URL where the YIP is being discussed.

The preferred discussion URL is a topic on [Y on Dimension Y](https://dimensiony.io/). The URL cannot point to Github pull requests, any URL which is ephemeral, and any URL which can get locked over time (i.e. Reddit topics).

### `type` header

The `type` header specifies the type of YIP: Standards Track, Meta, or Informational. If the track is Standards please include the subcategory (core, networking, interface, or ERC).

### `category` header

The `category` header specifies the YIP's category. This is required for standards-track YIPs only.

### `created` header

The `created` header records the date that the YIP was assigned a number. Both headers should be in yyyy-mm-dd format, e.g. 2001-08-14.

### `requires` header

YIPs may have a `requires` header, indicating the YIP numbers that this YIP depends on. If such a dependency exists, this field is required.

A `requires` dependency is created when the current YIP cannot be understood or implemented without a concept or technical element from another YIP. Merely mentioning another YIP does not necessarily create such a dependency.

## Linking to External Resources

Other than the specific exceptions listed below, links to external resources **SHOULD NOT** be included. External resources may disappear, move, or change unexpectedly.

The process governing permitted external resources is described in [YIP-5757](./yip-5757.md).

## Linking to other YIPs

References to other YIPs should follow the format `YIP-N` where `N` is the YIP number you are referring to.  Each YIP that is referenced in an YIP **MUST** be accompanied by a relative markdown link the first time it is referenced, and **MAY** be accompanied by a link on subsequent references.  The link **MUST** always be done via relative paths so that the links work in this GitHub repository, forks of this repository, the main YIPs site, mirrors of the main YIP site, etc.  For example, you would link to this YIP as `./yip-1.md`.

## Auxiliary Files

Images, diagrams and auxiliary files should be included in a subdirectory of the `assets` folder for that YIP as follows: `assets/yip-N` (where **N** is to be replaced with the YIP number). When linking to an image in the YIP, use relative links such as `../assets/yip-1/image.png`.

## Transferring YIP Ownership

It occasionally becomes necessary to transfer ownership of YIPs to a new champion. In general, we'd like to retain the original author as a co-author of the transferred YIP, but that's really up to the original author. A good reason to transfer ownership is because the original author no longer has the time or interest in updating it or following through with the YIP process, or has fallen off the face of the 'net (i.e. is unreachable or isn't responding to email). A bad reason to transfer ownership is because you don't agree with the direction of the YIP. We try to build consensus around an YIP, but if that's not possible, you can always submit a competing YIP.

If you are interested in assuming ownership of an YIP, send a message asking to take over, addressed to both the original author and the YIP editor. If the original author doesn't respond to the email in a timely manner, the YIP editor will make a unilateral decision (it's not like such decisions can't be reversed :)).

## YIP Editors

The current YIP editors are

- AdeThorMiwa (@AdeThorMiwa)

## YIP Editor Responsibilities

For each new YIP that comes in, an editor does the following:

- Read the YIP to check if it is ready: sound and complete. The ideas must make technical sense, even if they don't seem likely to get to final status.
- The title should accurately describe the content.
- Check the YIP for language (spelling, grammar, sentence structure, etc.), markup (GitHub flavored Markdown), code style

If the YIP isn't ready, the editor will send it back to the author for revision, with specific instructions.

Once the YIP is ready for the repository, the YIP editor will:

- Assign an YIP number (generally incremental; editors can reassign if number sniping is suspected)
- Merge the corresponding [pull request](https://github.com/why-labs/YIPs/pulls)
- Send a message back to the YIP author with the next step.

Many YIPs are written and maintained by contributors with write access to the Y Labs codebase. The YIP editors monitor YIP changes, and correct any structure, grammar, spelling, or markup mistakes we see.

The editors don't pass judgment on YIPs. We merely do the administrative & editorial part.

## Style Guide

### Titles

The `title` field in the preamble:

- Should not include the word "standard" or any variation thereof; and
- Should not include the YIP's number.

### Descriptions

The `description` field in the preamble:

- Should not include the word "standard" or any variation thereof; and
- Should not include the YIP's number.

### YIP numbers

When referring to a YIP, it must be written in the hyphenated form `YIP-X` where `X` is that YIP's assigned number.

### RFC 2119 and RFC 8174

YIPs are encouraged to follow [RFC 2119](https://www.ietf.org/rfc/rfc2119.html) and [RFC 8174](https://www.ietf.org/rfc/rfc8174.html) for terminology and to insert the following at the beginning of the Specification section:

> The key words "MUST", "MUST NOT", "REQUIRED", "SHALL", "SHALL NOT", "SHOULD", "SHOULD NOT", "RECOMMENDED", "NOT RECOMMENDED", "MAY", and "OPTIONAL" in this document are to be interpreted as described in RFC 2119 and RFC 8174.

## History

This document was derived heavily from [Ethereum's EIP-1](https://github.com/ethereum/EIPs/blob/master/EIPS/eip-1.md) written by Martin Becze et al which in turn was derived from [Bitcoin's BIP-0001](https://github.com/bitcoin/bips) written by Amir Taaki which also derived from [Python's PEP-0001](https://peps.python.org/). In many places text was simply copied and modified. Although the Ethereum's EIP-1 text was written by Martin Becze, Hudson Jameson et al, they are not responsible for its use in the Y Improvement Process, and should not be bothered with technical questions specific to Y or the YIP. Please direct all comments to the YIP editors.

## Copyright

Copyright and related rights waived via [CC0](../LICENSE.md).