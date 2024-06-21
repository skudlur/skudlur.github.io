---
title: "Why do I choose to use emacs?"
date: 2024-06-21T11:00:00+05:30
draft: false
---
## emacs

I started using emacs on a whim(pun intended hehe). I was using neovim during all my internships and I wanted to experience what emacs had to offer. I remember sending a text on the HSP Mentor chat saying, _"I think I will use emacs during the upcoming internship"_ and I was promptly challenged (and made fun off, a tad bit). There began the journey of using (imho) one of the best tools (not just a text editor).

## How did I get started?

As you can imagine, coming from vim where all the key bindings are pretty easy and straightforward, emacs posed the challenge of learning the awkward keybindings. I tried to use the man page and the GNU emacs tutorial but it only go me so far. This [playlist](https://youtube.com/playlist?list=PLEoMzSkcN8oPH1au7H6B7bBJ4ZO7BXjSZ&feature=shared) from **System Crafters** made the onboarding to emacs a bit simpler.

### Okay so, emacs is tough to get started with. What can I do to learn it faster?

In the process of figuring out emacs, there are things I wish I learned during this process to make using and customizing emacs a lot better. Here are the following:

- I wish I learned Emacs-Lisp early on. Emacs-Lisp is a dialect of Lisp (pretty much Lisp) and it is used by emacs for everything from configuration, customization and package managing. Learning this would make your emacs experience much better, much faster. Here is a reference to learn Emacs-Lisp -> [emacsdocs](https://emacsdocs.org/docs/elisp/Emacs-Lisp)
- I wish I started out on Doom Emacs when I first started to learn emacs. Doom Emacs is a heavily riced version of GNU emacs with tons of very cool features all packaged up for you to plug-and-play. Another nice thing about Doom, is that it comes with evil-mode which lets you use vim bindings as you learn the emacs bindings on the side. Here is the repository to [Doom Emacs](https://github.com/doomemacs/doomemacs) and another great emacs fork called [Spacemacs](https://github.com/syl20bnr/spacemacs).
- I wish I explored org-mode much earlier. Org files, Org agenda and everything Org on emacs is wonderful and potent. You can use it for notes, documentation and tasks and it is integrated well within emacs. Check this video by [thoughtbot](https://www.youtube.com/watch?v=SzA2YODtgK4) to get started with org-mode.

## How I use emacs?

I run Doom Emacs (with a custom configuration ofcourse) but I also my own flavour emacs that I like to call [skmacs](https://github.com/skudlur/dotfiles/tree/main/skmacs) that is (a bit) faster than Doom and has everything I need for my development work.

Here are some of the things I do from emacs:

- I write Bluespec/SystemVerilog, Rust and Python code. Emacs using ELPA/MELPA which is a large package directory and manager. You can install packages that aid your development work very easily with a click of `M+x package-install`. I use packages like `bsv-mode` (Om Shanti to the legendary Arvind), `verilog-mode`, `sv-lint`, `rustic-mode` (no LSP) and `python-mode` (no LSP) for syntax-highlighting and formatting.
- I perform git actions using `magit` which a great package to use as it makes performing commits much faster.
- Additionally, I use org-agenda (`M+x org-agenda`) to maintain tasks for myself for the day and org-mode for documentation.
- I also use `pdf-tools` to view PDFs on emacs. It's just faster to do it on Emacs instead of switching over to a browser or a file explorer.
- Occasionally, I use terminal emulators within emacs to run shell scripts or makefiles.
- I also have keybinds to perform processes I run the most. For example -> compile code, run makefiles, run simulations. You can create your own keybinds once you understand Emacs-Lisp well. 

## How I plan to use emacs in the coming years?

I will use emacs for latex and org documentation during my graduate program as I am quite comfortable at using it now. If you like Obsidian, I am sure you will love org-mode even more (but that is given, you have learned to use emacs). I would like to explore the feature of using emacs as a standalone window manager (proper neckbeard stuff right here).

## Should you use emacs?

The answer is not that simple as it depends on a few things. Do you like your text editor to be fast? Use Neovim. Do you not like customizing your text editor or having key binds? Use VSC or Espressor or Sublime Text. I would suggest emacs to users that like to do a lot of things in one place. Vim can do a lot of things emacs can do, but emacs lets you do almost everything you can do on your computer WM or DE. The level of customization and control you get over this tool is immense and if you seek such features, you would benefit from emacs.

Ending this meh blog with a quote from Tom Christiansen (Chad Perl user) - _"Emacs is a nice operating system, but I prefer UNIX"_. That should tell you a lot about what emacs actually is.
