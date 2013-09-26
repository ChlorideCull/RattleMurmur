RattleMurmur - The alternative Murmur (which doesn't need xorg)
====================================

RattleMurmur is an alternative Mumble Server, based of uMurmur (which doesn't need xorg either).

Instructions for building from source
-------------------------------------
1. Requirements
	* [OpenSSL](http://www.openssl.org/) or [PolarSSL](http://polarssl.org/) library. For PolarSSL version 1.0.0 and above is required.
	* [libconfig](http://www.hyperrealm.com/libconfig/)
	* [libprotoc-c](http://code.google.com/p/protobuf-c/) version 0.14 or 0.15 (use --disable-protoc option in its ./configure to build only the library). If you for some reason have to run an earlier version you need to recompile the protocol file `Mumble.proto` using the protobuf compiler for the corresponding version.

2. Build
	* `cmake`

3. Install
	* `cmake install`
	* Edit rmurmur.conf.example to your liking and put it in a suitable place. /etc/rmurmur.conf is default.

4. Run `rmurmurd -c <conf file> -p <PID file> -r`. For other switches and their meaning run `umurmurd -h`

A startup script can easily be created if you want to. Just copy an existing script and edit it to your liking.
