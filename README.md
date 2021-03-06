It is the minor mode for editing Ruby On Rails code with Emacs. This
minor mode makes your work much easier and user friendly.


# Requirements

The emacs-rails-reloaded is requiring a 22.x or 23 (CVS) version of
Emacs, and can’t be running on old versions (less 22.0). To install
Emacs:

* For UNIX: use your package manager (typically name of package emacs,
  emacs-cvs or emacs22) or compile it from source.

* For OSX: use the "Aquameacs":http://aquamacs.org or nightly builds
  of "CVS version with Cocoa":http://atomized.org/wp-content/cocoa-emacs-nightly/
  or install using macports (name of package: emacs or emacs-app)

* For Windows: download and install "EmacsW32":http://ourcomments.org/Emacs/EmacsW32.html


# Installation

Download last release from "github project page":http://github.com/dima-exe/emacs-rails-reloaded/downloads
and unpack it to directory containing libraries of Emacs, by default it’s
`$HOME/.emacs.d/`

After that add bellow code in your the `.emacs` file:

```
  (setq load-path (cons (expand-file-name "~/.emacs.d/rails-reloaded") load-path))
  (require 'rails-autoload)
```

Next bytecompile, press `[M-x]` and type `rails/bytecompile`.


# First Acquaintance

Go to directory with your rails application and open any file in Emacs:

```
  cd $HOME/project/simple_rails_application
  emacs app/controllers/application.rb
```

There must be “RoR” sign in the list of active minor-modes in status
bar. Thi means, that emacs-rails is enabled and ready to help you in
your not so easy work.

Almost all actions are in the “RoR” menu. You can check it
out and try some of them. Don’t forget, that menu will help you only
first time. After that you better use hot keys for effective work, you
can find them in the brackets.


# Features

* Integration with script/generate, script/destroy and rake, press
  `[C-c ']` or `[C-c ;]` and type 'rake', 'gen', 'des' to display
  available tasks.

* Navigation around rails files,
  * press `[C-c ']` or `[C-c ;]` to display available files.
  * `[C-c up]` to toggle (controller|mailer) <> view.
  * `[C-c t]` to toggle test <> implementation.

  NEW NAVIGATION FEATURE:
  Press:

  * `[C-c m]` to display model list
  * `[C-c g]` to display migration list
  * `[C-c c]` to display controller list 
  * `[C-c v]` to display view list
  * `[C-c l]` to display cell list
  * `[C-c j]` to display javascript list
  * `[C-c s]` to display css styles list
  * `[C-c b]` to display library list
  * `[C-c f]` to display cucumber features list

* Support test frameworks Test::Unit and RSpec, press `[C-c C-c .]` or
  `[C-c C-c ,]` to run current test.

* Management of WEBrick/Mongrel/Thing

* Per project configuration, you can setup the default port for server,
  the environment or etc.

* Apidock.com integration, press `[C-c ']` or `[C-c ;]` and type who you
  wish find.

* Textmate like snippets.


# Links

For bugs, patches and other requests:
http://dima.lighthouseapp.com/projects/1882-emacs-rails

Google group about rails development on Emacs:
http://groups.google.com/group/emacs-on-rails
