# dockerenter Help file
## Purpose 
`dockerenter` allows to open a bash shell (or other command) in a docker container 
*without* having to run first 

`docker ps` 

and then 

`docker exec -it <container id> /bin/bash`

## Use
`dockerenter <containername>  [command]`


For example : 

```
me@myserver:~/$ dockerenter mycontainer
Entering a60ce5779859 in -w /usr/scripts ...
containeruser@mycontainer:/usr/scripts$ ▓
```

And you can use autocompletion based on the container names in docker ps! 

## Installation
### System wide  
In this folder run : 

```
   sudo cp dockerenter /usr/local/bin/
   sudo cp bash_completion /etc/bash_completion.d/dockerenter
```
and reopen terminal or simply reload bash auto-completion: 

```
   . /etc/bash_completion
```

### Single user

```
   mkdir -p ~/bin
   cp dockerenter ~/bin/
```

And if `~/bin` isn't yet in your path :

```
   echo "PATH=~/bin:$PATH" >> ~/.bashrc
```

Finally add completion : 

```
   cat bash_completion >> ~/.bash_completion
```

## Customization
You can additionally set an initial working directory when opening the container. 
To this effect, you can copy the example in the dockerenter file. 


