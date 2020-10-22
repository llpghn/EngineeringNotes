# Engineering notes

## API

When there are some methods that can be brute forced, it might be a good practise to say "Yeah your registration succeed" even when it does not and to do no do the registration. So it takes longer time as when saying "Naeh, registration not good" until the attacker can start its next attack.

## Python 

SharedMemory is only limitted to binary-data or lists. This is easier in Unix and c where we can define a struct and save that in the RAM, no need to be limitted as we are it in python.

## Embedded programming best practise
In embedded programming (expecially programming MCUs) you dont want dynamic structures like lists etc. It is better to construct static structures to have all the needed memory allocated all the time. 

## Transmitting Data

When transmitting files, the byte-data have to be encoded in some way. The bytes cannot be converted directly to characters as there might be bytes that have no visible character represention or have ambilious interpretations. 
Therefore we need an Binary-to-text encoding (When the protocol only supports text). As solution might be base64 encoding, where 24 bit will be encoded in 4 characters (32-bit). By base64 6 bit are represented by an printeable character. So when using base64 the efficency is 75% (we need 32 Bit [4 chars] to transmit 24 bit). There are other encodings that have more efficency (see https://en.wikipedia.org/wiki/Binary-to-text_encoding).


