# HTML Template

We have a number of template repositories prepared in our `appdev-projects` GitHub organization for you to use.

This lesson details the `html-template` and how to make use of it to work on your own side projects.

Find the template at this link:

[github.com/appdev-projects/html-template](https://github.com/appdev-projects/html-template)

## Create repository from template

As opposed to the graded class projects, which you will begin by clicking a "Load [assignment]" button and forking, for our template repositories, you will manually create your own blank app. 

- Once you have signed in to GitHub, visit the template of your choosing (e.g. [appdev-projects/html-template](https://github.com/appdev-projects/html-template) is a good one for hosting static HTML pages) and click the "Use this template" button, and select "Create a new repository" from the dropdown:

<!-- ![](/assets/gh-pages-template-1.png) -->
![](https://res.cloudinary.com/dmxgp9oq2/image/upload/v1686161492/gh-pages-template-1_tlxhbl.png)
{: .bleed-full }

- On the next screen, leave the "Owner" dropdown alone, it should be set to _your_ GitHub username.
- For "Repository name", enter any name you would like for your new project. **You should choose a unique, memorable name for the repository. It does not have to match the template name.**
- Make sure the "Public" option is selected. 
- Click "Create repository from template".

<!-- ![](/assets/gh-pages-template-2.png) -->
![](https://res.cloudinary.com/dmxgp9oq2/image/upload/v1686166582/gh-pages-template-2_rvvdb4.png)
{: .bleed-full }

After a moment you will be brought to the new page at `github.com/<your-username>/<name-you-chose>`, with a copy of all the code from that template. You can get to work right away in a new codespace. Be patient, it will take about two full minutes to fully prepare, but subsequent boots of the codespace will be much faster from [your `github.com/codespaces` dashboard](https://github.com/codespaces).

<aside markdown="1">
You can also work on any project on [Gitpod](https://learn.firstdraft.com/lessons/48-gitpod-setup), or in a [local setup](https://learn.firstdraft.com/lessons/49-local-setup), but we recommend sticking with codespaces as your development environment for now.
</aside>

### This is not a fork

**This is not a fork, this is a newly generated codebase from a template repository.**

What does that mean for us practically?

* Just like a fork, the template generated repo contains a snapshot of all of the code in the repository you generated the template from.
* The template generated code is not tied to the upstream forked repository, meaning that changes to the upstream fork (i.e. commits) cannot be easily fetched into the new codebase.
* Creating codespaces from the template generated repo [will use your free monthly Codespace hours](#a-note-about-codespace-hours){: target="_self"}.
* Template generated code is not graded, so `rake grade` won't be necessary. The templates are just there for you to have fun with and build your own apps!

### A note about codespace hours

When you generate a repository from a template, rather than forking it in the case of the graded projects, the codespaces hours that you use will be billed to **your personal account rather than the `appdev-projects` organization**. But fear not, all GitHub accounts have 60 free codespace hours per month included.

<aside markdown="1">
Technically, all GitHub accounts have 120 free CPU hours (or 180 for Pro accounts) on Codespaces. By default, a new codespace is generated on a 2-core machine (2 CPUs), hence 120 core hours ➗ 2 cores = 60 hours. You can [increase the number of cores](https://learn.firstdraft.com/lessons/47-codespaces-setup#increasing-cores-on-a-codespace), but beware of that eating into your free hours significantly.
</aside>

You can also apply for education benefits on [education.github.com](https://education.github.com/discount_requests/application). Just select "Student" and ideally use a `.edu` email address associated with your school. After a processing period, your account will be upgraded to a free GitHub Pro account, which includes 90 free codespace hours!

Likely, the 60 (or 90) free monthly codespace hours will be sufficient for you to work on side projects, as the majority of time spent coding will be on graded forks of non-template projects.

If you're ever unsure of who is paying for the codespace hours in a given repository, just have a look at the note in the "Code" dropdown menu when you create a new codespace:

---

<!-- ![](/assets/who-pays-for-codespace.png) -->
![](https://res.cloudinary.com/dmxgp9oq2/image/upload/v1686181395/who-pays-for-codespace_rtvrwn.png)

## HTML Template

We made use of the HTML Template beginning in the "Hello, world!" lesson, which was actually just a project we generated from that template and added a couple of `rake grade` tests to. It's a good template for creating static HTML + CSS sites and deploying to GitHub Pages.

You can find the repository at:

* [appdev-projects/html-template](https://github.com/appdev-projects/html-template)

If you want to deploy a website from this template, just follow the instructions in the "Hello, World" lesson to [deploy the app](https://learn.firstdraft.com/lessons/106-hello-world#deploy-your-app).

### "Hidden" files

You may have noticed something a bit odd about the `appdev-projects/html-template` repository compared to codespaces that you made from forks or templates of it.

The repository page on `github.com/appdev-projects/html-template` has a whole bunch of files and folders in it:

---

<!-- ![](/assets/hidden-files-vscode-1.png) -->
![](https://res.cloudinary.com/dmxgp9oq2/image/upload/v1686182198/hidden-files-vscode-1_lsrufp.png)

---

But, when you booted up a codespace, the integrated VSCode file explorer appeared to be completely empty:

---

<!-- ![](/assets/hidden-files-vscode-2.png) -->
![](https://res.cloudinary.com/dmxgp9oq2/image/upload/v1686182995/hidden-files-vscode-2_jsrsjw.png)

---

I can assure you, the files _are_ there, but early in your developer journey we didn't want to distract you with all the supplementary files needed to do things like setup the codespaces environment, monitor your Git version controlling, run the live preview, and more. So we "hid" them in the VSCode explorer!

Curious? Just go to a bash prompt in terminal pane and run the command: 

```
% ls -a
```

(`ls` for "list" and `-a` for "all" files and folders in the current directory including any that start with a `.`):

---

<!-- ![](/assets/hidden-files-vscode-3.png) -->
![](https://res.cloudinary.com/dmxgp9oq2/image/upload/v1686182996/hidden-files-vscode-3_qr9h7m.png)

---

But what if you wanted to actually open one of those files to make some changes? You probably don't want to do that in early projects, but if you ever need to, you can simply run the command: 

```
% code <file-name>
``` 

or 

```
% code <folder-name>/<file-name>
``` 

and VSCode will open that file in your editor pane.

And, FYI, we hid the files by modifying the `.vscode/settings.json` file like so:

<!-- ![](/assets/hidden-files-vscode-4.png) -->
![](https://res.cloudinary.com/dmxgp9oq2/image/upload/v1686182997/hidden-files-vscode-4_b0eku7.png)

---
