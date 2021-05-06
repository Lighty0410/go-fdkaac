# go-fdkaac

fork from lib-fdkaac(https://github.com/izern/fdk-aac)

## Usage

First, get the source code:

```
go get -d github.com/izern/go-fdkaac
```

Then, compile the fdk-aac:

```
cd $GOPATH/src/github.com/izern/go-fdkaac &&
tar -zxvf fdk-aac-2.0.0.tar.gz && 
cd fdk-aac-2.0.0/ && ./configure --prefix=/usr/local/fdk-aac-2.0.0 && make && make install &&
cd ..
```

Done, import and use the package:

* [ExampleAacDecoder_RAW](fdkaac/example_test.go#L29), decode the aac frame to PCM samples.
* [ExampleAacEncoder_LC](fdkaac/example_test.go#L316), encode the PCM samples to aac frame.
* [audio resample](https://github.com/izern/go-aresample).

There are an example of AAC audio packets in ADTS:

* [avatar aac over ADTS](doc/adts_data.go), user can use this file to decode to PCM then encode.

To run all examples:

```
cd $GOPATH/src/github.com/izern/go-fdkaac && go test ./...
```

Winlin 2016
