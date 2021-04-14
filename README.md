# Usage
The working directory inside the container defaults to `/compose`

To execute the up command directly from the host system cd into the directory containing the docker-compose.yml and enter:  
```
docker run --rm -t \
--privileged \
-v $(pwd):/compose \
-v /var/run/docker.sock:/var/run/docker.sock \
-v /usr/bin/docker:/usr/bin/docker \
wagoautomation/docker-compose -f docker-compose.yml up
```
For convinience you could create a permanent alias by adding following line in ~.profile in your host system:  
```
alias docker-compose='docker run --rm -t \
--privileged \
 -v $(pwd):/compose \
 -v /var/run/docker.sock:/var/run/docker.sock \
 -v /usr/bin/docker:/usr/bin/docker \
 wagoautomation/docker-compose'
```
and just call  
```
docker-compose -f docker-compose.yml up
```

