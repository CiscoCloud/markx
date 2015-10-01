# Markx
### Markdown editor for scientific writing. Batteries included.

## Why Markx?
Markdown has recently become popular among academics as a way to produce scientific documents. 
When paired with document conversion engines such as pandoc, it provides an easy and powerful way to write.
Being a simple plain-text markup language, Markdown is easy to learn, and can be handled by version control systems.
We decided to build Markx as to make markdown writing a collaborative effort that could be hosted as web service.
For additional discussion, see these blog posts:

* [Markdown and the future of collaborative academic writing](http://inundata.org/2012/06/01/markdown-and-the-future-of-collaborative-manuscript-writing/)
* [Thoughts on a preprint server](http://inundata.org/2012/12/06/pre-print-servers/)
* [How to ditch Word](http://inundata.org/2012/12/04/how-to-ditch-word/)  

![](https://raw.github.com/yoavram/markx/master/screenshot.png)

## Features

1. Free as in free speech - promotes open science, pre-publication review, collaboration.
1. Free as in free beer - uses open-source, free software and released under [CC-NC-BY 3.0](http://creativecommons.org/licenses/by-nc-sa/3.0/).
1. Easy to learn - [Markdown] is not LaTex, for better and worse.
1. Integration with [GitHub] - free hosted version control, ideal for backup, versioning and collaboration.
1. [Pandoc] integration - multiple Markdown extensions, multiple output formats.
1. Real-time Markdown preview - [WYSIWYM](http://en.wikipedia.org/wiki/WYSIWYM) / [WYSIWYG](http://en.wikipedia.org/wiki/WYSIWYG).
1. Display math with LaTeX formatting - $x^2+y^2=r^2$.
1. Citations - [BibTeX]: [@Drake1991]
1. Code highlighting:
		
		if __name__ == '__main__':
		    # Bind to PORT if defined, otherwise default to 5000.
		    port = int(os.environ.get('PORT', 5000))
		    app.run(host='0.0.0.0', port=port, debug=app.debug)
1. Local host option with a limited number of dependencies - for offline editing on the train and in the airplane
1. Remote host option at <http://markx.herokuapp.com/> - no installation required
1. By scientists, for scientists

## License

[![](http://i.creativecommons.org/l/by-nc-sa/3.0/80x15.png)](http://creativecommons.org/licenses/by-nc-sa/3.0/)

## Setting Up on Shipped
This is an sample project to demonstrate how to create/deploy a Python application using Shipped.

### Step 1. Set Up GitHub

[Git](https://git-scm.com/) is a source and version control system hosted on the web, and [GitHub](https://github.com/) is a repository of Git projects. Shipped stores your projects on GitHub, and you'll need a GitHub account to use Shipped. If you already have a GitHub account, skip to step 2. Otherwise, navigate to the [GitHub home page](https://github.com/) using any modern browser (we recommend Chrome), click on [Sign up](https://github.com/join) and follow the instructions to create a free account. You don't need to do anything more with GitHub at this time; Shipped will do it all for you.

### Step 2. Login to Shipped
Your GitHub account is all you need to login to Shipped. Navigate to the [Shipped welcome page](http://ciscocloud.github.io/) and click on the big green "Sign up with GitHub" button. 

![](https://github.com/CiscoCloud/markx/blob/master/shipped/images/welcome.Png)

Shipped displays its home page. If this is your first time in Shipped, it automatically pops up the Create Your Project dialog. If not, select Create New Project from the Your Projects dropdown to get the popup:

### Create Your Markx Project with Shipped

### Step 3 Compose Your Project
Use any modern browser (we recommend Chrome) to navigate to the the Shipped welcome page. If you're not logged, click on the big green "Sign up with GitHub" button to login. If this is your first project, Shipped automatically pops up a Create New Project form; if not, select Create New Project from the Your Projects dropdown to get the popup:
![](https://github.com/CiscoCloud/markx/blob/master/shipped/images/createproject.Png)

Enter a name for your project (we'll use "Markx-Dev" for this project) and press Start Composing. Shipped displays a list of development services:
### Step 4 Fork the Github project
#### Fork CiscoCloud/markx as your repository master project branch.
![](https://github.com/CiscoCloud/markx/blob/master/shipped/images/fork.Png)

### Step 5 Add a service
The development services listed are examples of what Shipped calls "microservices" - supporting services used by a project. We can choose as many microservices as needed for a project. Shipped installs whatever is needed to deploy the selected microservices on one of the VMs it creates for you. 

#### Step 5.1 Select a service type.
 
For this project we will select **"Python"** which create Python installed VM
![](https://github.com/CiscoCloud/markx/blob/master/shipped/images/selectservice.Png)

Click on the Select button to the right of this service. Shipped pops up the Service Configuration form that you'll use to specify the GitHub repository where Shipped will store the source code using the service:
 
#### Step 5.2 Provide github repository name. 

![](https://github.com/CiscoCloud/markx/blob/master/shipped/images/selectrepo.Png)


This form allow us to specify:

| Name | Description          |
| ------------------- | -------------------- |
| Name of GitHub Repository|	The name of the GitHub repository where Shipped stores the source code using this service. Shipped automatically creates the repository if necessary|
| GitHub Organization|	The GitHub account owning the repository. This can be your personal account, or the account of a company or organization associated with your account. |
| Private Public	The type of repository to create | private (available only to specific GitHub users) or public (viewable by any web user). You need a paid GitHub account to create a private repository.|
 

 
### Step 6. Build Your Project
#### Step 6.1 Initiate Build process.
 
 Specify "Markx" for the repository name and press Add Service. Shipped re-displays the Compose Your Project form with the repository name for the selected service above the Build Project button.
![](https://github.com/CiscoCloud/markx/blob/master/shipped/images/buildproject.Png)

To build your project, press the Build Project button. The button label changes to Building, and a status bar moves across the button while Shipped creates your GitHub repository and stores the description of your project in its database. When it's finished, it pops up the Let's Get Set Up form containing the command to bootstrap the project on your computer:
![](https://github.com/CiscoCloud/markx/blob/master/shipped/images/buildlocal.Png)

### Bootstrap Your Local Development Environment
Bootstrapping a Shipped project means downloading the project's source code to your machine; setting up a local Git repository tied to the cloud-based repository created by Shipped; installing the pre-requisite software Vagrant and VirtualBox (if necessary); creating and the virtual machines that host your development environment; setting up a continuous integration build; and brings up a web server running the new application. The process is fully automatic; you just need to copy and paste the command presented by Shipped when you created the project.

### Step 7.1 Bootstrap your environment (Refer 7.2 for fast bootstrap)

The bootstrap process runs in a command-line terminal window, so the first step in bootstrapping your project is opening a terminal window. The way you do this depends on your operating system:

| Os Type | Action          |
| ------------------- | -------------------- |
| OS X (Mac)|	Press Command + Space to open Spotlight Search. Type Terminal and double-click the Terminal Application. Menu option Shell -> New Window will open a new window for you. |
| Ubuntu |	Press Ctrl+Alt+T |
| Windows |	Click Start, type "cmd", and press Enter for a normal terminal window, or Ctrl+Shift+Enter for an Administrator terminal window. You will need an Administrator window if the bootstrap process needs to install Vagrant and VirtualBox. If you already have this software installed, you can use a normal terminal window. |

When you completed creating your project in Step 6, Shipped popped up the Let's Get Set Up form containing the bootstrap command:
![](https://github.com/CiscoCloud/markx/blob/master/shipped/images/buildlocal.Png)


Execute these command in console/terminal.
![](https://github.com/CiscoCloud/markx/blob/master/shipped/images/console.Png)

and on the Shipped browser window, which displays a circular animation ticking off each step in the bootstrap process as it happens:
![](https://github.com/CiscoCloud/markx/blob/master/shipped/images/buildstatus.Png)

Among its other actions, the Shipped bootstrap process brings up a web server on a newly-created VM and uses it to run your application. The last few lines output on the terminal window show you Shipped is running the application:
![](https://github.com/CiscoCloud/markx/blob/master/shipped/images/consoleout.Png)

#### OR


### Step 7.2 (*optional) Fast bootstrap your environment

In case you dont this build to be deployed locally. you can opt for fast bootstrap option.

you can set **fast** option while running your cli command inside terminal/console
for example:

shipped.exe -t FJLDKmsJvvoFlpVssIAYkbKrImXeovaV Local bootstrap 9c38dd91-5bdf-11e5-9640-0242ac110008 fast

![](https://github.com/CiscoCloud/markx/blob/master/shipped/images/fastbuild.Png)

This flag will skip all the Vagrant related process in bootstrap. This means it stops after cloning the repository(s) and downloading files. you can still proceed with local commit to initiate a shipped build. 

If we wants to build locally, we needs to bootstrap again.


### Build and Deploy the Application

### Step 8 Run a Build

Among the tasks Shipped performed during bootstrap was to store the application's source code in a local Git repository tied to the Git repository in the cloud, and set up a continuous integration build, so that any commit to the repository automatically triggers a build. When the bootstrap process completes, the Shipped browser window displays the command you need to run your first build:

![](https://github.com/CiscoCloud/markx/blob/master/shipped/images/pushbuild.Png)

Once again, select the command by clicking on it, copy and paste it into your terminal window. The command changes the directory to the one containing your new local Git repository and commits the initial copy of the application source to your cloud-based remote Git repository

This automatically triggers a build, you see this in event section at your browser window

### Step 9 Deploy Your Project to the Cloud

The last step in the bootstrap process is deploying your project's application to the Cisco cloud. To do this, click on the Deploy tab at the top left of the screen. Shipped displays the Deploy tab with a message that there are currently no deployed environments:

#### Step 9.1 Create environment.
Create a new Environment as 

![](https://github.com/CiscoCloud/markx/blob/master/shipped/images/newenv.Png)

#### Step 9.2 Deploy to environment.
Shipped shows the message "Deploying to environment..." under the environment name. please click on that , and a short time later replaces it with a "Deployed successfully" message:
![](https://github.com/CiscoCloud/markx/blob/master/shipped/images/deploy.Png)


Congratulations! You've deployed your Markx application to the cloud. Click on the URL in the "Deployed successfully" message to see the application running in its new environment

## Development Status

Markx is currently in development but can be used locally (see Installation instructions below) or remotely at <http://markx.herokuapp.com>.

It is still experimental, so **take care of your data!**

We would love to get feedback from anyone using it - Please [open an issue](https://github.com/yoavram/markx/issues) with any bug or suggestion. 
If you can't open an issue please contact Yoav on [twitter](http://www.twitter.com/yoavram) (you can use the `#markx` hashtag).

## Technology
  * Server side (this is what you need to install if you run it on localhost):
    * [Python] with [Flask] and [requests]
    * [Pandoc] - optional, for conversion to PDF, DOCX etc.
  * Client side (no installation required):
    * [PageDown] - [Stack Overflow]'s [Markdown] editor
    * [Google Code Prettifier] - Code highlighting
    * [MathJax] - Rendering of $LaTeX$ equations
    * [BibTeX-js] - Processing [BibTeX] citations
    * [Twitter Bootstrap] with [Glyphicons Free]
    * [Github.js] - integration with [GitHub]
  * 3rd Party services:
    * [GitHub] - version control hosting
    * [Docverter] - online conversion of Markdown to multiple formats (currently, citations are not supported)
    * [LaTeX-Online] - online compilation of LaTeX to PDF

## Install locally

1. Clone [this repository](https://github.com/yoavram/markx/)
1. Install [Python] - developed with version 2.7 
1. Install [Flask] and [requests]: `pip install Flask requests`
1. Optionally install [Pandoc]
1. Run Markx by calling `python server.py` and pointing your browser at <http://localhost:5000>.
1. Load a BibTeX file with your citation library by choosing `Load a Bibliography File` from the `Bibliography` menu

More help can be found in the [help file](https://github.com/yoavram/markx/blob/master/HELP.md).

##References
[Markdown]: http://daringfireball.net/projects/markdown/
[Pandoc]: http://johnmacfarlane.net/pandoc
[Python]: http://python.org/
[Flask]: http://flask.pocoo.org/
[Twitter Bootstrap]: http://blog.getbootstrap.com/
[Google Code Prettifier]: http://code.google.com/p/google-code-prettify/
[Icomoon Free]: http://keyamoon.com/icomoon/
[MathJax]: http://mathjax.org/
[PageDown]: http://code.google.com/p/pagedown/
[BibTeX-js]: http://bibtex-js.googlecode.com/
[Stack Overflow]: http://stackoverflow.com/
[git]: http://git-scm.com/
[BibTeX]: http://www.bibtex.org/
[GitHub]: https://github.com/
[Github.js]: https://github.com/michael/github
[Docverter]: http://www.docverter.com/
[requests]: http://python-requests.org/
[LaTeX-Online]: https://github.com/aslushnikov/latex-online
