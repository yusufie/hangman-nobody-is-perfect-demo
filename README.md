# Create a hangman game

## Overview

If this is the first time you hear of Hangman, I suggest you read this [article](https://en.wikipedia.org/wiki/Hangman_(game)) and watch this [video](https://www.youtube.com/watch?v=leW9ZotUVYo).

Instead of having another player suggest the game, we will automate this by using an API as you can see in the requirements section. Example of what we want to accomplish [here](https://codepen.io/cathydutton/pen/ldazc). You can use it to know exactly what the game is about, but do not copy it. Use your own way. Be as creative as you can!

![Example of hangman game](images/example.jpg)

### Requirements

1. HTML:
    1. Add buttons that correspond to each letter from a to z.
    2. Add a section that will hold the blanks that are going to be equal to the number of characters for the current word.
    3. Add a div to show the man who's going to be hanged if you lose.
    4. Add a counter from 10 that will decrease by 1 with every wrong guess.
    5. Add a button to play again.

2. JS:
    1. At the beginning use fetch API to retrieve a random word from this api <https://random-word-api.herokuapp.com/word?number=1>. Make the blanks equal the number of letters in the random word.
    2. Everytime the user clicks on one of the letters the following should happen:
        1. Search through the random word to find if it contains the clicked letter, if the clicked letter is part of the random word's letters then it gets shown up instead of the space, if not, then the lives counter is decreased by one. In some cases a clicked letter corresponds to two letters in the generated word, if that happens then show both letters. Also, with every mistake draw a part of the hangman's body. You can draw your own designs. It doesn't have to be a hangman, it can any creature that you want. Be creative with this. One of the best ways to do this is to use the [HTML5 canvas](https://developer.mozilla.org/en-US/docs/Web/API/Canvas_API) element.
        2. The button becomes disabled and should only work once.
    3. If the lives counter reaches 0 then the game is over and the man should be HANGED! 👨‍🦱🔪😢
    4. Clicking on the play again button should do the whole process again.

3. CSS: We leave this to your imagination. Generally, design something that screams with your personality. I don't want to see an exact copy of the screenshot, but I do want to see something that is fun and unique.

## Team Management

- Working on this project should be a team work endeavour; that means that the whole team needs to pitch in and work together.
- Having a call between team members in the beginning of the project to look at what's needed then breaking down the tasks to manageable chunks, creating issues in Github, assigning issues to every member of the team and updating the Github project's boards according to what everyone is doing is important.
- Create an `issue` for every tasks. You can create one issue for big tasks and divide it into smaller issues inside with checkboxes.
- Use `projects` in github to manage the tasks, they can be useful in arranging the tasks or issues with description and image so everyone knows what they should do
- To track your work its better to add columns like `in progress`, `done` , and `closed`
- Minimize the communication required in Discord. Sending messages in the same group to ask "Who is working on task#2?" Should be direct to Github projects instead to look at the board there.

## Coding Phase

- You should create a branch locally with the naming convention `[issue id - issue title]` and then push it and submit a Pull Request that must be close that issue. So, if you are working on the word fetching feature, then a reasonable name for the branch should be `3-fetch-word`. Look at this [article](https://github.blog/2013-05-14-closing-issues-via-pull-requests/) to know more.
- Once you finish working on your issue/task, push your branch to Github and create a pull request to the `master/main` branch. This way others can see your code and review it and you can easily automate the project managment part so that when the PR is accepted, the connect issue becomes completed and moved to the **DONE** section.

## Git

### **Pull Requests**

- Go to the issues board and create a new issue with the task assigned to you.
- Assign the issue to yourself so others know who is working on this issue.
- After finishing the work, push your code and assign your team membmers on that pull request so they can review the code.

### **Commit Message Format**

Each commit message consists of a **header**, a **body** and a **footer**. The header has a special format that includes a **type** and a **subject**:

```
<type>: <subject>
<BLANK LINE>
<body>
```

The **header** is mandatory, while the **body** is optional but highly encouraged.

### **Type**

Must be one of the following:

- **Build**: Changes that affect the build system or external dependencies (example scopes: gulp, broccoli, npm)
- **Doc**: Documentation only changes
- **Feat**: A new feature
- **Fix**: A bug fix
- **Perf**: A code change that improves performance
- **Refactor**: A code change that neither fixes a bug nor adds a feature
- **Style**: Changes that do not affect the meaning of the code (white-space, formatting, missing semi-colons, etc)

### **Subject**

The subject contains a succinct description of the change:

- use the imperative, present tense: “change” not “changed” nor “changes”
- don’t capitalize the first letter
- no dot (.) at the end

### **Body**

Just as in the **subject**, use the imperative, present tense: “change” not “changed” nor “changes”. The body should include the motivation for the change and contrast this with previous behavior.

## The Code

- The code should be totally clean and checked line by line before committing and pushing.
- You shouldn't leave any unnecessary comments in the code.
- Don't leave any logs inside the code.
- All variables should be `const` except for specific cases where you will need to use `let`
- Variables should use camelCase naming convention
- CSS classes should follow BEM naming convention. *You can find more about it [here](http://getbem.com/naming/) and [here (Youtube)](https://www.youtube.com/watch?v=SLjHSVwXYq4)*
- Leave only one empty line between CSS classes. This also goes for different purpose code blocks (like `functions` and variables under it).
- Make sure your naming is right and not confusing i.e. the `sidebar` shouldn't be named `sidediv` or when you fetch `words` your function should return `words` not `stuff` or `x`
- Make sure you clean your imported modules or files that you don't use before committing. The same goes for any variable, function or piece of code not used.
- Don't repeat yourself (DRY). Make sure the code you write is reusable and reduce repetition of information of all kinds. For example, don't write two functions that do the same or almost the same job. *Read more about DRY [here](https://en.wikipedia.org/wiki/Don't_repeat_yourself).*

## Presentation

Your demo will be 10 minutes. We will time it. It's not meant to be a high pressure situation but we want to make sure that everyone has time to demo in the allocated time.

### Requirements

Please read these instructions and prepare some thoughts on these for your demo.

- Show us your work. We will go through this quickly. If you published your work on a netlify or github pages, share the link with everyone in the chat to use it.
- Each member will speak briefly about one part of the code, maximum of 1 minute per person. Remember the requirement that every member must be able to to explain any part of the code. Please think about what you want to say beforehand, usually people make it up as they go and it takes too long. I will cut you off if it goes longer than a minute, for the sake of having everyone present.
- What were the three hardest problems that you faced? One person answers this.
- Team work is important. How did you work together? How did you divide the work? One person answers this.
- If you could go back to the beginning of the project and rewrite it from scratch, what would you do? All members of the team.
- Reflection: all of the members must speak about what stood out to them about their learnings from the project. It can be abstract ("I learned how to better find my mistakes") or concrete ("I learned more about the DOM.").
- Reflection: what do you think is the difference between working on a project and working on small exercises?
