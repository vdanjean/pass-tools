# pass-tools

Tools to manage (lots of) passwords

## Dependencies

On Debian you might need to install the Path::Class perl module:

    sudo apt-get install libpath-class-perl

## Configuration

Although createpass can be used without configuration file, we provide a
sample configuration file with the default each parameters set to the default
value, copy it to your xdg configuration directory (usually `~/.configs`)
and then edit it:

    mkdir -p ~/.config/passtools
    cp config.rc ~/.config/passtools

One of the main advantages of this configuration file is that it allow you to
define a lists of usernames, domains and info that you can use for completion
in th createpass prompt.

Completion is done using the perl [Term::Complete](http://perldoc.perl.org/Term/Complete.html)
module:

+ `<tab>` Attempts word completion. Cannot be changed.
+ `^D` Prints completion list.
+ `^U` Erases the current input.
+ `<del>`, `<bs>` Erases one character.
