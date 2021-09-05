# Tutorial

### Fork the repo

![Click this button in GitHub](.gitbook/assets/2021-09-05-at-11.10.47.png)

### Clone your fork and install the project locally

At the command line:

```text
git clone <url-to-your-fork-of-helpafamily-here>
cd helpafamily/
cp .env.example .env
yarn install
```

### Set up your upstream remote

In your .git/config, add these 3 lines:

```text
[remote "upstream"]
        url = https://github.com/margaritahumanitarian/helpafamily-manual.git
        fetch = +refs/heads/*:refs/remotes/upstream/*
```

