# bpulse-protobuf-php

bpulse-protobuf-php is the model interface which bpulse relies on in order to send messages with pulses to the collector, it is a mandatory dependency of bpulse-sdk-php in order to compile it and send messages to the collector.

## Requirements

In order to build this project you need to install protoc on your machine, it is very important that you use specifically the 2.6.1 version otherwise the project might not compile.

The instructions for each OS are the following:

### Windows

Use the provided distribution in this repository under /protobuf/windows/protoc-2.6.1-win32.rar unpack it wherever you want. Edit your environment variables adding one that points to the unpackaged folder like PROTOC_HOME

```sh
e.g. PROTOC_HOME=C:\software\protoc
```

Then edit your PATH variable appending the new variable

```sh
e.g. PATH=[other_variables];%PROTOC_HOME%
```

You can check if the installation was ok by opening a terminal and executing the following command:

```sh
protoc --version
```

You should see this output:

```sh
libprotoc 2.6.1
```

### Linux

Use the provided distribution in this repository under /protobuf/linux/protobuf-2.6.1.tar.gz unpackit wherever you want.

Note: At this point you should have installed the two linux packages mentioned above.

Open a terminal and go to where you unpacked the file, then execute the following commands (one by one):

```sh
$ ./autogen.sh
$ ./configure
$ ./make
$ ./make install
```

Note: The make install commad may require sudo

After that, you can check if everything succeded by executin the command:

```sh
$ protoc --version
```

If you don't receive a message like:

```sh
libprotoc 2.6.1
```

Then execute the following:

```sh
$ sudo ldconfig
```

## Build

Once you checked out the sources, in a terminal go to the bpulse-protobuf-php folder  and type

```sh
$ make build
```

It's done!, now you can use the bpulse-sdk-php

## License

The Bpulse Protobuf PHP is licensed under the Apache License 2.0. Details can be found in the LICENSE file.