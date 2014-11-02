meteor-bones
============

Barebones scaffolding for meteor 1.0 apps

Installation
============

    git clone https://github.com/productiveme/meteor-bones.git project-name
    cd project-name
    meteor create app
    mv app/.meteor ./
    rm -rf app

Dependencies
============

[Node Version Manager](https://github.com/creationix/nvm) - Simple bash script to manage multiple active node.js versions

    curl https://raw.githubusercontent.com/creationix/nvm/v0.17.2/install.sh | bash
    source ~/.profile

[NodeJS](http://nodejs.org/) - Node.js is a platform built on Chrome's JavaScript runtime for easily building fast, scalable network applications. Node.js uses an event-driven, non-blocking I/O model that makes it lightweight and efficient, perfect for data-intensive real-time applications that run across distributed devices.
    
    nvm install stable
    n=$(which node);n=${n%/bin/node}; chmod -R 755 $n/bin/*; sudo cp -r $n/{bin,lib,share} /usr/local

[Meteor](http://www.meteor.com) - Meteor is an open-source platform for building top-quality web apps in a fraction of the time, whether you're an expert developer or just getting started.

    curl https://install.meteor.com | sh

[Coffeescript](http://coffeescript.org/) - CoffeeScript is a little language that compiles into JavaScript.

    sudo npm install -g coffee-script

[Less](http://lesscss.org) - The dynamic stylesheet language. LESS extends CSS with dynamic behavior such as variables, mixins, operations and functions.

    sudo npm install -g less

[Docco](http://jashkenas.github.io/docco/) is a quick-and-dirty documentation generator, written in [Literate CoffeeScript](http://coffeescript.org/#literate)

    sudo npm install -g docco

Various Meteor packages
    
    meteor list

Documentation
=============

Handy documentation to get familiarised with:

- [CoffeeScript Syntax](http://coffeescript.org/)
- [Meteor Docs](http://docs.meteor.com/)
- [Bootstrap3 CSS](http://getbootstrap.com/css/)
- [Mongo Manual](http://docs.mongodb.org/manual/)
- [Iron Router](https://github.com/EventedMind/iron-router/blob/0.9/DOCS.md)
- [Underscore](http://underscorejs.org/)
- [MomentJS](http://momentjs.com/docs/)
- [Font Awesome Icons](http://fortawesome.github.io/Font-Awesome/icons/)

Scaffolding
===========

### Folder structure

```
├── client
│   ├── compatibility   // 3rd party client side libraries that require global scope to work
│   ├── css             // importing and combining less files
│   │   ├── components  // component less import files
│   │   └── sites       // theme less import files
│   ├── lib             // 3rd party client side libraries that can be encapsulated
│   │   ├── helpers     // client side generic helpers
│   │   └── meteor      // client router and client startup code
│   └── views           // templates and controlling code
├── lib                 // isomorphic 3rd party libraries (client and server)
│   ├── helpers         // isomorphic generic helpers (client and server)
│   └── models          // isomorphic models to centralize database code (client and server)
├── public              // public assets
│   ├── fonts
│   └── img
└── server
        ├── api         // if an api is required
        ├── config      // server side configuration
        ├── lib         // server side 3rd party libraries
        │   └── helpers // server side generic helpers
        ├── models      // model rules
        └── publish     // publish methods
```
