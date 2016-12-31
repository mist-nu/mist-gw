# Mist Address Lookup Server

The Mist Address Lookup Server translates between a peer's public key and it's TOR hidden service address. It uses a REST API with two methods:

`GET /peer/`*fingerprint* returns a JSON array with the peer's TOR hidden service address and port.

`POST /peer` with the JSON array as request data and the peers public key as a client certificate. The Mist Address Lookup Server will copy the fingerprint from the client certificate.

The syntax of the JSON array is:

`[{"type":"tor","address":"`*address*`.onion","port":443}]`

Run the server with `node server.js`.

The server needs a key file and a certificate file in `./keys/`. The key file should be anmes `privkey.pem` and the certificate file `fullcert.pem`.

## Contributors

Oskar Holstensson  
Mattias Wingstedt

## Sponsor

Mist is sponsored by IIS (The Internet Foundation in Sweden). IIS finances independent, noncommercial projects that promote internet development in Sweden through the Internet Fund. Since its launch in 2004, the fund has financed over 350 projects. Private individuals and organizations are welcome to apply for financing.

## Copyright

The Mist Address Lookup Server copyright is owned by VISIARC AB.

## License

The Mist Address Lookup Server is licensed under the GNU General Public License, version 3 or later.
