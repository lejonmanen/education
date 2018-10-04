# Education for technical subjects

This repository is a collection of _"things that work"_, pedagogy 101 and some things that are obvious but just easy to forget when your in the middle of it. It includes everything from how to structure your lessons to actual practical tools to simplify and effectively create content for your students. This is **not a best practice or a silver bullet**, it's just based on first hand experience and may well be very wrong on some parts and I do not always follow these guidelines myself because I am mortal.

**Feedback and contributes are always welcome**

## Continuity

Everything can be reused and further built upon. Resuse everything you can and try to build on existing code. An example of how I structure one of my courses in HTML/CSS/JS, the days/number of days doesn't matter, it's more about the order. By always reusing previous code we can quicker get up to speed with the goal of the day instead of reinventing the wheel all the time.

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


## Explanations

* **Always have two explanations**: one correct but technical and one semi-correct that is primary non-technical.

![We get it!](images/poets.png)

* **Analogy**
    * _"An analogy is a cognitive process of transferring information or meaning from a particular subject (the analog, or source) to another (the target), or a linguistic expression corresponding to such a process."_ - Wikipedia
    * _"I know what an analogy is. It's like a thought with another thought's hat on."_ - Britta Perry, Community S03E11

## Student submissions

**Always** supply a strict format, name and structure for submitting an assignment. For example you can use the following:


* **File format**: everything must be supplied as a `.zip`. `.zip` isn't the most compact format but it will work on any modern computer without installing an extra utility. If you are working with external modules in the project (npm for example) be sure the student removes these from the project before submitting to decrease file size.
* **Naming of files**: **both** foldername and filename must follow the same naming standard. For example: `firstname_lastname_assignmentname.zip`. Otherwise you will have 5 `my assignment 2`-folders and you have no idea who actually sent in the assignment. This step is mainly for you to avoid cognitive load and headache both for you and your students, but mainly for you.
* **Credentials**: if the submission has some sort of login or database-credentials this must be supplied somehow, preferably the student has a README in the submission with these credentails. If the assignment uses a database like SQL, an exported `.sql`-file should be supplied as well.
* **README**: Every submission should have a README with at least the students name in it.

Some alternative methods of submission are:

* **Repository link**: students send you a link to a repository, or invite you to collaborate on it
* **Online code snippet**: students send you a link to a code snippet using an online service. Examples include [CodePen](https://codepen.io/), [repl.it](https://repl.it/languages/) and [JS Bin](https://jsbin.com/?html,css,js,output)
* **repl.it automated submissions**: create assignments complete with unit tests, to give students instant feedback on whether they pass. [Teacher area on repl.it](https://repl.it/teacher)


## Structure

### Day to day
> A single day in higher education is usually **6 hours**. Depending on the subject the steps below can be repeated 2-4 times a day (excluding step 1). This means that you can have one or two big presentations followed by exercises and feedback or you could have many short presentations and shorter exercises. The exercises should be in focus. Remember to take frequent breaks: up to 45 minutes of _presentation_ and 15 minutes _break_ is a good rule of thumb.

1. **Clarify the content of the day**: what we will learn and why is it important to learn based on **practical day to day usage**. Don't start of by explaining the theoretical parts of `Big O Notation`, start of by saying: _"Every loop or sort impacts performance making your application slower which makes your users impatient which results in loss of customers and money. Big O helps you understand that impact."_
    * _"We will learn the basics of how a function works, well defined functions helps you debug, scale functionality and find problems faster."_
2. **Supershort slides about the subject**: The basics can be read in the documentation of the tool/language or _any_ tutorial on the internet so keep that part really short. Your slides should be about _gotchas_, _best practices_, _pitfalls_ and _the why_. Some of these things can be brought up at the end of the day instead when the students have some experience with the problems. **More teorethical parts can be left as _Further reading_-links in the course material.**
3. **CODE DEMO: Jump into code as quick as possible**. Comments in code can be used as _"slides"_. Show at least two areas of application, preferably real world usage. `class Cat extends Animal` is fine if your real world classes are too complex but "regular examples" usually makes the code too abstract. It is always a good idea to step through code with a debugger if possible.
4. **EXERCISES**: most important part, a lot of exercises with varying level of difficulty. Spend more time on the exercises than the time spent on presentations.
5. **Solutions/feedback**: **Ask if some students want to show their solutions. It doesn't have to be finished solutions. You can use a students code and solve it live with the help of the class. As long as some key concepts and gotchas are brought up. Create an environment were showing your code is encouraged**. If no volunteers, walk through some solutions yourself to some of the exercises that you found that the students had the hardest time to grasp. Use a debugger to step through the code here.
6. Move on to next deeper area of subject or a different subject. Repeat step 2-5 until end of day. At end of day, summarize the content of the day.

### Course

// TODO

## Exercises

Each block of exercises should have the following structure if possible:

* **1-2** exercise that everyone can manage to solve. This exercise should be close to the example/examples done during _demo time_: _"Print 10 numbers with a loop"_
* **1-2** exercise that builds upon the knowledge obtained by the previous exercise but a bit harder: _"Sum all the previous 10 numbers and then print the summed value."_
* **1-∞** exercises that can either build upon the previous exercises or be something completely new as long as it exercises the current objective: _"Go through a list of words and only print those words that are longer than 5 chars"_. It can be a good idea to supply hints: _"There is a built in function to count the length of a string, search for it."_

## Projects

// Todo

// Individual, pairs, groups of three and above

// Usually a good idea to use agile methods with larger projects


## Exams

**An exam must do two things**:
    1. _Test the students current knowledge, primarly fact based questions._
    2. _Let the student apply their current knowledge to learn new things about the subject._

**Example**: During the course or during a presentation you could provide the student with only the pros of a tool/language/framework, presenting why it's a good thing for the student to learn it. On the exam on the other hand, you could ask the question: _"What are the cons of using tool/language/framework?"_. 

If the student can answer the question the student will have deducted the answer and learn't something new. If the student failed to answer the question the student should now know what to research/study for the future. 

### Written exams

* This is not my area of expertise :grimacing:

### Home exams

* This is not my area of expertise :grimacing:

### Quizes

* This will be expanded upon. 
* If you are doing quizes on a page that has a WYSIWYG-editor you can use a tool such as [**http://hilite.me/**](http://hilite.me/) to provide the student with code with syntax highlighting. This will make it easier to read the source code and makes it easier to focus on actually solving the question.
 
## Tools

### Course outline and material

Every course should have a [GitHub](https://github.com/)-repository. It doesn't need to be GitHub, you can also use GitLab, BitBucket or similar. Everything that is not sensitive information should be in this repository. This approach is prefered because:


* Get students familiarized with hosting services for version control. Learn how to navigate a project.
* Accessable anywhere, no login required (if you are using public repos, you can get free private repos for education purpose if you want to hide some material) and students can easily link and share details.
* Easier for **you** to update the course material. If you use markdown-based material, updating this material is fast and fairly easy as it is just a commit of updated text. If you use markdown-based presentations as well (linked in a later section below) it's easy to update mistakes in the presentations aswell, instead of reuploading a new `.pdf` or `.pptx`. Just make sure to ask the students to reload the page after your updates (people seldom reload pages)
* Repository can easily be cloned or copied

Alternatives to a GitHub repository include

* Google Doc with links to resources - easiest to update
* Wiki - superior ability to do text search on files


#### Structure of course on GitHub

The course can have the following outline. You can further divide the readme if it gets too long.

* :page_with_curl: `README.md`
    - _Overview of course, small intro_
    - _Course literature_
    - _Course links_
    - _Schedule_
* :open_file_folder: `exercises`
    - Folder with all exercises
    - May be a good idea to label them with numbers according to when they appear: `01_intro.md`, `02_variables.md` etc.
* :open_file_folder: `slides`
    - Your `.pdf`, `.pptx` or `.md`-slides here
* :open_file_folder: `democode`
    - Everything that is done during demo code-time should be put in this folder
* :open_file_folder: `examinations`
    - Every mandatory assignment in here
* :page_with_curl: `issue_template.md`
    - If you use issues you may want a template for submitting an issue, your students can open issues if they have a problem or found an error in the course material


### Presentation

Prefer text-based presentation tools that can easily be converted between different formats.

* [Deckset](https://www.deckset.com/)
    - Only for _Mac_. Turns `.md`-files into presentations. Easier to change, write and commit. Can be exported as `.pdf` for example.
* [Reveal.js](https://revealjs.com/#/)
    - HTML-based presentation tool. Can be made to handle `.md`-files as well.
* [MDX-Deck](https://jxnblk.com/mdx-deck/#0)
    - React-based presentation tool that uses `.mdx`-files for content (an extension of `.md`)
* [Slides.com](https://slides.com/)
    - HTML-based presentation tool, online tool based on reveal.js
* [hackmd](https://hackmd.io/)
    - Collaborative markdown-notes with built in presentation mode

Google Slides allows for shared documents that are very similar to PowerPoint.
