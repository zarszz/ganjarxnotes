---
layout: category-post
title: "Debugging Ruby On Rails Application With Visual Studio Code"
date: 2020-03-22
categories: tutorial
---
# Debug RoR applications with VSCODE

> Requirement
>
> ruby version    >= 2
>
> rails version   >= 5

## Installing ruby-debug-ide and debase gem

```console
  $~ gem install ruby-debug-ide
  $~ gem install debase
```

## Add ruby-debug-ide and debase in our projects

Open your gemfile and add 2 lines below in your development group
```Gemfile
  gem 'ruby-debug-ide'
  gem 'debase'
```

Running bundle install

```console
  $~ bundle install
```

## Add this configuration to launch.json

 To get PATH_TO_BUNDLER we can use command below

```console 
   $~ whereis bundle 
```

 Same as above, to get PATH_TO_RDEBUG_IDE we can use command below

```console
  $~ whereis rdebug-ide
```

 After that, we can add to launch configuration

```json
        {
            "name": "Debug Rails server",
            "type": "Ruby",
            "request": "launch",
            "cwd": "${workspaceRoot}",
            "useBundler": true,
            "pathToBundler": "PATH_TO_BUNDLER",
            "pathToRDebugIDE": "PATH_TO_RDEBUG_IDE",
            "program": "${workspaceRoot}/bin/rails",
            "args": [
                "server",
                "-p",
                "3000"
            ]
        }
```
