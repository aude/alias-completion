alias-completion
================

If you make an alias in Bash, it's not trivial to get tab completion for it.
This project aims to make that easy.

Examples
--------

    $ source alias-completion-bash k kubectl
    $ eval "$(source alias-completion-bash k kubectl)"

Usage
-----

    usage: source alias-completion-bash <alias> <command>
    
    outputs bash completion code for alias of command.
    
    for example:
    
        $ source alias-completion-bash k kubectl
    
    to load the generated completion:
    
        $ eval "$(source alias-completion-bash k kubectl)"
    
    you could use it in ~/.bashrc, or use it in completion files.

Installation
------------

Put `alias-completion-bash` in a directory in your `$PATH`.

For example:

    # install ./alias-completion-bash /usr/local/bin/

Uninstallation
--------------

Remove `alias-completion-bash` from where you installed it.

For example:

    # rm /usr/local/bin/alias-completion-bash

Motivation
----------

Getting tab completion for a Bash alias is not trivial. That is because Bash
does not have a system for automatically doing tab completion for aliases;
Bash considers the alias an entirely separate command.

As such, the usual approach is that you have to add the tab completion for
your Bash alias yourself.

This project automates the step of finding the tab completion specification
for the upstream command, and then repurposing it for use with your alias.

Resources
---------

- https://brbsix.github.io/2015/11/23/perform-tab-completion-for-aliases-in-bash/
- https://github.com/scop/bash-completion
