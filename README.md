# Microfrontend Architecture in REACT.js
Illustration of how micro frontend architecture is achieved

## What are Microfrontends
Micro frontends are small apps that are individually developed and maintained and can be integrated into a main application also referred as container

## What are the ways to achieve the Microfrontend arcitecture?
There are different approaches in itegration of Microfrontends into a main application/ Container, they are catogrized into following types.

1. Build-Time integration
2. Run-Time integration

### Build Time integration
Apps are integrated into the Container before Container gets loaded into the web browser i.e at compile time (npm run builds)

one way
-> develop -> deploy -> publish (as NPM pacjkage or any other way) -> import in container as a dependency -> now the application contains all the code at build time.

PRO - easy to setup/understand

CONS - ANY time micro app changes whole application needs to be redeployed
     - Since source code is directly shared amoong apps it is tightly coupled

### Run Time integration
Microfrontend app will be loaded once the container get loaded into the browser or when the associated URL is invoked into the browser.

Process
-> develop -> deploy (deployed at container.com/microfe1) -> when user gets into container.com container is loaded -> when user gets into container.com/microfe1 the corresponding microfrontend is loaded.

PRO - can be independently deployed
    - different versions of a microfrontend can be deployed and container can choose at any point of time.

CONS - setup is complex as webpack has to be installed and has to be maintained the same accross developers

