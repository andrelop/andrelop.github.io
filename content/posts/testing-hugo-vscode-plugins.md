---
title: "Testing Hugo VSCode Plugins"
date: 2023-04-29T21:18:08-03:00
draft: false
---

## Testing Hugo VSCode Plugins

I'm testing VSCode plugins for [Hugo](https://gohugo.io/), which is
the static site generator solution I'm currently using.

At first, I have no interest in plugins to help with syntax highlight
or code completion. The only thing I need is a set of shortcuts for
running some Hugo commands, like starting and stopping the Hugo server,
building the site, creating new posts, etc.

A plugin I found which does all of this is **GoHugo**. I found it searching
for Hugo related plugins using VSCode's builtin plugin search functionality.

It allows you to use some Hugo commands from inside VSCode, using keyboard
shortcuts so you don't need to open a terminal.

You reach the available commands by opening VSCode's commands pallete
(which in my case opens using the `Ctrl+Shift+P` shortcut) and start
typing `hugo`.

All the existing shortcuts will be listed. Just choose the one you want
to use and the corresponding Hugo command will run.

For creating new posts, use the option `GoHugo: Create New Content`.

You can also type the shortcut cited previously and choose the option named
`GoHugo: Start Server` to start the local Hugo server.

When you have the local Hugo server running, just open [http://localhost:3000](http://localhost:3000)
in your local browser and you will get a preview of your site rendered.
This is nice to test locally first before deploying to production.

What's also really nice about this is that everytime you save the post's content
on VSCode, your browser will reload the content and you will be able to quickly
see the resuls locally.

For building the Hugo site, use the `GoHugo: Build` option. After building the site,
I just commit the changes from inside VSCode, push to GitHub and then the GitHub
Actions pipeline already created on GitHub will run and the site will be deployed
to GitHub Pages.

After you publishes your new post, use the `GoHugo: Stop Server` option to stop the
local Hugo server.