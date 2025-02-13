# Purpose : 
This script allows to open a bash shell in a container 
without having to run first `docker ps` and then `docker exec -it <container id> /bin/bash`

# Use : 
dockerenter <containername>

And bash autocompletion is available !

# Installation
## system wide  
In this folder run : 

```
   sudo cp dockerenter /usr/local/bin/
   sudo cp bash_completion /etc/bash_completion.d/dockerenter
```
and reopen terminal or simply reload bash auto-completion: 

```
   . /etc/bash_completion
```

## for single user

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


