---
title: Node.js
tags: nodejs, languages
category: Languages and Frameworks
---

# Node.js
We use **nvm** to manage different node versions. We read the node version you set in your **package.json** and install the appropriate one.

## Default Version
The default version when we can't find a setting in your package.json is ```0.10.22```

## Set it in Setup commands
You can of course always set it directly through the setup commands by running

~~~shell
nvm install NODE_VERSION
nvm use NODE_VERSION
~~~

## Preinstalled versions
We install the latest versions for ```0.8.x , 0.9.x , 0.10.x and 0.11.x```

## Npm
You can use npm to install your dependencies. We set the **PATH** to include the **node_modules/.bin** folder so all executables installed through npm can be run

## Tools and Test frameworks
You can use all test frameworks or tools including karma, mocha, grunt or any other node based tool. Make sure you install the first through npm. Use the same commands you are using on your own system to start your tests, for example:

~~~shell
grunt test
~~~
