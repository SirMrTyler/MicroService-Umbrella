# MicroService-Umbrella

This repository is the **umbrella** repo for our microservices system.  
It contains each microservice as a **Git submodule** under `services/`.

> IMPORTANT: The microservice repos are **private**.  
> You must be a member of the org/team with access to the repos before submodules will clone successfully.

---

## Repo Structure

- MicroService-Umbrella/
  - services/
    - email-verification/ (Tyler)
    - image-bg-removal/ (Tyler)
    - buddha-quote-gen/ (Kaia)
    - joke-microservice/ (Kaia)
    - holiday-microservice/ (Ford)
    - random-username-gen/ (Ford)
    - golf-api/ - email-verification/ (Wiley)
    - zip-code-microservice/ (Wiley)
    - email-sender/ (Unassigned)
  - .gitmodules

---

## Clone the Umbrella Repo + All Submodules (Recommended)

Use _this command_ in your bash terminal to clone everything in one go (after accepting the team invite):

```bash
git clone --recurse-submodules https://github.com/SirMrTyler/MicroService-Umbrella.git
```

> NOTE: If the command doesn't work; see the `## Prerequisites` section below (you may not be logged in via your IDE/console/terminal/etc)

## Prerequisites

1. Make sure you accepted the GitHub Organization/Team invite.
2. Make sure Git can authenticate to GitHub for private repos:
   - **Recommended:** SSH set up (`ssh -T git@github.com`)
   - Or: GitHub CLI auth (`gh auth login`)

---

## Making Changes

> **VERY IMPORTANT**: Make sure you cd INTO the directory you want to change. Otherwise you're changing the entire Umbrella repo.

## After cloning our Umbrella repo, simply do this in bash from the Umbrella's root dir:

```bash
cd services/desired-repo-dir
git add file_name(s)
```

- Adds per file changes

**OR**

```bash
cd services/desired-repo-dir
git add .
```

- Adds all changes

```bash
git commit -m "What you did yuh dig"
git push origin main
```

---

---

Go back to Umbrella Repo

```
cd ../..
git add services/<service-folder>
git commit -m "chore: bump <service-name> submodule pointer"
git push
```

## Getting updates

If you want to pull the newest submodule changes to your local folder simply use the following bash command:

```bash
git pull origin main
git submodule update --init --recursive
```
