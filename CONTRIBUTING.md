# Contributing to GrimoireLab Toolkit

These are some general guidelines and information related to how we 
contribute to GrimoireLab.

GrimoireLab is a part of the [Software Technical Committee](https://wiki.linuxfoundation.org/chaoss/software) 
of the [CHAOSS Collaborative Project](http://chaoss.community).

## Communication means

GrimoireLab  use the following communication channels:

* Mailing list
* IRC channel
* Issues / Pull Requests

Each of them is intended for an specific purpose. Please understand
that you may be redirected to some other mean if the communication you
intend to have is considered to fit better elsewhere.

### Mailing list

List:
[grimoirelab-discussions@lists.linuxfoundation.org](https://lists.linuxfoundation.org/mailman/listinfo/grimoirelab-discussions)

We use the list for:

* Discussions related to the management of the project, including the
relationship with the CHAOS Software Technical Committee.
* General announcements, including information about releases.
* General discussions about the future of the project, relationship
with other projects, new features or refactorings that really don't fit
in other communication means.
* Questions and community support that really don't fit in other
communication means.

### IRC channel

Channel: `#grimoirelab` at [Freenode](http://freenode.net/)

We use the channel for pinging people, quick and informal
discussions, questions and answers, etc. Please, don't consider that
developers in the channel will be always available, or always willing
to answer questions and comments. However, anyone interested in the
project is welcome to join the channel and hang around.

### Issues / Pull Requests

Repositories: [GrimoireLab repositories in GitHub](https://github.com/chaoss/grimoirelab#grimoirelab-components), 
which are all in the [CHAOSS organization](http://github.com/chaoss).

Most of the work is discussed here, including upgrades and
proposals for upgrades, bug fixing and feature requests. For any of
these, open an issue in the corresponding repository. If in doubt, ask in
the IRC channel, or try in any one: if needed you will be redirected to
the right repository. If you are proposing code change, open a pull request.

## Accepting contributions

Except for a few exceptions, **all contributions to current repositories
in GrimoireLab will be received as pull requests in the corresponding
repository**. They will be reviewed by at least one committer before
being accepted. Anyone is welcome to comment on pull requests.

Except in very special circumstances, that should be defined,
contributions will be accepted under the GPLv3 (GNU Public License
version 3).

The list of current repositories is the list of 
[GrimoireLab projects](https://github.com/chaoss/grimoirelab#grimoirelab-components) 
in the [CHAOSS organization](http://github.com/chaoss) in GitHub.

## DCO and Sign-Off for contributions

The [CHAOSS Charter](https://github.com/chaoss/governance/blob/master/project-charter.md) 
requires that contributions are accompanied by a 
[Developer Certificate of Origin](http://developercertificate.org) sign-off.
For ensuring it, a bot checks all incoming commits.

For users of the git command line interface, a sign-off is accomplished 
with the `-s` as part of the commit command: 

```
git commit -s -m 'This is a commit message'
```

For users of the GitHub interface (using the "edit" button on any file, 
and producing a commit from it), a sign-off is accomplished by writing

```
Signed-off-by: Your Name <YourName@example.org>
```

in a single line, into the commit comment field. This can be automated 
by using a browser plugin like [DCO GitHub UI](https://github.com/scottrigby/dco-gh-ui).

#### Guidelines to follow to write good commit messages

Writing a well-crafted Git commit message is the best way to
communicate context about a change to fellow developers.

Seven rules of a great Git commit message are mentioned in 
[How to Write a Git Commit Message](https://chris.beams.io/posts/git-commit/):

1. Separate subject from body with a blank line
2. Limit the subject line to 50 characters
3. Capitalize the subject line and (optionally) 
start the subject with a tag
4. Do not end the subject line with a period
5. Use the imperative mood in the subject line
6. Wrap the body at 72 characters
7. Use the body to explain what and why vs. how

The below git commit message is a good example which follows
the above rules.

```
Summarize changes in around 50 characters or less

More detailed explanatory text, if necessary. Wrap it to about 72
characters or so. In some contexts, the first line is treated as the
subject of the commit and the rest of the text as the body. The
blank line separating the summary from the body is critical (unless
you omit the body entirely); various tools like `log`, `shortlog`
and `rebase` can get confused if you run the two together.

Explain the problem that this commit is solving. Focus on why you
are making this change as opposed to how (the code explains that).
Are there side effects or other unintuitive consequences of this
change? Here's the place to explain them.

Further paragraphs come after blank lines.

 - Bullet points are okay, too

 - Typically a hyphen or asterisk is used for the bullet, preceded
   by a single space, with blank lines in between, but conventions
   vary here

If you use an issue tracker, put references to them at the bottom,
like this:

Resolves: #123
See also: #456, #789
```

## Pull Request Etiquette

### Why do we use a Pull Request workflow?

PRs are a great way of sharing information, and can help us be 
aware of the changes that are occuring in our codebase. 
They are also an excellent way of getting peer review on the work 
that we do, without the cost of working in direct pairs.

**Ultimately though, the primary reason we use PRs is to encourage quality 
in the commits that are made to our code repositories**

Done well, the commits (and their attached messages) contained within tell 
a story to people examining the code at a later date. If we are not careful to 
ensure the quality of these commits, we silently lose this ability.

**Poor quality code can be refactored. A terrible commit lasts forever.**

### What constitutes a good PR?

A good quality PR will have the following characteristics:

* It will be a complete piece of work that adds value in some way.
* It will have a title that reflects the work within, and a summary that 
helps to understand the context of the change.
* There will be well written commit messages, with well crafted commits that 
tell the story of the development of this work.
* Ideally it will be small and easy to understand. Single commit PRs are 
usually easy to submit, review, and merge.
* The code contained within will meet the best practises set by the team 
wherever possible.

A PR does not end at submission though. A code change is not made 
until it is merged and used in production.

A good PR should be able to flow through a peer review system easily and quickly.

Github's recommendations for PRs, which has some useful tips on 
notifying teams and collegues via the github @-syntax, 
[How to write the perfect pull request - The GitHub Blog](https://github.blog/2015-01-21-how-to-write-the-perfect-pull-request/)

## Submitting Pull Requests

### Ensure there is a solid title and summary

PRs are a GitHub workflow tool, so it's important to understand 
that the PR title, summary and eventual discussion are not as 
trackable as the the commit history. If we ever move away from 
Github, we'll likely lose this infomation.

That said however, they are a very useful aid in ensuring that 
PRs are handled quickly and effectively.

Ensure that your PR title is scannable. People will read through 
the list of PRs attached to a repo, and must be able to distinguish 
between them based on title. Include a story/issue reference 
if possible, so the reviewer can get any extra context. Include a 
reference to the subsystem affected, if this is a large codebase.

Use keywords in the title to help people understand your intention with 
the PR, eg [WIP] to indicate that it's still in progress, so should not be merged.

### Rebase before you make the PR, if needed

Unless there is a good reason not to rebase - typically because more 
than one person has been working on the branch - it is often a 
good idea to rebase your branch to tidy up before submitting the PR. 

Use `git rebase -i master # or other reference, eg HEAD~5`

For example:

* Merge 'oops, fix typo/bug' into their parent commit. There is no 
reason to create and solve bugs within a PR, **unless there is 
educational value in highlighting them**.
* Reword your commit messages for clarity. Once a PR is submitted, 
any rewording of commits will involve a rebase, which can then mess 
up the conversation in the PR.

### Aim for one succinct commit

In an ideal world, your PR will be one small(ish) commit, doing 
one thing - in which case your life will be made easier, since 
the commit message and PR title/summary are equivalent.

If your change contains more work than can be sensibly covered in a 
single commit though, **do not** try to squash it down into one. 
Commit history should tell a story, and if that story is long then 
it may require multiple commits to walk the reviewer through it.

### Describe your changes well in each commit

Commit messages are invaluable to someone reading the history of the 
code base, and are critical for understanding why a change was made.

Try to ensure that there is enough information in there for a person 
with no context or understanding of the code to make sense of the change.

Where external information references are available - such as Issue/Story IDs, 
PR numbers - ensure that they are included in the commit message.

Remember that your commit message must survive the ravages of time. 
Try to link to something that will be preserved equally well -- 
another commit for example, rather than linking to master.

** Each commit message should include the reason why this commit was made. 
Usually by adding a sentence completing the form 'So that we...' will give 
an amazing amount of context to the history that the code change itself cannot **

### Keep it small

Try to only fix one issue or add one feature within the pull request. The larger 
it is, the more complex it is to review and the more likely it will be delayed. 
Remember that reviewing PRs is taking time from someone else's day.

If you must submit a large PR, try to at least make someone else aware 
of this fact, and arrange for their time to review and get the PR merged. 
It's not fair to the team to dump large pieces of work on their laps without warning.

If you can rebase up a large PR into multiple smaller PRs, then do so.

## Reviewing Pull Requests

It's a reviewers responsibility to ensure:

* Commit history is excellent
* Good changes are propagated quickly
* Code review is performed
* They understand what is being changed, from the perspective of 
someone examining the code in the future.

## Committers

Committers have the permision to merge code in GrimoireLab. Committers
can be for all GrimoireLab, or for specific repositories.

New committers will be proposed by committers, and accepted (granted
committer rights) by an action vote among committers (see below).
Developers can apporach committers to ask to be proposed as comitter.
Main rule for acceptance of new committers will be their merits on the
project, including past contributions and expertise.

Committers may resign if they are no longer involved enough in the
project. Committers can also propose the removal of other committer
rights, in case they are no longer involved in the project. For being
removed, after the proposal there will be an action voting among
committers, except for the one being proposed to be removed.

The current list of committers is (GitHub handles):

* General: @sduenas, @acs, @dicortazar, @sanacl, @jgbarah, @jsmanrique, @valcos
* Manuscripts: @alpgarcia
* Sigils: @alpgarcia

## Voting on action items (action votes)

Action items will be decided by public votes in the mailing list for
the project. Anyone in the mailing list can vote, to express their
opinion, but the result of the vote will have into account only the
votes by general committers.

Votes will be casted as (details taken in part from the Apache
project):

-  +1: Yes, agree, or the action should be performed.
-    0 : Abstain, no opinion, or I am happy to let the other group members
decide this issue.
- -1: No, I veto this action. All vetos must include an explanation of
why the veto is appropriate. A veto with no explanation is void.

A period of four days, since the moment the action item is proposed,
will be valid for casting votes. Any comitter can propose an action
vote, which will be effective if at least two other committers agree
during a period of two days. The voting period will start when the
proposer sends a message stating that, after the second agreement is
received.

Action votes will be mandatory for:

* Accepting a new committer.
* Proposal for removal of committer rights.
* Accepting a new repository in the project.
* Removing a repository from the project.
* Deciding that some certain code in some repository needs to be moved
to some other repository.

In all the cases, the action vote will pass with at least 3 positive
votes and no vetos.

## Incubating repositories

In some cases, activity related to GrimoireLab may start in
repositories outside the GrimoireLab project. In that case, if the
developers collaborating in those repositories want, they can inform
GrimoireLab of their progress, and propose coordianted actions (such as
definition of APIs). However, they will be considered external projects
until the moment they are accepted as repositories in GrimoireLab, via
an action vote.

## Releases

GrimoireLab will deliver frequent coordinated releases of several of
the code in its repositories. These releases are generated by using 
[Bitergia/release-tools](https://github.com/Bitergia/release-tools).

### Changelog Entries

The contributors need to create note entries about the changes in the code. 
These notes will be included in the release notes. The contributors can use the 
interactive [changelog](https://github.com/Bitergia/release-tools#changelog) 
tool for this purpose. 

Changelog entries use [YAML format](https://yaml.org/). Remember you can write blocks 
of text using `>` character at the beginning of each block. See the next example:
```
title: 'Fix bug #666'
category: fixed
author: John Smith <jsmith@example.com>
issue: 666
notes: >
  The bug was making impossible to cast a spell on
  a magician.
```

These changelog entries would be included in the release notes which is read by 
users who might not know anything about the internals of the code. The `notes` 
should be written in simple language that is understandable by the audience.
