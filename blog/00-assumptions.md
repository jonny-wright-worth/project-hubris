# Assumptions

Everyone has a context. You might just be starting out learning web development for fun; you might be a enterprise-architect, polyglot, 30+yrs experience engineer; or somewhere in between. Where you come from will affect what you choose to build and how you choose to build it.

My context is that I co-lead a team of ~20 engineers on multi-year projects. A lot of my choices are predicated on this. The choices that I make are not universally right, they may not even be 100% optimal for my exact situation, but these things do inform the way I progress. If getting 'just something' up and running is your goal then there will be a lot that is here that is completely overkill. If you exist in a mature corporate infrastructure where there are well trodden paths then a lot of this might be re-inventing the wheel. If you are somewhere in the middle, then hopefully this is an interesting journey to come on.

## Specifics

There are a few less common ideas that we embrace at KDSE. These also form a large part of my context. You may adopt these, you may not. Some of my choices may be more or less relevant depending on this.

### Mobbing

Our understanding is that the limit on feature output is not how fast you can type, but how fast you can think. And so we mob. This typically happens in groups of 3 - one person driving, one person navigating, one person either scouting or facilitating (see the [cucumber article](https://cucumber.io/blog/bdd/five-roles-in-a-healthy-mob/) for more details). With 3 people staring at a screen while something compiles, dev-experience (DX) is paramount. I have been in a mob where tests take 10 minutes over a whole run - this is half a person hour. Fast builds, fast tests, fast running is of specificially high priority to me.

### Trunk based development

> Merge conflicts are the worst thing ever
> _Quote attributed to literally everyone, everywhere_

Hyperbole aside, at KDSE we find that it is much better to make small, regular commits to the trunk instead of using branches. Disconnecting a development stream from trunk only causes pain. Instead we rely on [branching by abstraction](https://martinfowler.com/bliki/BranchByAbstraction.html). It is much better to bring some code back into the fold that quote 'has no business affect' than to leave it languishing out on a branch where it can become stale.

### TDD & 100% coverage

This is very much related to trunk based development (above). We have found that it is better to write tests for every single lines of code that you write, than to write it after the fact - if you write some code why are you writing it? There should be a test to ensure that you have written the correct code.
