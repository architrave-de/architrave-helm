# architrave-helm
## General
This repo is holding architrave helm charts for Kubernetes deployment.
For the reason of how github pages works the repository is public and accessable for everyone. For that reason make sure all published helm charts contain no private information, secrets, certificates or passwords before commiting.

## Before publishing to repo
1. cd to the parent of the chart you like to publish, lets say you like to publish `folder1/chart1/` you should cd `folder1`
2. package the chart by running `helm package chart1`. The result will be a `chart1-{version from chrt}.gz` file

## How to use this repository
To update the repository with new charts and chart versions
1. Clone the repository to your local machine by running  `git clone git@github.com:architrave-de/architrave-helm.git`
2. `cd architrave-helm`
3. Checkout `gh-pages` branch by running `git checkout gh-pages`
4. Copy `chart1-{version from chrt}.gz` to the root of the the repo
5. To update the `index.yaml` file, run `helm repo index . --merge index.yaml --url https://architrave-de.github.io/architrave-helm/`
6. Commit the changes by running `git commit -a -m "Added chart1-{version from chrt}"`
7. Push the changes `git push`

## Using the helm repo
To make the helm charts available on kubernetes run `helm repo add architrave-helm https://architrave-de.github.io/architrave-helm/`
