# mdp
> ~ preview your markdown with pleasure

It exposes an HTTP server and express middleware, with a very basic REST Api to notify the server of a particular change.

It doesn't have any watch ability, it must be done at the build process or application level.

Instead, it exposes a very simple API to notify the server that some changes have been made, then broadcasted to every livereload client connected.

Ever wanted to just spin up a quick markdown session while in your editor,
with livereload?
Or to preview how your markdown file would look like on github or npm?
Well now you can!

This readme was previewed using mdp, so you know it works. :)

## Install
```
$ npm install mdp -g
```

## Usage

It's really simple to get started with mdp. 
Assuming that you have it installed(see [Install](#install)),
all you have to do to run a file is enter a directory and run the command
with the filename:

```
$ mdp myfile.md
```

mdp handles running the servers, orchestrating changes, and livereload,
automatically. There is no need to use the livereload extension for your browser.

By default, mdp opens your file in the browser automatically.
If you wish to not do this, add the `n`/`nopen` flag:

```
$ mdp myfile.md -o
```

## Profiles

mdp offers a feature that no other markdown previewer offers — _profiles_.
This means that you can preview your file confident of how it'll look
on whatever website.
Right now, there's two different profiles:

1. __gh__: looks as if the markdown file was on github. 
This is the default profile.
2. __npm__: looks as if the markdown file was on npm.

Selecting a profile just requires adding it as an argument to the `-p` flag:

```
$ mdp myfile.md -p npm
```

I know that the profiles don't look perfect. 
Please add issues and pull requests on specific things that I should fish
If you want me to add another profile, send a pull request or an issue.