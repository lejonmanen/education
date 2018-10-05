# Education for technical subjects

This repository is a collection of _"things that work"_, pedagogy 101 and some things that are obvious but just easy to forget when your in the middle of it. It includes everything from how to structure your lessons to actual practical tools to simplify and effectively create content for your students. This is **not a best practice or a silver bullet**, it's just based on first hand experience and may well be very wrong on some parts and I do not always follow these guidelines myself because I am mortal.

**Feedback and contributions are always welcome. If you want to know more on how you can contribute, visit [CONTRIBUTING.md](CONTRIBUTING.md)**

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

**Prefer projects over any other type of knowledge assessment because it is closer to real life**. Projects do make it harder to assess the knowledge. How to make it easier to assess the student during projects will be expanded upon in the future (contributions welcome).

### Individual

* Keep in mind that the class is likely to have widely varying degrees of skill. Make sure there is a _G version_ that covers the most basic course requirements, and a _VG version_ that provides a reasonable challenge for the top of the class.
* Good for assessing individual skill.
* Takes a lot more time to correct and grade, not always feasible for large classes.

### Pairs

* Students will naturally seek out classmates with similar skill. They will carry each other tend to get stuck less.
* Skill level between groups still likely to vary much.
* Group is small enough that students will not be able to "evade work" as easily.
* Pair programming can be used, which transfers skill and helps in lowering rate of bugs.
* Students will tend to pair up with the same person. This can be good or bad.

### Larger groups

Prefer working in larger groups, **size > 3**, depending on the length of the project. This is prefered because:

* Collaboration with Git, the students have to work with git conflicts and multiple branches.
* Not as heavy burden on the individual, get help from team members, diversity in problem solving.
* Students can take on different roles in the project.

However:

* Weaker students tend to choose simpler tasks and work less; stronger students will work more. Groups thus have a natural tendency to be "unfair" unless this is controlled.
* It's harder to ascertain that every group member has learned everything they need to pass the course. Consider having requirements like _"every group member should write at least one AJAX function"_.
* Some students will try to evade work. To combat this, make both the group as a whole and each member write a **Log Book**. The project log should contain any relevant information about the agile meetings the group is doing. The individual log should contain a short description of work done each day or week. They should also list any fulfilled individual requirements.

You need to choose whether to manually select students for each group or let them choose themselves. If the students decide, they will form groups based on who they already know and people of similar skill. This will lead to several strong groups, but risk getting a "disaster group" that is almost predetermied to fail.

On the other hand, if **you decide the groups**, you can either pick people of similar skill level or try to form mixed groups. If groups are too internally similar in skill, we get a disaster group. Mixing the weaker students among several groups shares the risk. Students will generally accept this if some form of check is made (log books) to prevent group members getting away with avoiding work.

Use **different groups on different projects** for several reasons. The students get to know others in their class better. They won't be able to choose their groups in work. They are thrown out of their comfort zone and get to practice group dynamics. They better learn how to work with others.

Teams can work agile, the amount of application of agile framework or method can vary. The minimum should be:

* **Daily standups**
* **Some kind of board to handle backlog**: [GitHub Project Boards](https://help.github.com/articles/about-project-boards/) or [Trello](https://trello.com/)


## Presentations

Project groups should have a presentation for the class as part of the examination. When doing a project over several weeks, consider having weekly presentations - _sprint review_ - to let the students practice presenting their work.

* Make sure the presentation shows as many of the requirements as possible, so you can "check the boxes" as they speak.
* Invite the school administration (utbildningsledare) to presentations. Double benefit: they get to see how the class is doing and students get to practicing explaining their work for non-technical people.
* Keep in mind that some students may be shy. As a general rule, we do not choose working with computers because we love public speaking. Some students may have real issues just standing in front of the class. Try to identify such students early and have an ongoing discussion with the school administration about how to handle their situation. These students are also more likely to have difficulities finding internship (LIA) on their own.
* How long the presentation should be. Set a time or an interval.

A presentation can contain these points:

* (first presentation) Show any prototypes you have. Talk about your vision for the project.
* Show the project board
* Talk briefly about what you have done since last presentation. What were your greatest obstacle and how did you solve it? This hopefully teaches other students that groups regularly run into problems, the important thing is learning how to solve or sidestep them.
* (all but last presentation) Talk briefly about what remains to be done. What do you expect to be the greatest challenges?
* Demonstration of the new parts
* (final presentation) Demonstrate the project from the perspective of a new user.
* (final presentation) Briefly evaluate your process. Are you satisfied with how you worked? Would you have planned it differently with what you know now?
* Allocate some time for questions from the audience and the teacher.
* Applause!

## Exams

**An exam must do two things**:
    1. _Test the students current knowledge, primarly fact based questions._
    2. _Let the student apply their current knowledge to learn new things about the subject._

**Example**: During the course or during a presentation you could provide the student with only the pros of a tool/language/framework, presenting why it's a good thing for the student to learn it. On the exam on the other hand, you could ask the question: _"What are the cons of using tool/language/framework?"_. 

If the student can answer the question the student will have deducted the answer and learn't something new. If the student failed to answer the question the student should now know what to research/study for the future. 

### Written exams

You get to see what students know when all help is taken away. This gives a clear picture of basic knowledge. Conditions are artificial compared to actual work, which involve stack overflow to a sometimes alarming degree. The score of an exam is super useful in getting to know the skill of each student. Students with lower scores should be higher on your priority throughout the education.

* Good for testing theoretical and basic knowledge.
* Grade levels can feel arbitrary, but actually give a pretty good picture of the students knowledge. This is useful when making groups for projects.
* Bad for testing practical coding skill.
* Bad for testing knowledge about larger projects.
* Better for first term courses than later courses, because projects will be larger.
* Sample questions:
* * What is the result of the following JavaScript operation? `'1' + 0` (answer: '10')
* * Write a function that calculates the sum of an arbitrary list of integers
* * What does the following code print to the console? (several rows, tests student ability to read code and understand the compiler/interpreter)

// A separate document might be useful, with different kinds of useful exam questions, and types of questions to avoid

### Home exams

A home exam is basically an obligatory assignment that each student makes. Students will be able to google and discuss the exam among themselves.

* Use open ended questions where students need to argue, rather than find the correct solution: _What are the main advantages and disadvantages of framework X?_ rather than _Is this function synchronous or asynchronous?_
* Students are forced to actually research the questions, so you can ask questions about stuff you have not gone through in detail.
* Try to formulate questions so the answer is not immediately obvious if you type the question in google.
* Better for thinking about the whole picture, rather than specific problems and solutions.
* Good for later courses, when the answer is not directly obvious or you want students to use previous knowledge to make a point.

### Quizzes

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
