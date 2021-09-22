[![CourseStack Frontend](https://img.shields.io/badge/Property_Listing-Backend-orange)](https://github.com/parithoshpoojary/property-listing-api/releases)

# Property Listing API

This folder includes all of the backend code that the web application requires. This was accomplished with the help of `Spring-Boot`, `Spring-Data-JPA` and `Postman` for 
testing the webservice api.

#### This folder contains the following:
1. **src** - This source folder includes all the packages and java classes that build up the backend webservice.
2. **applications.property** - includes the connector for MySQL.
3. **pom.xml** - includes all of the dependencies necessary for the web application to work properly. 

## Getting started

To get started with property-listing-api you need to obtain a binary of the property-listing-api build. It is available at the [releases](https://github.com/parithoshpoojary/property-listing-api/releases) section. You can use the jar file to directly run the application.

To run, you need to need to have Java 8 (and above) installed. It is recommended to customize the `application.properties` according to your needs and use it in the following way:

If you already have an `application.properties` file in the directory, run:

```
java -jar property-listing-api.jar
```

To use a properties file from another directory, add the full path as an argument:

```
java -jar property-listing-api.jar /.../application.properties
```

This will try to read the specified properties file based on availability. If it does fail or has missing values, the server will read from the defaults.

The properties file should also include a password column in the application.properties file, so that the connection can be made with the database.

If you'd like to build from source, follow along:

## Build Instructions

#### For building the project do the following:

#### Clone the project

```
git clone https://github.com/parithoshpoojary/property-listing-api.git
cd property-listing-api/
```

### Configuration

To choose a custom port number, etc. head over to the [application.properties](https://github.com/parithoshpoojary/property-listing-api/tree/master/src/main/resources) file in the src/main/resources/ directory and change the configuration to your preferences.

Once you are done configuring, do either of the following methods.

### Building with Maven (For developers)

If you'd like to change something on the service itself and test it on your local machine, I'd personally prefer this method since it can use your local `.m2` repository.

Build Requirements

* Java 8 or Java 11
* Apache Maven

#### Steps

If you already have maven installed in your system, you can compile the source to generate a binary.

`mvn clean package` to build the system. It will run all the tests in the project and verify everything's alright. If the tests fail, it probably is because there was no mysql database running on your machine. Turn them on and run `mvn clean package` once again. A binary will be generated at `target/`, enter the directory.

Run the generated binary with: `java -jar property-listing-api.jar`

## License
#### For more information about the license of the property-listing-api usage [click here](LICENSE)

## Contributing
To contribute to the repository, open an issue or a pull request.

For more information about spring, check their [documentation](https://docs.spring.io/spring-framework/docs/current/reference/html/).
