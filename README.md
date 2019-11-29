# Storyteller: A Web Appication for Short Stories

Storyteller is a self-started modern organizational web app that helps to organize and write novels, poetry, and prose.


There are several versions of this project that range from having a MERN stack, one with GraphQL (in order to provide a single-source-of-truth for the API) as well as firebase (which I wanted to try to test how it's authentication method works). Currently the site that is on display uses Firebase.

## Conception and Introduction of the Problem

In the beginning, this application was heavily inspired by [Novelize](https://getnovelize.com/), a simplified novel-writing application that helps writers keep track of their writing flow, character progression, and manuscripts. I would say it is best known for it's wide-range customization features (i.e. the ability for the writer to add custom categories of what they would like to keep track of) as well as it's modern style and a rather simple interface that makes it easy to use and quick to learn.

![Screen shot of Novelize story writing Chapter One](https://lh3.googleusercontent.com/7pfOXfy9TygQ-riovUuQWxeF1gvG7-eSGVCrPSJPspY9ZMktC7u7AARvS224PofqE1F42pX8Rg=w640-h400-e365)

*A screenshot of it's many features*

That being said, I thoroughly enjoyed my time when I used Novelize during my days in college. Having a background in writing, I really appreciated the app's flexibility. Novelize has a ton of features and as well as a few core templates that allow it to appeal to not only novelists, but publishers, editors, and college students alike.

That being said though, I, like many other writers are often overcome by the ability to customize and will spend so much time in the beginning designing characters, detailing backstories, and drawing out story maps that when presented with (even still) the white screen of emptiness and despair that we often immediately fall into sea of writer's block and go back to the safe harbor of detailing our would-be villans and superheros.

Too many I think, this is a personal hurdle that writers must push through themselves. There's no other real solution to it, and you find many inspirational books and 'how-to' guides that merely say, "Just start writing. [The first draft is always shitty](https://wrd.as.uky.edu/sites/default/files/1-Shitty%20First%20Drafts.pdf). The sooner you start the better you get."

But I thought, how can I make this process easier for the writer? What tools can I provide that would perhaps kickstart this turn of events.

## The Solution

Storyteller provides a temporarily solution to this by initially offering the writer a sort of free writing structure or template to kick off their overall writing process. It follows (for now at least) Dan Harmon's guide of ["The Story Embryo"](http://channel101.wikia.com/wiki/Story_Structure_104:_The_Juicy_Detail) directly to the point of how most popular movies, TV shows, and novels follow a sort of 8-step plan to developing a character, breaking that characer down, and rebuilding him/her in a new or different situation than they were in after a series of (un)fortunate events. 

![One interpretation of the Dan Harmon's Story Embryo](https://notjustamoviepodcast.files.wordpress.com/2014/08/story-circle.png)
*A visual diagram of the story embryo, according to Dan Harmon.*


While I still need to research on perhaps better or more thorough guides, this is ultimately the idea of a feature I thought would be a great asset to a site like [Novelize](https://getnovelize.com/) that has really brimmed on their potential and still have so many possibilities left to conquer.

### Features & User Stories

Currently such general features are thought to be of as such:

- All users (regardless of authenticated or not) should be able to view all stories on the browsing page
- All users should be able to log in or create an account, via Google or through the site itself
- Authenticated users should be able to view the stories that _they_ have written on a separate profile page with information pertaining to only them
- Authenticated users should be able to edit or delete _only_ the stories that they have created.
- Authenticated users should have the ability to view other user's profile pages, but should not be able to edit or delete anything on said pages
- All users should have the ability to view most recently updated stories displayed on the browsing page.
- All users should be able to rate or 'like' stories, but the ability to downvote stories or 'dislike stories' should not be a thing
- All users should be able to search for stories based on genre, rating, or language

### UX Challenges

Probably the biggest initial hurdle with the design of this was choosing a proper color scheme that would help encourage the writer to write. I had noticed that Novelize had choosen to go with a warm orange color that is often associated with friendliness and creativity, but for my choice I felt locked between the decision to use a blue-based color palatte vs a purple-based one.

![Rosy Purplish Color Scheme]()

### UX Solutions

The reason for this challenge is less about what is most aesthetically pleasing and moreso about choosing colors that would fit the proper atmosphere for whatever time of day the author wishes to write. 

While doing a bit of research and asking around, it was revealed that most writers (although the time at which they choose to write varies) openly admit that the time at which they feel most creative is during the early evening up until they are about to fall asleep. In this sense, I decided that working with a brighter color like orange or light blue would be less ideal, because those colors seem to be used more often than not to control attention and to stimulate. 

Therefore, I decided to go with a more rosy gold, purplish color scheme because I thought the mood it encourages would be able to flux between both day and night without incurring eye fatigue or boredom.

### Developer Challenges

The core of my challenges code-wise lie in the initial way I've drawn up the database infrastructure as well as my unfamiliarity with Firebase and using online cloud storage as a database. My current issue is that because I am unfamiliar with how to retrieve nested data from the Firebase, the possibility the following tree structure:

```user --> user's stories --> stories' chapters```

has become sort of a hassle to implement because I have yet to find sufficient documentation on how to setup proper models with firebase. From my experience however, it seems that Firebase has a pretty flexbile infrastructure in that it merely adds on the differences in structure when a user or admin updates a document, and it is only when trying to pull this information back out on the front end (say, if one document has a "names" property and another doesn't within the same collection ) that you will then begin to run into problems.



### Developer Solutions

Although is listed a somewhat cumbersome issue, really the only issue that's stopping me from progressing is lack of time


## Built With

* ReactJS - for my frontend framework
* Firebase - provides the cloud storage and user authentication through social media
* React-Materialize - Used for styling in combination with SASS
* Surge - used for deployment
* Adobe XD CC - for wireframing and prototyping
* Adobe Illustrator and Autodesk Sketchbook Pro - for icon creation


## Acknowledgments

* Novelize (for inspo!)
