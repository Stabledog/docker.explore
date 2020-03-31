## taskrc.md

```bash

docker_projname=v1

function docker-comp {
    #Help general docker-compose wrapper
    command docker-compose -p $docker_projname "$@"
}

alias dc='docker-comp'
#Help
alias dcup='docker-comp up'
#Help

function docker-shell {
    #Help shell to one of the services:
    local srvname=${1:-gobuild}
    docker-comp exec $srvname bash
}

alias dsh='docker-shell'
#Help

```
 7273  2020-03-31 05:19:02 docker-compose up -p v1
 7274  2020-03-31 05:20:20 docker-compose exec v1_gobuild_1 ash
 7276  2020-03-31 05:20:42 docker-compose -p v1 exec gobuild ash
 7277  2020-03-31 05:20:48 docker-compose -p v1 exec gobuild bash
 7278  2020-03-31 05:19:52 docker-compose -p v1 up
