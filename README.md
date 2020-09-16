# TestContainers with Postgres fails with Quarkus 1.8

test-containers-173 and test-containers-18 contain the exact same code except for the Quarkus version.

As this test uses TestContainers, you need Docker up and running.
`PingPostgreSQLTest` is just a TestContainers test that pings a Postgres DB.
If you take the `@QuarkusTest` annotation out of the test, both work ok.
If not, when running different versions of Quarkus: 

* test-containers-173: Success 
* test-containers-18: Failure 

https://github.com/quarkusio/quarkus/issues/12116
