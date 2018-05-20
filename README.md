# Adventure Builder [![Build Status](https://travis-ci.com/tecnico-softeng/prototype-2018.svg?token=fJ1UzWxWjpuNcHWPhqjT&branch=master)](https://travis-ci.com/tecnico-softeng/prototype-2018) [![codecov](https://codecov.io/gh/tecnico-softeng/prototype-2018/branch/master/graph/badge.svg?token=OPjXGqoNEm)](https://codecov.io/gh/tecnico-softeng/prototype-2018)


To run tests execute: mvn clean install

To see the coverage reports, go to <module name>/target/site/jacoco/index.html.


|   Number   |          Name           |                       Email                      |  Name GitHUb   | Grupo |
| ---------- | ----------------------- | ------------------------------------------------ | -------------- | ----- | 
|  83446     |  Diogo Lopes Vaz        | diogo.vaz@tecnico.ulisboa.pt                     | diogolvaz      |   1   |
|  83507     |  Marcelo Regra Silva    | marcelo.filipe.regra.da.silva@tecnico.ulisboa.pt | RegSilverz     |   2   |
|  83472     |  Guilherme Nogueira     | guilherme.ramadas.nogueira@tecnico.ulisboa.pt    | Goldspy        |   3   |
|  83420     |  Alexandra Figueiredo   | alexandra.figueiredo@tecnico.ulisboa.pt          | asgcfigueiredo |   3   |
|  83443     |  Denis Voicu            | dennydenii@gmail.com                             | Smeurfy        |   2   | 
|  83520     |  Mariana Loureiro       | mfc.loureiro@sapo.pt                             | marianafcl     |   1   | 

- **Group 1:** 100Writes
- **Group 2:** 100Reads
- **Group 3:** 30Writes

### Infrastructure

This project includes the persistent layer, as offered by the FénixFramework.
This part of the project requires to create databases in mysql as defined in `resources/fenix-framework.properties` of each module.

See the lab about the FénixFramework for further details.

#### Docker (Alternative to installing Mysql in your machine)

To use a containerized version of mysql, follow these stesp:

```
docker-compose -f local.dev.yml up -d
docker exec -it mysql sh
```

Once logged into the container, enter the mysql interactive console

```
mysql --password
```

And create the 6 databases for the project as specified in
the `resources/fenix-framework.properties`.

To launch a server execute in the module's top directory: mvn clean spring-boot:run

To launch all servers execute in bin directory: startservers

To stop all servers execute: bin/shutdownservers

To run jmeter (nogui) execute in project's top directory: mvn -Pjmeter verify. Results are in target/jmeter/results/, open the .jtl file in jmeter, by associating the appropriate listeners to WorkBench and opening the results file in listener context

