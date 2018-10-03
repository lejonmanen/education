# Education

This repository is a standard for creating a Quality Insured And Great EducationTM. It includes everything from how to structure your lessons to actual practical tools to simplify and effectively create content for your students. This is **not a best practice or a silver bullet**, it's just based on first hand experience and may well be very wrong on some parts.

## Continuity

Everything can be reused and further built upon. Resuse everything you can and try to build on existing code. An example of how I structure (approximately) one of my courses in HTML/CSS/JS, the days/number of days doesn't matter, it's more about the order. By always reusing previous code we can quicker get up to speed with the goal of the day instead of reinventing the wheel all the time.

* Day 1: _"Today we will recreate a common web-component in HTML structure_:
```html
<div>
    <p>The Avengers: Infinity War</p>
    <p><strong>Rating: 8.9</strong></p>
    <p><em>Genres: Action, Comedy</em></p>
</div>
```
* Day 2: _"Today we will style this element as a standard card-component"_: `<div class="card"></div>`
* Day 3: _"Today we will place this card in a `flexbox`-grid/`float`-grid"_
* Day 4: _"Today we will use a single column layout on small screen and expand the cards to a multi-column grid on bigger screens"_
* Day 5~8: _"Today we will learn about control statements and loops in JavaScript so we can programmatically create this card multiple times in the DOM"_
* Day 9: _"Today we will replace the hardcoded values in the card with this array of objects that represent some data from a database"_
* Day 10: _"Today we will fetch data from IMDBs API and replace our previous array of objects with actual up to date data"_
* Day 11: _"Today we will save our favorite movies in the browser by using buttons and events"_
* Day far ahead in the future: _"Today we will fetch movies from an API and save our favorites both in the browser and our own database and connect it to our logged in user"_

## Structure

### Day to day
> A single day in higher education is usually **6 hours**. You can't talk for six hours and nobody wants you too. This puts high pressure on creating good exercises which is _way_ harder.

1. **Clarify the content of the day**, what we will learn and why is it important to learn based on **practical day to day usage**. Don't start of by explaining the theoretical parts of `Big O Notation`, start of by saying: _"Every loop or sort impacts performance making your application slower which makes your users impatient which results in loss of customers and money. Big O helps you understand that impact."_
    * _"We will learn the basics of how a function works, well defined functions helps you debug, scale functionality and find problems faster."_
    * _"Another quote"_
2. **Supershort slides about the subject**. The basics can be read in the documentation of the tool/language or _any_ tutorial on the internet so keep that part really short. Your slides should be about _gotchas_, _best practices_, _pitfalls_ and _the why_. Some of these things can be brought up at the end of the day instead when the students have some experience with the problems.
3. **CODE DEMO: Jump into code as quick as possible**. Comments in code can be used as _"slides"_. Show one or two examples, preferably real world usage. `class Cat extends Animal` is fine if your real world classes are too complex. 