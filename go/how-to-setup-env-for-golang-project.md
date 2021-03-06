# Guidelines regarding golang projects

This file contains guidelines to setup environment for go projects.


## Required Tools

Install the tools given below on your local machine.

|  Tools | Description  |
|---|---|
| docker | Docker is a platform for developers and sysadmins to develop, deploy, and run applications with containers [link](https://docs.docker.com/install/linux/docker-ce/ubuntu/) |
| kubectl  | Kubernetes command line tool [link](https://kubernetes.io/docs/tasks/tools/install-kubectl/) |   
| oc  | Openshift command line tool [link](https://docs.openshift.com/enterprise/3.0/cli_reference/get_started_cli.html) |   
| helm  | Package manager for kubernetes [link](https://helm.sh/) |  
| terraform | Tool to write infrastructure as code [link](https://www.terraform.io/) | 
| VS code| Code editor |
| glide | Package manager for golang [link](https://glide.sh/) |


## Visual Studio Code Extension

Add the extensions given below:
- docker
- go

## Folder Structure

Define this code structure in your home directory for golang projects:

```bash
/home/<your-username>/go/src/github.com/stakater/<repo-name>
```

For further details follow these [guidelines](https://golang.org/doc/code.html)

## Golang code practice

Follow this [tour](https://tour.golang.org/) to practice golang.


## Coding Style using github

Code comments are necessary for better code readability, so follow this [convention](https://github.com/golang/go/wiki/Comments) for adding code comments:


##  Golang CI-Lint Checker
It is a good practice to fix linting issue locally before pushing code on remote repository. Golang CI-Lint is one of the tools to do this job.

  * To Install the tool use this [link](https://github.com/golangci/golangci-lint#install).
  * To run the tool use this command but before running this command move to project root directory
  ```bash
  $ cd <you-project-folder>
  $ golangci-lint run
  ```

## Run tests locally

  * Move inside the root directory of project
  ```bash
  cd <project-directory>
  ```
  * To run all tests run the command given below:
  ```bash
  go test run ./...
  ```
  It will run all the test files by going through all folders recursively.

  * To run tests in verbose mode use the command below:
  ```bash
  go test run -v ./...
  ```
  * To run a specific test from a test cases file use the command given below:
  ```bash
  go test run -v <path to a package> -run <name of the test>
  ```
  * To check the coverage of unit tests use the command given below: 
  ```bash
  go test run  -coverprofile fmt -v <path to a package> 
  ```
