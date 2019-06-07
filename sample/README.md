# ThinWAR Example

The ThinWAR microservice was created with: [Java EE 8 Essential Archetype](http://www.adam-bien.com/roller/abien/entry/java_ee_8_essentials_archetype)
1. Install the builder image: [https://github.com/AdamBien/s2i-payara](https://github.com/AdamBien/s2i-payara)
2. `oc new-app s2i-payara:latest~/. --name=thin`
3. `oc start-build --from-dir . thin`
4. `oc expose svc thin --port=8080`

The service is going to be accessible under: 

`http:/[GENERATED_HOST or DNS]/thin/resources/ping`