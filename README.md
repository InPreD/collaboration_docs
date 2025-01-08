# collaboration_docs 👥💬

how to develop tools and services in collaboration with other inpred nodes

## Communication channel 📫

Our current channel of communication is the email list. We should try to set up a more direct channel of communication such as slack, gather, mattermost or teams. By means of the communication channel, we should share biweekly updates on projects regarding all nodes; preferably, a list with ongoing projects and a short comment or just "none" if nothing has happened. This will ensure that everyone is up to date and knows what is going on - anything that is handled through PRs can be omitted as people get notified anyways.

## Project planning 🗓️

Prior to starting a new project, a short meeting with at least one representative of each node (option to opt out) to discuss and plan the new tool or service should be held. This meeting can be referred to as the scoping meeting which will define the scope of the project where we can discuss the following:

- purpose
- language (default: python)
- interface (e.g. command line interface, web server)
- involved collaborators (which nodes have resources to contribute)
- deployment options (e.g. baremetal, docker/apptainer)
- integration with existing projects
- license (default: GNU AFFERO GENERAL PUBLIC LICENSE - Version 3)
- intended timeline

## Development 🔧

1. Code should be made available through [inpred group on github](https://github.com/InPreD).
2. Start off by creating a repository with an empty `README.md` and `LICENSE` file, clone it to your local environment and then start developing.
3. Use the agreed branching strategy (suggested: [simplified Gitflow workflow](https://inpred.github.io/24-03_bioinfo_ws/#22)).
4. Commit and push changes early and often to allow others to follow along.
5. Follow best practices for the selected programming language. Generally recommended are unit testing (cover test cases from different nodes), keeping functions short, avoid hard-coding, sensible use of packages and libraries.
6. Use [git commit message conventions](https://inpred.github.io/24-03_bioinfo_ws/#19).
7. Keep the features and PRs small (ideally one PR per feature) to have a tight feedback loop. Focus on one small problem for one feature. Include at least one representative from each node (option to opt out) and set a deadline (e.g. two weeks).
8. Pair-programming should be used where it makes sense to enable knowledge and expertise transfer between the different groups.
9. Use [github actions](https://inpred.github.io/24-03_bioinfo_ws/#24) to test, lint and publish or build your project.
10. Provide at least a docker image (can be converted to apptainer) and push them to the [inpred group at docker hub](https://hub.docker.com/u/inpred).
11. Write documentation and check with others that it is understandable.
12. [Tag and release](https://inpred.github.io/24-03_bioinfo_ws/#52) code that is ready for production using semantic versioning.

The goal should be to write code that can be used directly by any node - refactor anything necessary and make things (e.g. filepaths, templates, node-specific variables) configurable where necessary.

### Python 🐍

[Here](https://inpred.github.io/24-03_bioinfo_ws/#72) are some of the best practices for python.

## Issue and bug handling 🐞

Any issues and bugs should be reported on github and then handled there to have the discussion and code fixing tightly linked. This enables us to easily find previous problems, share knowledge and track the development process.
