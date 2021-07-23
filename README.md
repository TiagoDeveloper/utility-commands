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
## Docker windows wsl
### WSL 2 should automatically release disk space back to the host OS
````
  wsl --shutdown
  optimize-vhd -Path C:\Users\<user-machine>\AppData\Local\Docker\wsl\data\ext4.vhdx -Mode full
````
## Git
### Stash de um único arquivo 
````
git stash push -m <stash-name> <file-name>
````

## Linux
### Zip pasta local selecionando ou com todos os arquivos, mantendo o nome da pasta
```
zip -r "$(basename $(pwd)).zip" <N... names or . (all)>
```
