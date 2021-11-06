snap alias swi-prolog.swipl swipl
snap alias swi-prolog.swipl-win swipl-win

swi-prolog.swipl
swi-prolog.swipl-win

```
# https://wiki.archlinux.org/title/desktop_entries
# https://specifications.freedesktop.org/desktop-entry-spec/desktop-entry-spec-latest.html#recognized-keys
[Desktop Entry]
# The type as listed above
Type=Application
# The version of the desktop entry specification to which this file complies
Version=1.0
# The name of the application
Name= Prolog Terminal
# A comment which can/will be used as a tooltip
Comment=Open prolog by drubi
# The path to the folder in which the executable is run
#Path=/opt/example
# The executable of the application, possibly with arguments.
Exec=swi-prolog.swipl-win
# The name of the icon that will be used to display this entry
Icon=/home/drubico/xp.png
# Describes whether this application needs to be run in a terminal or not   
Terminal=false
# Describes the categories in which this entry should be shown
Categories=Development;
#Education;Languages;Java;

```
sudo mv Prolog_ventana.desktop /usr/share/applications/


```
# https://wiki.archlinux.org/title/desktop_entries
# https://specifications.freedesktop.org/desktop-entry-spec/desktop-entry-spec-latest.html#recognized-keys
[Desktop Entry]
# The type as listed above
Type=Application
# The version of the desktop entry specification to which this file complies
Version=1.0
# The name of the application
Name= Prolog Ventana
# A comment which can/will be used as a tooltip
Comment=Open prolog by drubi
# The path to the folder in which the executable is run
#Path=/opt/example
# The executable of the application, possibly with arguments.
Exec=swi-prolog.swipl
# The name of the icon that will be used to display this entry
Icon=/home/drubico/xp.png
# Describes whether this application needs to be run in a terminal or not   
Terminal=false
# Describes the categories in which this entry should be shown
Categories=Development;
#Education;Languages;Java;

```

sudo mv Prolog_terminal.desktop /usr/share/applications/
