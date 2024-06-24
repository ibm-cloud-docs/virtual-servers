# Getting Started with Markdown

## What is Markdown?

Markdown is a lightweight markup language with plain text formatting syntax designed so that it can be converted to HTML. This opens our docs for easier collaboration with SMEs (subject matter experts), development, and even our customers. For more information, see [Getting started with Markdown](https://dev-console.stage1.bluemix.net/docs/developing/markdown/markdown.html#getting-started-with-markdown) in the content design and development guide. This will provide you with an in-depth overview of Markdown.

## Setting up your Markdown environment

Running builds locally on your system is a great way to look at your output before it goes through the actual build servers. You can see immediate output by running local builds as opposed to waiting 30 minutes to an hour for the build to be processed by the build team. Transforming your Markdown files into HTML files makes is much easier to run accessibility tools (DAP) and translation tools against your content, and it also allows for you to catch initial formatting errors.

### Step 1 - Prerequisites

1. Get authorized to GitHub
    **NOTE**: You should already have acquired access to GitHub if you completed the tasks in the [Welcome](Welcome.md) page.

2. Get Git
    * You need to install the latest versions of the following:
        * [Node JS](http://nodejs.org/)
        * [Git](http://git-scm.com/)

3. Get GitHub Desktop (this tool is awesome)
    * Install it locally from https://desktop.github.com/.
    * Open the tool and sign in with your Github ID and password.
    * Check your authorization - you will need to sign in to Github Enterprise (GHE). Navigate to **Github Desktop > Preferences**. Make sure you are signed in.
    * From GitHub Desktop you can clone the repositories that you need to your local environment.

### Step 2 - Cloning the repositories

Assuming that you installed Github Desktop, use it to clone the repositories.

1. Clone both the staging repository and the production repository
    * Click File.
    * Click Clone repository....
    * Enter the link for the staging repository. The organization will be Bluemix-Docs. For example, https://github.ibm.com/Bluemix-Docs/appid.
    * Enter the link for the production repository. The organization will be IBM-Bluemix-Docs. For example, https://github.com/IBM-Bluemix-Docs/appid.
2. You should now see the repositories listed in Github Desktop. Click the Fetch origin button to pull the latest content on the remote repository down to your local system.

### Step 3 - Setting up the Markdown generator

1. What is it?
It transforms your Markdown files to HTML5 output. Installing it locally allows you to test and validate ouput.

2. Install the parser into a new directory.
    * On both Mac and Windows run:
      `npm install marked-it-cli`

      OR

      `npm install -g marked-it-cli`

    * From the [internal docs](https://github.ibm.com/Bluemix/docs/tree/staging/developing/markdown) repo, grab:
        * header.txt
        * footer.txt

    * From our build environment, grab the latest [conref](https://github.ibm.com/Bluemix-Docs/docs-build/blob/master/markdown/cloudoeconrefs.yml) file:
        * cloudoeconrefs.yml

    **Note**: These files (header.txt, footer.txt, cloudoeconrefs.yml) need to be copied into the marked-it-cli directory. To see the required arguments to build your content in IBM Cloud, see the table in the [content design and development](https://dev-console.stage1.bluemix.net/docs/developing/markdown/setup.html?pos=2#step-5-get-the-markdown-generator-markdown-html5-) guide. Also use this link for the sample commands for Mac and Windows in order to transform your Markdown files.

For more detailed instructions, see [Setting up your Markdown environment](https://dev-console.stage1.bluemix.net/docs/developing/markdown/setup.html#setting-up-your-markdown-environment).

## Creating content in Markdown
See [Creating IBM Cloud content in Markdown](https://dev-console.stage1.bluemix.net/docs/developing/markdown/create.html?pos=2#creating-ibm-cloud-content-in-markdown).

## Creating Markdown navigation
See [Creating Markdown navigation files for IBM Cloud docs](https://dev-console.stage1.bluemix.net/docs/developing/markdown/navigation.html?pos=2#creating-markdown-navigation-files-for-ibm-cloud-docs).

## Markdown tips
See [Markdown tips](https://dev-console.stage1.bluemix.net/docs/developing/markdown/tips.html?pos=2#markdown-tips).

## Requesting help with builds
If you need help with new builds, issues, or migration, see [Requesting build focal help](https://dev-console.stage1.bluemix.net/docs/developing/build/build_templates.html#requesting-a-documentation-build-and-getting-build-focal-help-if-needed-.).
