## Configure Github

This document will walk you through configuring your personal github account so you can work
effectively from the command line in your future classes.

Students can get a free [Github Pro](https://education.github.com/pack) account as long as you sign
up with your Boise State email address. This will allow you to use Github Codespaces and other cool
services for free in all your classes. If you run out of free hours on codespaces you can use the CS
department lab machines to complete all projects. You **never** have to pay for GitHub, all
assignments can be completed with the free tier or in the CS Labs.

## GitHub Student Developer Pack

As a student you can get access to a free GitHub Pro account as well as other really cool features
such as GitHub Copilot and GitHub Codespaces.

- [Get your developer Pack](https://education.github.com/pack)
- [Sign up for Copilot](https://education.github.com/experiences/primer_copilot)

::: danger

Be aware that there are some professors in the CS department who view using A.I. technologies such
as Copilot as cheating. So please carefully read the syllabus in all your classes and look for their
policy regarding using A.I. tools.

:::

## Install the command line client

You can skip this task if you are working on one of the cs lab machines.
The gh command line tool is already installed for you.

Install the github command line client [cli.github.com](https://cli.github.com/).

Windows users **MUST** reboot their machines. If you are on windows do not
continue until you have rebooted your machine. Once the gh tool is installed you
should be able to open a terminal and type **gh** as shown below.

```bash
$ gh
Work seamlessly with GitHub from the command line.

USAGE
  gh <command> <subcommand> [flags]

... Lots more output!
```

## Setup Authorization

We want to configure our machine to use ssh keys using the command
`gh auth login`. Other tools and some Integrated developer environments
need ssh to work properly. This will ensure that your setup will work no
matter how you choose to write code 😃.

```bash
$ gh auth login
? What account do you want to log into? GitHub.com
? You're already logged into github.com. Do you want to re-authenticate? Yes
? What is your preferred protocol for Git operations? SSH
? Generate a new SSH key to add to your GitHub account? Yes
? Enter a passphrase for your new SSH key (Optional)
? Title for your SSH key: (GitHub CLI
? Title for your SSH key: GitHub CLI
? How would you like to authenticate GitHub CLI? Login with a web browse
! First copy your one-time code: XXXX-XXXX
Press Enter to open github.com in your browser...
✓ Authentication complete.
- gh config set -h github.com git_protocol ssh
✓ Configured git protocol
✓ Uploaded the SSH key to your GitHub account: C:\Users\shane\.ssh\id_ed25519.pub
✓ Logged in as shanep
```

## Confirm everything works

We want to confirm that we have everything setup correctly. Luckily the
command line tool has an option to do this for us. Run the command
`gh auth status` and you should see output similar to what is shown
below.

Your output will be slightly different depending on the OS and other
factors. You are not required to match the output exactly, you just need
to confirm that github.com is configured to use the ssh protocol.

```bash
gh auth status
github.com
  ✓ Logged in to github.com as shanep (keyring)
  ✓ Git operations for github.com configured to use ssh protocol.
  ✓ Token: gho_************************************
  ✓ Token scopes: admin:public_key, gist, read:org, repo
```

Congrats you are now configured to use github.com with the ssh protocol!

## Submitting

Log into canvas and submit a screen shot showing that you have completed the assignment. An example
is shown below. **NOTE:** Your screen shot may look slightly different depending on the Operating
System so don't worry if it doe not match exactly.

![gh cli](/images/gh-cli-submit.png)
