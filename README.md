##Install

	npm install apns_test -g

##Usages

	apns_test your_token development|production cert_key_path private_key_pem [Message]

##Example

	apns 094f11604aa8fddb85c3cef4fd6e30dd42389b45d717113a0d922ee8f4ceb788 development ./cert.pem ./key.pem "Testing APNS"

##Generate Key

Download **.cer** file from Apple Development.

	$openssl x509 -in cert.cer -inform DER -outform PEM -out cert.pem

Open Keychain Access and select push notification certificate and private key. Right Click export.

![keychain export](http://d.pr/i/y1Mb+)

Chose .p12 File Format Extension.

	$openssl pkcs12 -in key.p12 -out key.pem -nodes