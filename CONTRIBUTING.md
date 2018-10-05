# Contributing to education

Thanks for taking your time to contribute to this project. 

The following is a set of guidelines for contributing to `education`. These are mostly guidelines, not rules. Use your best judgment, and feel free to propose changes to this document in a pull request.

##### Table of Contents

* [**What should I know before I get started?**](#what-should-i-know-before-i-get-started)
* [**Pull Request Process**](#pull-request-process)
* [**How Can I Contribute?**](#how-can-i-contribute)

## What should I know before I get started?

This repository is mainly the thoughtworks of the individual that owns this repository: [`@jesperorb`](https://github.com/jesperorb) and should not be treated as an official guide where _everything_ will be collected. The goal is to have _short_ sections for every part and just the _bare necessary_ parts. This means that the owner/owners of this repository, as it is now, will have final say on what's get added. **But don't get discouraged, the owner of this repository plans to collect all the contributions that didn't make the cut in an _appendix_. So contributions are very much welcomed, even if they don't make the cut they will still be saved.**

## Pull Request process

1. Fork this repository.
2. Create a new branch with your changes.
3. Push branch to your own fork.
4. Create pull request from your own fork into `master` of base repo.

## How can I contribute?

### Adding examples

Each point/section/statement made in this repository should have an example bound to that statement. For example: if you make the statement that all students should comment their code, you must also supply an example of how and when the student should comment.

_example:_

* You should primarily comment on the purpose of the code instead of what it does. The problem is seldom that we don't understand the code, it is more often that we don't understand the intention and use case.

```php
/* Sometimes when editing a post the title gets set to empty string.
 * This is a way to handle that scenario. We need to check what is 
 * causing the title to get set to empty but until then this code is
 * required
 */
if(check_empty($_GET["title"])){
   // handle error
}
```

### Adding resources

You can add additional resources that either will help with the pedagogical process or tools that will help to deliver content. For example if you have additional presentation tools or tools for structuring course content. It can also be more methodical resources that explains parts of the learning process.

The resources should primarily be the form of links to these additional resources with a brief explanation of what it is.

example:
```
* [Reveal.js](https://revealjs.com)
    - HTML-based presentation tool. Can be made to handle `.md`-files as well.
```

### Suggesting enhancements

You can also suggest enhancements to already exisiting examples or resources.

### Fix spelling

This repository needs some spellchecking. It can either be just correcting misspelled words. It can also be to suggest better wording of sentences.

### Styleguide

* // TODO

#### Git Commit Message

* // TODO