# yichaoo.github.io

## 部署

### **Usage**

Add the following line to your mkdocs.yml:

```
theme:

 name: 'material'
```

Mount the folder where your mkdocs.yml resides as a volume into /docs:



Start development server on http://localhost:8000



```
docker run --rm -it -p 8000:8000 -v ${PWD}:/docs squidfunk/mkdocs-material
```

Build documentation



```
docker run --rm -it -v ${PWD}:/docs squidfunk/mkdocs-material build
```

Deploy documentation to GitHub Pages

```
docker run --name my-github-docs --restart always -dp 8210:8000 -v "%cd%":/docs squidfunk/mkdocs-material
```

```
docker run --rm -it -v ~/.ssh:/root/.ssh -v ${PWD}:/docs squidfunk/mkdocs-material gh-deploy 
```

For other installation methods, configuration options, and a demo, visit squidfunk.github.io/mkdocs-material

### with docker recommended

The official [Docker image][7] is a great way to get up and running in a few
minutes, as it comes with all dependencies pre-installed. Pull the image for the 
`latest` version with:

```
docker pull squidfunk/mkdocs-material
```

The `mkdocs` executable is provided as an entry point and `serve` is the default
command. Start the development server in your project root – the folder where
`mkdocs.yml` resides — with:

=== "Unix"

    ```
    docker run --rm -it -p 8000:8000 -v ${PWD}:/docs squidfunk/mkdocs-material
    ```

=== "Windows"

    ```
    docker run --rm -it -p 8000:8000 -v "%cd%":/docs squidfunk/mkdocs-material
    ```

### Organization and User Pages

User and Organization Pages sites are not tied to a specific project, and the
site files are deployed to the `master` branch in a dedicated repository named
with the GitHub account name. Therefore, you need working copies of two
repositories on our local system. For example, consider the following file
structure:

```
my-project/
    mkdocs.yml
    docs/
orgname.github.io/
```

After making and verifying updates to your project you need to change
directories to the `orgname.github.io` repository and call the
`mkdocs gh-deploy` command from there:

```
cd ../orgname.github.io/
mkdocs gh-deploy --config-file ../my-project/mkdocs.yml --remote-branch master
```

```
cd ../site/
mkdocs gh-deploy -f ../mkdocs/mkdocs.yml -b master
```
Note that you need to explicitly point to the `mkdocs.yml` configuration file as
it is no longer in the current working directory. You also need to inform the
deploy script to commit to the `master` branch. You may override the default
with the [remote_branch] configuration setting, but if you forget to change
directories before running the deploy script, it will commit to the `master`
branch of your project, which you probably don't want.

Be aware that you will not be able to review the built site before it is pushed
to GitHub. Therefore, you may want to verify any changes you make to the docs
beforehand by using the `build` or `serve` commands and reviewing the built
files locally.

!!! warning

    You should never edit files in your pages repository by hand if you're using
    the `gh-deploy` command because you will lose your work the next time you
    run the command.
