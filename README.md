MyAdwaita - A GTK theme
=======================

My Adwaita appropriation, made with a decent amount of scorn for GNOME's
recent idiocity and yearnful longing for days when running Linux desktop
was still a fun, colorful, customizable, and empowering experience.

Aiding maintanability, the theme inherits all styles from Adwaita-Dark,
but with the following distinctions:

* reduced padding/min-size of elements like tabs and buttons,
* a more prominent keyboard/mouse focus and current window state indicator.

The theme is, time permitting, made to work with GNOME/GTK+ stack that
comes with (each) Debian stable release.


Installation
------------
Copy all files into ~/.themes/MyAdwaita.

    mkdir ~/.themes
    cd ~/.themes
    git clone https://github.com/kernc/MyAdwaita


Hacking GTK3
------------
To query `GtkSettings` (of _./gtk-3.0/settings.ini_), run:

    gtk-query-settings

To view Adwaita theme built into GTK+, run:

    gresource extract \
        /usr/lib/x86_64-linux-gnu/libgtk-3.so.0 \
        /org/gtk/libgtk/theme/Adwaita/gtk-contained-dark.css

    # Extract colors
    ... | grep -B3 define-color


To inspect GTK+ widgets' properties and styles:

    GTK_DEBUG=interactive gtk3-widget-factory