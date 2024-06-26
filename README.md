<h1 align="center">AtomicGo</h1>

---

<p align="center">
<strong><a href="https://github.com/atomicgo">AtomicGo Libraries</a></strong>
|
<strong><a href="https://pkg.go.dev/github.com/atomicgo/template" target="_blank">Conventions</a></strong>
|
<strong><a href="https://github.com/atomicgo/atomicgo/blob/main/CONTRIBUTING.md" target="_blank">Contributing</a></strong>
</p>

---

<p align="center">AtomicGo is a collection of small Go libraries, which help you to code faster and more efficient!</p>

![AtomicGo](/assets/header.png?raw=true "AtomicGo")

## Clone all repos

Use this bash script to clone all atomicgo repos.  
Useful for atomicgo contributors.

```bash
#!/bin/bash

# GitHub organization name
ORG="atomicgo"

# GitHub API URL to get the list of repositories
API_URL="https://api.github.com/orgs/$ORG/repos?per_page=100"

# Fetch all repository names
repos=$(curl -s $API_URL | jq -r '.[].clone_url')

# Clone each repository
for repo in $repos; do
    git clone $repo
done
```
