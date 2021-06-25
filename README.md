# utility-commands

## Windowns

### Tail no power shell:
````
  Get-Content <file-name> -Wait
````
## Docker
### Remover tudo relacionado ao docker-compose
````
  docker-compose down -v --rmi all --remove-orphans
````
## Git
### Stash de um único arquivo 
````
git stash push -m <stash-name> <file-name>
````
