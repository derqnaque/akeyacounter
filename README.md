## akeyacounter - count events by hierarchical keys

Very simple application, that can be used to count events (e.g. anonymous usage of certain application features) 

### Count events

Counts events with a simple GET Request like `http://localhost:8080/count/app.cat.sub.key` .
The format is quit free but must follow URL syntax. 
The dot is reserved as a seperator between aggregation-keys and aggregation-key and leaf-key.

### Retrieve counted events

Counts can be retrieved with a simple GET Request on `http://localhost:8080/sum/app.cat.sub.key` .

Or for the aggregates with 
- `http://localhost:8080/sum/app.cat.sub` 
- `http://localhost:8080/sum/app.cat` 
- `http://localhost:8080/sum/app` 

Counter are persisted into a file, so they survive restarts.

Application is dockerized to run as a sidekick to the application that is to be measured
