# Why are there two scripts for ENIGMA-CNV project?
The original scripts were made to run Freesurfer on Mac/Linux operating system. So, there were some errors when these scripts were run on other operating systems.

These files on the GitHub repository will come in handy if you are running Freesurfer on the windows operating system. So, if you are running Freesurfer on Mac/Linux operating system then you must use the original scripts.  

Freesurfer is an application that is made for Mac operating system, so if you want to run it on windows, you have to run it in a docker container. Download the docker desktop from this URL: (https://www.docker.com/products/docker-desktop/). 

To run these scripts on windows you have to download Gitbash from the URL: (https://git-scm.com/download/win). And then run these scripts through Gitbash. 

The original shell scripts were not running on the windows computer, as they were made on a mac operating system. So, some changes were to be made. First, we had to add winpty, it is a windows-based software package that provides an interface similar to Unix. The syntax for binding was changed by adding an extra slash (/) in the command after usr, to make it functional in windows. The following is an example for the two changes that were made. 

#### The original script: 
##### docker exec -it -w /usr/local/freesurfer/myfiles enigma-cnv-freesurfer sh 1a_enigma_runfreesurfer_loop.sh /usr/local/freesurfer/myfiles
## The changed script: 
### winpty docker exec -it -w //usr/local/freesurfer/myfiles enigma-cnv-freesurfer sh 1a_enigma_runfreesurfer_loop.sh //usr/local/freesurfer/myfiles

We had to choose an EOL conversion to finish making the scripts Unix friendly by using the Unix(LF) option in Notepad ++. Once this is done, the scripts are ready to be used with Windows. 
