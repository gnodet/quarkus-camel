# quarkus-camel

Simple Quarkus + Camel demo

## Java mode

Run `mvn package`.

Launch with `java -jar target/my-artifactId-my-version-runner.jar`

## Native mode

Run `mvn package -Pnative`. Note that the native part build is quite long and cpu intensive...

Launch with `./target/my-artifactId-my-version-runner`.  

You'll have the following output
```
2019-03-12 08:36:17,187 INFO  [io.qua.cam.cor.run.CamelRuntime] (main) Apache Camel 3.0.0-M1 (CamelContext: quarkus-camel-example) is starting
2019-03-12 08:36:17,188 INFO  [io.qua.cam.cor.run.CamelRuntime] (main) confPath: 
2019-03-12 08:36:17,188 INFO  [io.qua.cam.cor.run.CamelRuntime] (main) confDPath: 
2019-03-12 08:36:17,188 INFO  [io.qua.cam.cor.run.CamelRuntime] (main) routesUri: 
2019-03-12 08:36:17,188 INFO  [io.qua.cam.cor.run.FastCamelContext] (main) Route: timer started and consuming from: timer://keep-alive
2019-03-12 08:36:17,189 INFO  [io.qua.cam.cor.run.FastCamelContext] (main) Route: file started and consuming from: file://./target/orders
2019-03-12 08:36:17,189 INFO  [io.quarkus] (main) Quarkus 0.11.0 started in 0.008s. 
2019-03-12 08:36:17,189 INFO  [io.quarkus] (main) Installed features: [camel-core, cdi]
2019-03-12 08:36:18,190 INFO  [keep-alive] (Camel (quarkus-camel-example) thread #0 - timer://keep-alive) Exchange[ExchangePattern: InOnly, BodyType: String, Body: I'm alive !]
2019-03-12 08:36:19,196 INFO  [keep-alive] (Camel (quarkus-camel-example) thread #0 - timer://keep-alive) Exchange[ExchangePattern: InOnly, BodyType: String, Body: I'm alive !]
```
