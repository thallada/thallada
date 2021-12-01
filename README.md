- 💼 I work at [Outcomes4Me](https://www.outcomes4me.com/) building an app that gives breast cancer patients the knowledge, tools, and options to navigate their treatment
- ✏️ I have a blog which you can visit at [https://www.hallada.net/blog/](https://www.hallada.net/blog/)
- 📫 How to reach me: tyler@hallada.net | [@tyhallada](https://twitter.com/tyhallada) | [LinkedIn](https://www.linkedin.com/in/thallada/)
- 😄 Pronouns: he/him/his
- 🌱 I’m currently learning Rust and C++
- 💡 Interests: Rust language, game development, game mods, procedural generation, generative art, natural language processing, vim, performant web services

## Current Projects

### modmapper

Creating a database of all Skyrim mods on nexusmods.com and displaying the cells they edit on a map. Should make it easier to figure out what mods conflict with each other in the worldspace, and to find untouched areas of the map to build new mods in.

* [skyrim-cell-dump](https://github.com/thallada/skyrim-cell-dump): Library and binary for parsing Skyrim plugin files and extracting CELL data
* [modmapper](https://github.com/thallada/modmapper): (WIP) Downloads every Skyrim mod plugin from nexusmods.com and saves CELL edits of each to a database

### Bazaar Realm

A networked Skyrim mod that allows players to own shops and visit other player's shops to buy and sell items. It's a rather ambitious project so I haven't yet released anything playable.

* [BazaarRealmAPI](https://github.com/thallada/BazaarRealmAPI): API server for the mod that stores all shop data
* [BazaarRealmClient](https://github.com/thallada/BazaarRealmClient): DLL that handles requests and responses to the API
* [BazaarRealmPlugin](https://github.com/thallada/BazaarRealmPlugin): [SKSE](https://skse.silverlock.org/) plugin for the mod that modifies data within the Skyrim game engine
* [BazaarRealmMod](https://github.com/thallada/BazaarRealmMod): Papyrus scripts, ESP plugin, and all other resources for the Skyrim mod

### Advent of Code

I'm currently particpating in the [Advent of Code 2021](https://adventofcode.com/). I have also participated in several past years. I commit my daily solutions to these repos:

* [advent-of-code-2021](https://github.com/thallada/advent-of-code-2021) (Rust)
* [advent-of-code-2020](https://github.com/thallada/advent-of-code-2020) (Rust)
* [advent-of-code-2019](https://github.com/thallada/advent-of-code-2019) (Rust)
* [advent-of-code-2018](https://github.com/thallada/advent-of-code-2018) (Rust)

## Shelved Projects

This is a summary of coding side projects that I have worked on in the past but I'm not actively working on now. It's roughly sorted by most recently worked on first.

<details>
  <summary><strong>warp-caching</strong>: Testing different methods of caching with the warp web framework</summary>
  <br>
  
  [warp-caching](https://github.com/thallada/warp-caching) is an example project demonstrating a few different methods of caching with the [warp web framework](https://github.com/seanmonstar/warp) that was an offshoot of my work with the [BazaarRealmAPI](https://github.com/thallada/BazaarRealmAPI). My intention with this project is to eventually create some benchmarks of the different approaches and write a blog post about the findings. I think there is a general lack of information out there about how to handle caching in warp projects, and since I found a neat solution in my own project I wanted to share it with the rest of the community.
  <br><br>
</details>

<details>
  <summary><strong>bevy-nbody</strong>: N-body simulation using bevy and bigbang crates</summary>
  <br>
  
  [bevy-nbody](https://github.com/thallada/bevy-nbody) is a N-body simulation using the bevy and bigbang Rust crates. I developed it as a way to try out the bevy game engine after it was initially released and to figure out what that ECS thing is all about.

  It was a fun small project, but I will need to develop a proper game in bevy in the future to really understand how ECS works.

  Animating dots around the screen is a favorite past-time of mine (see [proximity-structures](https://github.com/thallada/proximity-structures)).
  <br><br>  
</details>

<details>
  <summary><strong>rust-skse-plugin</strong>: My mostly failed attempt at creating a fully-Rust SKSE plugin</summary>
  <br>
  
  [rust-skse-plugin](https://github.com/thallada/rust-skse-plugin) is my mostly failed attempt at creating a fully-Rust [SKSE](https://skse.silverlock.org/) plugin. This was an offshoot of my work on [BazaarRealmPlugin](https://github.com/thallada/BazaarRealmPlugin). I was able to successfully register the plugin with the SKSE interface, but I wasn't able to do much else due to limitations of FFI between Rust and C++ code. I intend to take another crack at this in the not-to-distant future using some of the great work that has been coming out of the [cxx](https://github.com/dtolnay/cxx) project.
  <br><br>
</details>

<details>
  <summary><strong>chela</strong>: HTML & CSS Sanitizer and Transformer</summary>
  <br>
  
  [chela](https://github.com/thallada/chela) is a HTML & CSS Sanitizer and Transformer written in Rust. chela (/ˈkiːlə/ - KEE-LUH) is a program that prunes untrusted HTML and CSS using a whitelist of rules. It is also a library for general-purpose HTML and CSS transforming that allows users to define custom functions that modify the parsed HTML tree node-by-node as it is traversed.

  I came up with the idea for chela while working at Consider (a now defunct email startup) where we were having performance issues processing thousands of HTML emails for every user in our Ruby on Rails web server. A large chunk of that processing was sanitizing the HTML emails to remove dangerous code and to transform the styling and structure of the HTML tree to match the styling of the rest of our web app that the email would be embedded in. We used the Ruby project [sanitize](https://github.com/rgrove/sanitize) for this processing and chela is heavily inspired by it. The goal of chela is to match the ease and usability of sanitize but with the performance and reliability of Rust under the hood. The browser-grade [html5ever](https://github.com/servo/html5ever) HTML parser and [rust-cssparser](https://github.com/servo/rust-cssparser) are used to parse HTML and CSS respectively.

  While it is in a useable state now, it still needs quite a bit of work before it can be relied upon in any production service. The big things left are documentation, examples using it, tests, benchmarks, and writing a blog post once that's all done to announce it to the community.
  <br><br>
</details>

<details>
  <summary><strong>icosahedron</strong>: Generates subdivided and truncated icosahedron spheres in Rust</summary>
  <br>
  
  [icosahedron](https://github.com/thallada/icosahedron) generates subdivided and truncated icosahedron spheres in Rust. I wrote a [blog post about this project that you can read on my blog](https://www.hallada.net/2020/02/01/generating-icosahedrons-and-hexspheres-in-rust.html).

  [planet](https://github.com/thallada/planet) is the sibling project which is the web frontend I developed in [regl.js](https://github.com/regl-project/regl) to display the 3D icosahedrons and hexspheres.
  
  You can see this project live at: [https://www.hallada.net/planet/](https://www.hallada.net/planet/).
  <br><br>
</details>

<details>
  <summary><strong>ferret</strong>: A rust terminal program for searching DuckDuckGo</summary>
  <br>
  
  [ferret](https://github.com/thallada/ferret) is a terminal program for searching DuckDuckGo. It was my first major project that I developed in Rust as I began to learn the language. It has some major jankiness due to limitations in the TUI library I used, so I abandoned it before I finished all of the features I wanted to add to it.

  This was a reincarnation of my [search-pane program which I wrote about in a blog post in 2013](https://www.hallada.net/2013/07/10/quick-command-line-search-search-pane.html).
  <br><br>
</details>

<details>
  <summary><strong>transport</strong>: Procedurally generated train network simulation</summary>
  <br>
  
  [transport](https://github.com/thallada/transport) is a procedurally generated train network simulation written in TypeScript.

  I didn't get very far with this project but you can see what I did at [https://transport.hallada.net/](https://transport.hallada.net/).

  The idea of this project was to create a game out of managing and building huge train networks to deliver freight and passengers. I was inspired by the train networks that I built in the video game [Factorio](https://factorio.com/), and I wanted to develop a game focused on that aspect and take it to the extreme. I may rewrite this project in Rust using the bevy framework in the future, who knows.
  <br><br>
</details>

<details>
  <summary><strong>proximity-structures</strong>: A procedurally generated and interactive animation created with PixiJS</summary>
  <br>
  
  [proximity-structures](https://github.com/thallada/proximity-structures) is a procedurally generated and interactive animation created with [PixiJS](https://www.pixijs.com).

  You can see it live at https://proximity.hallada.net/. I also wrote [a blog post about this project](https://www.hallada.net/2017/08/07/proximity-structures.html).
  <br><br>
</details>

<details>
  <summary><strong>panic-shack</strong>: Website for my Minecraft server</summary>
  <br>
  
  [panic-shack](https://github.com/thallada/panic-shack) is a little website I developed to host info about a Minecraft server that I host for friends. It features maps generated using [Minecraft Overviewer](https://overviewer.org) and a custom log stream and chat box I hacked together with some python and screen.
  <br><br>
</details>

<details>
  <summary><strong>Personal Site</strong>: Latest version of my personal website</summary>
  <br>
  
  [thallada.github.io](https://github.com/thallada/thallada.github.io) is my main website which is built with [Jekyll](https://jekyllrb.com/).

  You can see it live at [https://www.hallada.net](https://www.hallada.net).
  <br><br>
</details>

<details>
  <summary><strong>nlp</strong>: Various scripts for playing around with natural language processing/generation</summary>
  <br>
  
  [nlp](https://github.com/thallada/nlp) is a collection of python scripts I wrote while playing around with generating text using natural language processing libraries like [nltk](https://www.nltk.org/) and [spacy](https://spacy.io/).

  It also contains an IPython Notebook detailing how to generate random poems in python. I wrote a [blog post about that](https://www.hallada.net/2017/07/11/generating-random-poems-with-python.html).
  <br><br>
</details>

<details>
  <summary><strong>pi-glow</strong>: Scripts to control a strip of LPD8806 LEDs from a raspberry pi's GPIO</summary>
  <br>
  
  [pi-glow](https://github.com/thallada/pi-glow) contains scripts to control a strip of LPD8806 LEDs from a raspberry pi's GPIO.
  <br><br>
</details>

<details>
  <summary><strong>whats-open</strong>: Simple Django site displaying which dining locations are currently open on George Mason University's campus</summary>
  <br>
  
  [whats-open](https://github.com/thallada/whats-open) is a simple Django site displaying which dining locations are currently open on George Mason University's campus.

  This repo contains the original code for the project, but it has been since taken over by the student group I helped found at GMU called [SRCT](https://srct.gmu.edu/).
  <br><br>
</details>

<details>
  <summary><strong>laundry</strong>: Django site for displaying current laundry machine usage in GMU dorms</summary>
  <br>
  
  [laundry](https://github.com/thallada/laundry) is a Django site for displaying current laundry machine usage in GMU dorms. 

  It's no longer working anymore since I developed it years ago and GMU has changed their laundry systems since then. I did write a [blog post about the project](https://www.hallada.net/2013/04/09/visualizing-laundry-usage.html) though.
  <br><br>
</details>
