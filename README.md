# proto-events

The protocol buffer definitions for DE events.

## Preparation

* Install the Protocol Buffers 3.0 compiler for your OS. Availiable at https://github.com/google/protobuf/releases/tag/v3.0.0.

* Install the Go-specific plugin. Instructions at https://developers.google.com/protocol-buffers/docs/gotutorial.

## Build Instructions

### ping

#### Go

```protoc -I=. --go_out=<go-events-repo>/ping ping.proto```

Then commit and push the generated code into the go-events repo. Substitute your own
directory when applicable.

#### Java

```protoc -I=. --java_out=<java-events-repo>/src/java ping.proto```

Then commit and push the generated code into the java-events repo.

## Message Design
```
message [MSG_NAME] {

    int64 timestamp = 10; // ms since the epoch
}
