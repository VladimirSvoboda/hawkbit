Build: [![Circle CI](https://circleci.com/gh/eclipse/hawkbit.svg?style=svg)](https://circleci.com/gh/eclipse/hawkbit)

# Eclipse.IoT hawkBit - Update Server

[hawkBit](https://projects.eclipse.org/projects/iot.hawkbit) is an domain independent back end solution for rolling out software updates to constrained edge devices as well as more powerful controllers and gateways connected to IP based networking infrastructure.

# Documentation

see [hawkBit Wiki](https://github.com/eclipse/hawkbit/wiki)

# Contact us

* Want to chat with the team behind hawkBit? [![Join the chat at https://gitter.im/eclipse/hawkbit](https://badges.gitter.im/eclipse/hawkbit.svg)](https://gitter.im/eclipse/hawkbit?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge&utm_content=badge)
* Having issues with hawkBit? Open a [GitHub issue](https://github.com/eclipse/hawkbit/issues).
* You can also check out our [Project Homepage](https://projects.eclipse.org/projects/iot.hawkbit) for further contact options.

# hawkBit sandbox

We offer a sandbox installation that is free for everyone to try out hawkBit. However, keep in mind that the sandbox database will be reset from time to time. It is also not possible to upload any artifacts into the sandbox. But you can use it to try out the Management UI, Management API and DDI API.

https://hawkbit.eu-gb.mybluemix.net/UI/

# Compile, Run and Getting Started

We are not providing an off the shelf installation ready hawkBit update server. However, we recommend to check out the [Example Application](examples/hawkbit-example-app) for a runtime ready Spring Boot based update server that is empowered by hawkBit. In addition we have [guide](https://github.com/eclipse/hawkbit/wiki/Run-hawkBit) for setting up a complete landscape.

#### Clone and build hawkBit
```
$ git clone https://github.com/eclipse/hawkbit.git
$ cd hawkbit
$ mvn clean install
```
#### Start hawkBit example app
[Example Application](examples/hawkbit-example-app)
```
$ java -jar ./examples/hawkbit-example-app/target/hawkbit-example-app-#version#.jar
```
#### Start hawkBit device simulator
[Device Simulator](examples/hawkbit-device-simulator)
```
$ java -jar ./examples/hawkbit-device-simulator/target/hawkbit-device-simulator-#version#.jar
```
#### Generate Getting Started data
[Example Management API Client](examples/hawkbit-mgmt-api-client)
```
$ java -jar ./examples/hawkbit-mgmt-api-client/target/hawkbit-mgmt-api-client-#version#.jar
```

# Releases and Roadmap

* We are currently working on the first formal release under the Eclipse banner: 0.1 (see [Release 0.1 branch](https://github.com/eclipse/hawkbit/tree/release-train-0.1)).
* The master branch contains future development towards 0.2. We are currently focusing on:
  * Rollout Management for large scale rollouts.
  * Clustering capabilities for the update server.
  * Upgrade of Spring Boot and Vaadin depedencies.
  * And of course tons of usability improvements and bug fixes.


# Modules
`hawkbit-core` : core elements.  
`hawkbit-security-core` : core security elements.  
`hawkbit-security-integration` : security integration elements to integrate security into hawkbit.  
`hawkbit-artifact-repository-mongo` : artifact repository implementation to mongoDB.    
`hawkbit-autoconfigure` : spring-boot auto-configuration.  
`hawkbit-dmf-api` : API for the Device Management Integration.  
`hawkbit-dmf-amqp` : AMQP endpoint implementation for the DMF API.  
`hawkbit-repository` : repository implemenation based on SQL for all meta-data.    
`hawkbit-http-security` : implementation for security filters for HTTP.    
`hawkbit-rest-api` : API classes for the REST Management API.  
`hawkbit-rest-resource` : HTTP REST endpoints for the Management and the Direct Device API.  
`hawkbit-ui` : Vaadin UI.  
`hawkbit-cache-redis` : spring cache manager configuration and implementation with redis, distributed cache and distributed events.
