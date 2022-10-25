# Improving the Dapr proposal process

* Author(s): John Ewart (@johnewart), Mukundan Sundararajan (@mukundansundar)
* State: Draft
* Updated: 10/25/2022

## Overview

This proposal is to formalize the structure and lifecycle to proposals with three primary goals: first, make it easier for contributors to both put forth proposals as well as review them, second, increase the clarity and focus of proposals themselves, and, third, provide guidance on what is expected for a well defined feature to be "dev complete". In order to do this, we should:

1. Create a template for new proposals.
2. Define the core requirements for a feature that is being proposed to be considered complete.
3. Implement a process for reviewing and accepting new proposals.

## Background

### Why define a proposal process and templatize it?
 
As a community project, Dapr relies on contributors to help advance the project the goal of this proposal is to simplify the process of contributing, and evaluating, new ideas. We want to make it more inviting for community members to propose new ideas (or evaluate them) as well as ensure that the time being spent evaluating proposals or working on new features is well spent.

Adding clarity to the proposal process, as well as some amount of structure, will hopefully make it easier for contributors of all experience levels to both contribute and review new ideas. As a new contributor it can sometimes feel a bit daunting to propose a new idea -- not knowing quite where to start, whether or not what you are proposing has the right level of information, etc. Having structure makes it easier for a new contributor who wants to propose a new idea to know what is expected and feel confident that their proposal meets those expectations. In addition, for anyone putting forward a proposal, the structure proposed prompts thinking about how someone else would use the feature, how they might benefit from it, and what other ways the feature they are proposing might be solved using existing features (or other technology).  

On the other side of the equation are the community members who are reviewing those proposals; it can be challenging to review something if you feel that information or context is lacking. A consistent structure means that reviewers can know what to expect out of a proposal document and clearly ask for more information if some is missing. And, the suggested structure would make sure that reviewers have the right information needed to have a conversation about the proposal (as well as reduce the scope of the review). 

As a community, we want to be welcoming of new people and also respectful of the time and energy that everyone devotes to make this project great. I believe that adding this small amount of structure to the proposal process will help not only make it easier to propose new ideas, but also ensure that everyone who is participating can make the best use of the time they have available to improve Dapr!

### Why define minimum requirements for a feature to be complete?

As Dapr increases in scope and brinds on more contributions, it is important that we define what we expect before a new feature is added to Dapr. In order to assure that all aspects of the feature have been completed for release we need to provide clear guidance on what needs to be accomplished before it is accepted into Dapr. This will help us to qualify these features as complete for a particular release milestone and be confident in what is being released. For example, most features would require, at a minumum:

* Completion of the code
* Maintainer signoff on the implementation by the feature freeze date
* Code merged into the main branch well before the code freeze date (feature freeze date at the latest) 
* During the time between feature freeze and code freeze, any P0 regressions/bugs related to this feature that are identified need to be fixed.
* Adding / updating performance tests, e2e tests etc.
* Documentation for the new feature has been committed to `dapr/docs` 
* Creating / updating quick starts, tutorials (if relevant)

In addition, some features would require changes to SDKs or have additional requirements in order for it to be considered fully complete, and so those requirements should also be tracked in order to ensure completion.


## Background vs Design

> "Your scientists were so preoccupied with whether they could, they didn’t stop to think if they should." - Dr. Ian Malcolm (Jurassic Park)

The goal of a proposal is to focus on two primary areas: 

* **Context:** _What_ the proposal is putting forth, and _why_ the proposal is required (what will it do for users?)
* **Analysis / Design:** _How_ the proposal will be implemented and any background analysis of the feature

### Context

The first goal of a proposal is to help reviewers understand the background for the proposal; it includes a summary of the proposed feature or change as well as explanation for why it is being proposed to the community. It is intended to inform the reviewers what this proposal introduces, at a high level, and why it is valuable so that they have the appropriate context when evaluating the proposal. 

In order to be effective, a proposal must provide not only a description of the idea itself (what it is and how it works) but also _why it should be introduced to Dapr_. The _why_ part of this proposal is just as important (if not more so) than what is being proposed, as it lets the reviewers understand better what kinds of use cases that the feature shall enable, how it will make Dapr better technically or improve the experience of Dapr users. By going through and clarifying _why_ something should be added to Dapr it helps the community to understand how this proposal would impact users as well as the benefits and potential drawbacks that it might bring. This, in turn, helps the community to better evaluate the proposal and weight the cost/benefits of the proposed changes. 

### Analysis / Design

The second half of the process focuses on the implementation of the proposal - the goal of this part is to show the community not only how it will operate, but also provide information on how success shall be measured and also include a list of activities that must be completed in order for this proposal to be complete, what the expected lifecycle / impact of this changes is on users or Dapr, and so on. 

This section of the proposal is where the authors can convey not just how a feature will work technically, but also identify what is in scope and what is out of scope (i.e what things have been deliberately omitted vs. what will be addressed as part of this proposal) along with any alternatives that have been considered and why they were not a good fit. 

## Proposed templates for Design and Build Phases

See the following file: [templates/proposal.md](templates/proposal.md) 

## Related Items

### Related proposals 

N/A

### Related issues 

N/A

## Expectations and alternatives

### What is in scope for this proposal?

This proposal covers the process for creating, storing, and reviewing proposals. The intention is to improve the process and increase clarity around proposals, their status, and their design. 

### What is deliberately *not* in scope?

The planning process for including proposals in a given release is not a part of this proposal, the assumption is that process will continue to operate as it currently does. 

### What advantages / disadvantages does this proposal have? 

This proposal has the advantage of increasing clarity of proposals as well as implicitly creating a record of design decisions; however, it is a little more involved and structured than the previous process, which may be viewed as a disadvantage. The authors of this proposal believe that the advantages significantly outweigh any potential disadvantages, however. 

### Related work

There is no need to reinvent the wheel and it is important to give credit where it is due; this proposal has taken some inspiration from the gRPC RFC process (also called "gRFC"), specifically around the naming of proposal files as well as some of the terminology and structure of the proposal template -- see [the gRPC proposal repository](github.com/grpc/proposal) for their process. 

## Implementation Details

### Completion Checklist

- [ ] A new repository (`dapr/proposals`) is created as a copy of this repository
- [ ] Any relevant documentation around submitting proposals or the development process point to this new repository and process
- [ ] Migration of existing _in-flight_ proposals from GitHub issues to this repository
- [ ] _(Optional)_ Migration of previous proposals to this repository
