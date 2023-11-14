## Assignment Submission Requirements
- Course Title [CPNT 262-A Web Client and Server Programming]
- Assignment 6 - Reactivity and Events
- Code by: John Dagsa
- Netlify Deployed Site [https://bespoke-sundae-b00200.netlify.app/]
- GitHub Repo Link [https://github.com/jdvgsa/reactivity-test]
- GitHub Pages Link [https://jdvgsa.github.io/reactivity-test/]


## Attributions

I took huge inspiration from a youtube channel called "Cooper Codes".

I made the to do checklist app with the guidance from this youtube video. [https://www.youtube.com/watch?v=MnTfpmVzxQc&ab_channel=CooperCodes]

In this video, he demonstrates how to create a To Do List / Checklist app with sveltekit.
He goes over how to create the scripts, loop through the tasks with svelte, creating the logic for editing and deleting tasks, and finally he goes over how to render the input from user when they "add" task.
This video is extremely in-depth and provides you with the knowledge to be able to create your own app for future projects.

## Search Terms

My Goal was to create a component/button that would reset/refresh the page so that the site would be reset/restarted to it's initial state.

The search term I used was not great but it was ["How to reset a page Javascript"] which took me to this link [https://www.freecodecamp.org/news/javascript-refresh-page-how-to-reload-a-page-in-js/#:~:text=The%20simplest%20way%20to%20refresh,and%20loading%20the%20latest%20content] which helped me get an idea but I needed more information.

I then refined my search a bit by adding the keyword ["stackoverflow"] at the end of my search which finally gave me this link [https://stackoverflow.com/questions/29884654/button-that-refreshes-the-page-on-click].

Through the answers provided, I was able to take the sample code
/**
 function refreshPage() {
 window.location.reload();
} 
<button type="submit" onClick="refreshPage()">Refresh Button</button> **/

and implement it into my own component (Reset.svelte).

