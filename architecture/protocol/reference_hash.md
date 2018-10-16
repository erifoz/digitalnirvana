
reference hash for the purposes of this POC is a security principle required in the implementation of digital identity.

example of using reference hash (POC):

creating 10 levels of references

reference0 - level0 reference to other system

1. perform hash function over string output of reference0 (level0 hash)
2. add reference1
3. perform hash function over string outputs of level0 hash and reference1 (level1 hash)
4. ....
5. perform hash function over string output of reference9 (level10 hash)

Use

1. to access level 10 hash, input must contain level 9 hash and reference9
2. reference is a "pin-code", reference9 proves that the user trying to access level 10 hash already knows what is in level below

Advantages:

1. it is possible to enforce access to data in such way user must prove they already know the data by providing a hash result of it
2. using hash function in this way creates multiple levels of security for potential brute force attack