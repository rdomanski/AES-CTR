AES-CTR
=======

Python implementation of AES encryption algorithm in counter mode. 

Script bases on the python Crypto library. This version supports 128 bit key only.

$ aes-ctr.py --help
usage: aes-ctr.py [-h] [-d] -i IN [-o OUT] -k KEY -iv IV [-v]

AES implementation in counter mode. This version supports 128 bits key
encryption only. This is experimental script. NO INPUT VALIDATION

optional arguments:
  -h, --help            show this help message and exit
  -d, --decrypt         Use decrypt instead of default encrypt
  -i IN, --input IN     File containing plaintext/ciphertext
  -o OUT, --output OUT  Output file to store result of the program
  -k KEY, --key KEY     Encryption 128bits key
  -iv IV                Initial 128 bits counter
  -v, --version         show program's version number and exit

Exemplary usage:

1) Encryption

$ python aes-ctr.py -i plaintext -o ciphertext -k abcdef1234567890abcdef1234567890 -iv 01010101010101010101010101010101

2) Decryption

$ aes-ctr.py -d -i ciphertext -o plaintext -k abcdef1234567890abcdef1234567890 -iv 01010101010101010101010101010101
