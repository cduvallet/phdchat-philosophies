# PhDChat: philosophies on coding and data for comp PhD students

You can see the talk at [cduvallet.github.io/phdchat-philosophies/](https://cduvallet.github.io/phdchat-philosophies/).

This is a talk I gave at the Alm lab summit, an annual tradition in our [lab](almlab.mit.edu) which is essentially a day-long group meeting with friends of the lab invited and lots of time for brainstorming.

It provides a very brief overview of some of the most important things I learned during and/or used to guide how I approached my work during my computational PhD.

I think I was a pretty successful student and I know I was a very happy and organized one.
I think the concepts in this presentation are largely responsible for both of those things (plus lots of friends, frisbee, and a great environment to do science in, obvs).

# Technicalities

This talk is actually just one [markdown file](docs/phdchat.md), which is converted by reveal.js into a fancy-looking presentation.

I relied heavily on [Christian Deiner](https://github.com/cdiener)'s [example presentation](https://github.com/Gibbons-Lab/ccmb_workshop)
to figure out how to make this presentation.

I installed reveal.js according to the instructions on [their repo](https://github.com/hakimel/reveal.js).

Then, I made this empty repo and copied the css, js, plugin, and lib (from the cloned reveal.js repo) directories into the directory where my `index.html` and talk (`phdchat.md`) will go.

## Making presentation in Markdown

Here, I also mostly just copied Christian's code in `index.html`.
I'm not entirely sure what all is necessary to enable the markdown, but I think most of the heavy lifting is done in the following lines:

```
<div class="slides">
    <section data-markdown="phdchat.md"
    id="markdown"
    data-separator-vertical="^\n----\n"
    data-separator-notes="^Note:"></section>
</div>
```

In this setup, three dashes (`---`) makes a new slide that goes horizontally, and four dashes (`----`) makes a new slide that goes vertically (as specified in `data-separator-vertical`).

The hardest part of getting this set up was to figure out how to enable the emojis, which I mostly figured out by trial-and-error commenting out parts of Christian's `index.html`.

## Previewing locally

You have to run a python server. From one directory above where you have your `index.html` file, run:

```
python -m SimpleHTTTPServer
```

## Hosting on a GitHub pages

Go to your repo on github.com (e.g. ([github.com/cduvallet/phdchat-philosophies](https://github.com/cduvallet/phdchat-philosophies))), click on Settings, and under the GitHub Pages heading check that yes you want this to be a github pages website.
You can choose for github to host it from the root folder of your repo, or from a `docs/` folder.
Whichever you choose, just make sure your `index.html` file is in that.
Once it's published, you'll be able to see your presentation at `<your-github-username).github.io/<your-repo-name>` (it'll also tell you where the site is published after it's done building, in a lovely green box!).
