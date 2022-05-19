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
## Java
### Agrupando os dias úteis por mês
```
  import java.time.DayOfWeek;
  import java.time.LocalDate;
  import java.time.temporal.TemporalAdjusters;
  import java.util.List;
  import java.util.Map;
  import java.util.stream.Collectors;
  import java.util.stream.Stream;

  public class WorkingDays {

      public static void main(String[] args) {
          LocalDate initial = LocalDate.of(2022, 1,1);

          Map<Integer, List<LocalDate>> workingDays = Stream.iterate(initial, e -> e.plusDays(1))
          .peek(e -> {
              System.out.println(e+" => "+e.getDayOfWeek().name());
          })
          .limit(initial.with(TemporalAdjusters.lastDayOfYear()).getDayOfYear())
          .filter(day ->
              !(day.getDayOfWeek().equals(DayOfWeek.SATURDAY) || day.getDayOfWeek().equals(DayOfWeek.SUNDAY))
          ).collect(Collectors.groupingBy(LocalDate::getMonthValue));

          System.out.println(workingDays);
      }

  }
```

## Links úteis
### Ambientes local fake da AWS
[localstack](https://localstack.cloud/)
### Exemplos de sql para iniciantes
[animatesql](https://animatesql.com/)
### Acervo de banco de dados aberto 
[basedosdados](https://basedosdados.org/)
### Calculadora científica 
[geogebra](https://www.geogebra.org/calculator)



