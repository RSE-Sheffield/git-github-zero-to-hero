---
title: Pulling from a remote repository
weight: 7
---
**Push** makes sure that your work is not only in your computer but "online" as well which means:

  - It is backed up.
  - You can access it from any location.
  - If your repository is open, other people can benefit from your work, they can contribute, reference you or even make recommendations.
  
Now, what if you you make changes directly on the GitHub repository or using another machine? These changes are not locally synchronized with your primary computer. This is where **pull** comes into play.  

<br>

- Navigate to your repository in GitHub and scroll down to *README.md*. GitHub automatically uses this file as a landing page to a repository which at the moment should be a mere *git-lesson*. To edit this file click on the small pencil icon. This icon is available for any file if you click on it but specifically for `README.md` it's also available as soon as you enter your repository.

	<img src="/images/work-9-gk.png" alt="title picture" width="700px">	

<br>


- Now let's add some text, *Markdown* text (more on markdown [later](https://annakrystalli.me/open-source-workshop/practicalexercises/github/git-02-websites-with-github-pages)).

	<img src="/images/work-11-gk.png" alt="title picture" width="700px">
<br>

- Let's see how our Markdown code is rendered and check for typos in the text. If we are happy we can commit the changes. Since we are working online on GitHub there is no **push**.

	<img src="/images/work-10-gk.png" alt="title picture" width="700px">

<br>

- Now back in GitKraken Client, we see that our remote repository is ahead of our local. We can also see that it is the local README.md file that is out of date. In order to synchronize the local with the remote repository we can use **Pull**. This will "download" any updates from the remote repository to our local one.

	<img src="/images/work-12-gk.png" alt="title picture" width="700px">

<br>

- Let's seen what happened after pulling the remote repository.

	<img src="/images/work-13-gk.png" alt="title picture" width="700px">

<br>
