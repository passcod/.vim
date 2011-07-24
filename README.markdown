pathogen.vim
============

Manage your `'runtimepath'` with ease.  In practical terms, pathogen.vim
makes it super easy to install plugins and runtime files in their own
private directories.

Usage
-----

Install to `~/.vim/autoload/pathogen.vim`
(`~\vimfiles\autoload\pathogen.vim` on Windows, and that pattern applies
to the paths below, too), and add this to your vimrc:

    call pathogen#infect()

Now any plugins you wish to install can be extracted to a subdirectory
under `~/.vim/bundle`, and they will be added to the `'runtimepath'`.
Observe:

    cd ~/.vim/bundle
    git clone git://github.com/tpope/vim-fugitive.git

Now [fugitive.vim](https://github.com/tpope/vim-fugitive) is installed.
If you really want to get crazy, you could set it up as a submodule in
whatever repository you keep your dot files in.  I don't like to get
crazy.

Normally to generate documentation, Vim expects you to run `:helptags`
on each directory with documentation (e.g., `:helptags ~/.vim/doc`).
Provided with pathogen.vim is a `:Helptags` command that does this on
every directory in your `'runtimepath'`.  If you really want to get
crazy, you could even invoke `Helptags` in your vimrc.  I don't like to
get crazy.

If you're one of those OCD types that insists pathogen.vim live in
`~/.vim/bundle` like every other plugin, you can do that if you add an
extra line to your vimrc:

    source ~/.vim/bundle/vim-pathogen/autoload/pathogen.vim

Finally, pathogen.vim has a rich API that can manipulate `'runtimepath'`
in ways most people will never need to do.  If you're one of those edge
cases, look at the source.  It's well documented.

Contributing
------------

If your [commit message sucks](http://stopwritingramblingcommitmessages.com/),
I'm not going to accept your pull request.  I've explained very politely
dozens of times that
[my general guidelines](http://tbaggery.com/2008/04/19/a-note-about-git-commit-messages.html)
are absolute rules on on my own repositories, so I may lack the energy
to explain it to you yet another time.  And please, if I ask you to
change something, `git commit --amend`.

Beyond that, don't be shy about asking before patching.  What takes you
hours might take me minutes simply because I have both domain knowledge
and a perverse knowledge of VimScript so vast that many would consider
it a symptom of mental illness.  On the flip side, some ideas I'll
reject no matter how good the implementation is.  "Send a patch" is an
edge case answer in my book.

Self-Promotion
--------------

Like pathogen.vim?  Follow the repository on
[GitHub](http://github.com/tpope/vim-pathogen) and vote for it on
[vim.org](http://www.vim.org/scripts/script.php?script_id=2332).  And if
you're feeling especially charitable, follow tpope on
[Twitter](http://twitter.com/tpope) and
[GitHub](http://github.com/tpope).