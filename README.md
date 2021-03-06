Central place for ideas and designs for MooTools Projects.

Want to help, go to the [Wiki](https://github.com/mootools/website/wiki) and add your things.

Now there is something implemented already too. To start hacking follow the steps below:

## Installation

To install everything you need to clone the repository and submodules (for the docs), install dependencies, build the documentation and run the server:

```bash
~$ git clone git://github.com/mootools/website.git
~$ cd website
~/website$ npm install
~/website$ node build/all
~/website$ node index
```

### Notes:

- Some dependencies use native C code which requires some compiler.
  - For **Mac** users this means that Xcode (Command Line Tools) should be installed.
  - For **Windows** you need *python* (2.7, and don't forget to add it you your `%PATH%`) and a C++ compiler like [Visual Studio Express](http://www.microsoft.com/visualstudio/eng/downloads#d-express-windows-desktop)

## Run it

To run it, you can either use node directly, use `forever` or use `supervisor`.

```bash
node index
```

Now the website is running on `http://localhost:3000`.

`supervisor` watches all files, while wrapup/stylus write to the `public`
folder. It is advised to use `supervisor --ignore public index`.

## Vagrant

If you don't want to install all node.js dependencies (and maybe later nginx),
you can use Vagrant to get the same setup.

Once that's done you're only a `vagrant up` away of running everything
automatically. The website should then be running on `http://localhost:5001`.

## Like to help?

* We need all websites for all projects, it needs to be easy, fast and done well.
* Like to work with cool techniques like node, express, jade and stylus?
* We also need great content and documentation.
* All pages and navigation need to be fixed
* <del>Homepage needs to be transformed into html/css according to [the design](https://github.com/mootools/website/tree/master/design)</del>
* Styling for different projects according [designs](https://github.com/mootools/website/tree/master/design)
* <del>Adding sites for other projects: wrapup, moofx, agent</del>
* Integrate the wrapup-webbuilder better
* Search (Lucene with node?)
* Overall polish
* So fork and send pull requests!

## Adding new release of project

```bash
node build/release [project] [tag]
```

this command should update the `package.json` configuration fields. After that
doing as `node build/all` will clone the repository and build docs etc.
