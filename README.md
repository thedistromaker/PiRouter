# PiRouter
PiRouter aims to make a project that can make a CM4/5 into a router that can be used for light use cases.<br>  
The OS (routerPi) has three flavours:<br> 
1. routerPi LTS - This version has long-term support, with a CIP kernel, and ChromaPKG LTS.
2. routerPi Stable - This version has around 1 year of support, with an LTS kernel (like 6.12), and ChromaPKG Stable.
3. routerPi Beta - This version is a nightly build of routerPi, with the linux-next source code, and ChromaPKG Beta.<br>   
# Q&A
Q: How do I flash the OS?<br> 
A: The setup utility (written in Python3) will be released on the day of the image publication. This program will include downloading the image, and flashing the image, resizing partitions as necessary.<br>  
Q: How do I set up the OS without a video output?<br> 
A: The setup utility (which was mentioned before) will ask you if it will be fully headless, which you will then configure the installer, or if UART/Serial/HDMI/MIPI-DSI is available, for an interactive installation.<br> 
Q: When will the OS be released?<br> 
A: Good question! Currently, the OS seems like it will release in January 2026, but there isn't a specific date yet.<br> 
Q: What will be the default package manager?<br> 
A: ChromaPKG will be the default, which is currently in progress. The command will be ```chroma```, and the specific commands are listed below:<br>  
1. ```chroma -iw <packagename>``` - Installs the package from online repositories, with dependency resolution included.
2. ```chroma -il /path/to/package.cpkg``` - Installs the packahge from the specified path, with dependency resolution included.
3. ```chroma -u``` - Updates the package manager, and any packages.
4. ```chroma -r <packagename>``` - Removes the specified package.
5. ```chroma -iwr <packagename>``` - Rolls back the specified package, reading from the "published versions" document on the repo.
6. ```chroma -l clean``` - Cleans the package manager temp stores, e.g. /var/chroma/cached/zsh-3.0.6.cpkg
7. ```chroma -w update-repo``` - Updates the repositories from the update-repo utility found on the main repository.
