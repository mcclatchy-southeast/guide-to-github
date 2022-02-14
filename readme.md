
# A McClatchy Southeast guide to GitHub

Prepared by Lucille Sherman and Tyler Dukes. *Note: This is a working draft subject to change and review.*

There are four parts to this guide: 
 1. What you need
 2. How to organize
 3. How to commit
 4. Collaboration

## What you need

### TITLE
Title of the project, also known as the repository name. Usually the slug or something close to it. 

### DESCRIPTION
This should read sort of like a budline. Here’s a good example: “Data for Wasted Minds, an investigation into educational opportunities for inmates within the Florida Department of Corrections.”

### README

Here’s [a guide to formatting a markdown file](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet). 

Here’s what to include in the readme:

#### HOW WE DID IT
How did you complete the analysis or build the dataset? What tools did you use? Whose analysis did you model yours after? 

#### WHY WE DID IT
What’s unique about this project? What part does it play in the overall investigation or story? 

#### DATASET EXPLAINERS
If you have a massive amount of separate datasets, consider including explainers of each if the file names aren’t self explanatory (make your file names self explanatory, though). Here’s [an index example](https://github.com/GateHouseMedia/wasted-minds). 

#### ACKNOWLEDGEMENTS/KUDOS
List people who helped you with this project, link their GitHub username or Twitter handle and provide a description of what they assisted with.

#### WORTH NOTING
Include caveats or issues here. 

#### CONTACT INFORMATION
Name, email, Twitter handle, link to your GitHub repo, if applicable.

#### LINKS
Don’t forget to embed links to your project and other methodology pages housed on the project site.

#### DATA
Include all files that were used as part of the project or analysis. If you need to exclude datasets that aren’t allowed to be shared, [add them to a .gitignore file](https://help.github.com/en/articles/ignoring-files). (If you forget to do that, as I often do, [use this guide](https://help.github.com/en/articles/removing-sensitive-data-from-a-repository) to scrub your repo history.) Again, include an explainer or index for datasets if there are a lot or they’re not self-explanatory. 

#### CODE
Same applies here. Include all files that were a part of the project or analysis. Don’t forget to remove API keys, passwords or other sensitive information. If you forget to remove them before committing, [use this guide to scrub your repo history](https://help.github.com/en/articles/removing-sensitive-data-from-a-repository). 

## How to organize

Below is one folder structure example.

main-project-folder

 - data
 - scripts
 - interviews
 - clips
 - story-drafts
 - visuals
 - readme

Within each folder, you can include specific folders for specific datasets or scripts, and then run a .gitignore on interviews, clips, drafts, sensitive datasets, etc. 

*Still need to figure out best practices for creating “clean” versions of scripts without passwords, keys, etc. 

## How to commit

 1. Go to https://github.com/mcclatchy-southeast.
 2. Click the green box that says https://github.com/mcclatchy-southeast “New” near the top on the right-hand side.
 3. Give the repo a title
 4. Give it a description, if you’re ready. 
 5. Keep the repo set to private until your project is published and all your code is up and organized.
 6. Click “create repository.” 
 7. The next page will walk you through steps to commit your data and code from the command line (Make sure you’re already set up to use Git from the command line. Here’s a quick guide to using it, if you need a refresher. You also might need to set your username in Git.). If you don’t want to do that, manually add your files in the web browser.
 8. Set the repo to public.

## Collaboration

Instead of sending chunks of code through Slack, use GitHub.

 1. Clone the repo.
 2. Create a new branch: `$git checkout -b branchname`
 3. Work on that branch. 
 4. Stage, commit and push changes on that branch: 
	```bash
	$ git add filechanged
	$ git commit -m “commit message” 
	$ git push --set-upstream origin branchname
	```
5. Then, create a pull request for the file remotely. There are two ways to do this.
   - You can do it remotely [using this guide](https://help.github.com/en/articles/creating-a-pull-request). (After you make a commit from a branch from your machine, git should give you a link to create a pull request.)
   - Or from your command line, [using this package](https://hub.github.com/).
   *Either way, don’t forget to **assign a reviewer**. (That way the owner of the project gets a notification that you’ve made changes and submitted a pull request). 
  6. Merge. 