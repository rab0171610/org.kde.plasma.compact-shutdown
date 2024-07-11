# org.kde.plasma.compact-shutdown-KF6
Compact Shutdown Widget for Plasma 6

I have ported the compact-shutdown plasmoid to KF6. The icons in the widget (shutdown, reboot, etc.) are now sourced from the users default icon theme.
If you are using the default Breeze theme, the icons will likely appear as they always have. This is a change made in Plasma 6 and not in the widget itself.  
The size of the widget is resizable -- it is no longer defined in the qml code. If you want to increase 
or decrease the size of the panel you should be able to drag the edges of the expanded widget to the size you desire.  
The functions had to be changed as KSMserver options used in the previous version no longer work in KDE 6.
The functions for logout, reboot, and shutdown are now coded to use 'qdbus6 org.kde.Shutdown /Shutdown' commands.
In limited tests in a KDE 6 virtual machine, these appeared to work as they always did. 

I believe most of the work is done that allows this widget to function as it always did in KDE 5, however it is a work in progress.  I will be updating the credits eventually. If there are any issues while testing this, please let me know.
To test this plasmoid, download the code and copy the parent directory (org.kde.plasma.compact-shutdown-KF6) to ~/.local/share/plasma/plasmoids. If this directory does not exist, create it.  
'ls ~/.local/share/plasma/plasmoids' should return:
org.kde.plasma.compact-shutdown-KF6

Full path should be:
~/.local/share/plasma/plasmoids/org.kde.plasma.compact-shutdown-KF6

Logout and log in again.  The widget should now appear in the available widgets list when adding widgets to the panel or the desktop.

Please download the KF6 release to try it out.
