bash-alias-completion
=====================

If you make an alias in Bash, it's not trivial to get Bash completion for it.
This project aims to make that easy.

Examples
--------

    $ source bash-alias-complete k kubectl
    $ eval "$(source bash-alias-complete k kubectl)"

Usage
-----

    usage: source bash-alias-completion <alias> <command>
    
    outputs Bash completion code for alias of command.
    
    for example:
    
        $ source bash-alias-completion k kubectl
    
    to load the generated completion:
    
        $ eval "$(source bash-alias-completion k kubectl)"
    
    you could use it in ~/.bashrc, or use it in completion files.

Installation
------------

Put `bash-alias-completion` in a directory in your `$PATH`.

For example:

    # install ./bash-alias-completion /usr/local/bin/

Uninstallation
--------------

Remove `bash-alias-completion` from where you installed it.

For example:

    # rm /usr/local/bin/bash-alias-completion

Motivation
----------

Getting Bash completion for an alias is not trivial. That is because Bash does
not have a system for automatically doing Bash completion for aliases; it
considers the alias an entirely separate command.

As such, the usual approach is that you have to add the Bash completion for
your alias yourself.

This project automates the step of finding the Bash completion for the upstream
command, and then repurposing it for use with your alias.

Resources
---------

- https://brbsix.github.io/2015/11/23/perform-tab-completion-for-aliases-in-bash/
- https://github.com/scop/bash-completion
