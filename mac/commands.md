# Copy & Paste
The clipboard in OS X is a.k.a. pasteboard. And there're two commands.
* `pbcopy` copies whatever is passed to it.

        echo -n 'foo' | pbcopy
    This will copy "foo" into your clipboard.

* `pbpaste` pastes the previous copied content.

        pbpaste > temp
    This will paste "foo" into file temp.
