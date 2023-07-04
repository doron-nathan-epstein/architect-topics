# Hashing

![Hashing](https://www.thesslstore.com/blog/wp-content/uploads/2018/12/Hashing-Example-768x369.png)

## Definition

Hashing is the process of transforming any given key or a string of characters into another value. This is usually represented by a shorter, fixed-length value or key that represents and makes it easier to find or employ the original string.

## Notes

- The most popular use for hashing is the implementation of hash tables. A hash table stores key and value pairs in a list that is accessible through its index. Because key and value pairs are unlimited, the hash function will map the keys to the table size. A hash value then becomes the index for a specific element.
- A hash function generates new values according to a mathematical hashing algorithm, known as a hash value or simply a hash. To prevent the conversion of hash back into the original key, a good hash always uses a one-way hashing algorithm.
- Hashing is relevant to **but not limited to** data indexing and retrieval, digital signatures, cybersecurity and cryptography. 

## Common Hashing Algorithms

- **MD4** - MD4 is a self-loathing hash algorithm, created in 1990, even its creator, Ronald Rivest, admits it has security problems. The 128-bit hashing algorithm made an impact though, it’s influence can be felt in more recent algorithms like WMD5, WRIPEMD and the WHSA family.
- **MD5** - MD5 is another hashing algorithm made by Ray Rivest that is known to suffer vulnerabilities. It was created in 1992 as the successor to MD4. Currently MD6 is in the works, but as of 2009 Rivest had removed it from NIST consideration for SHA-3.
- **SHA** - SHA stands for Security Hashing Algorithm and it’s probably best known as the hashing algorithm used in most SSL/TLS cipher suites. A cipher suite is a collection of ciphers and algorithms that are used for SSL/TLS connections. SHA handles the hashing aspects. SHA-1, as we mentioned earlier, is now deprecated. SHA-2 is now mandatory. SHA-2 is sometimes known has SHA-256, though variants with longer bit lengths are also available.
- **RIPMED** - A family of cryptographic hashing algorithms with a lengths of 128, 160, 256 and 320 bits. It was developed under the framework of the EU’s Project Ripe by Hans Dobbertin and a group of academics in 1996. Its 256 and 320 bit variants don’t actually add any additional security, they just diminish the potential for a collision. In 2004 a collision was reported for RIPEMD-128, meaning RIPEMD-160 is the only algorithm from this family worth its salt (this is going to be an amazing pun in about two paragraphs).
- **WHIRLPOOL** – Designed by Victor Rijmen (the co-creator of the AES algorithm we discussed earlier) and Paulo Barreto in 2000. Since then it has undergone two revisions. It produces 512-bit hashes that are typically represented as 128-digit hexadecimal numbers.
- **TIGER** – A fairly new algorithm that is beginning to gain some traction with file sharing networks and torrent sites. There are currently no known attacks that are effective against its full 24-round variant.

## Collision

- Hashing in cybersecurity demands unidirectional processes that use a one-way hashing algorithm. It is a crucial step in stopping threat actors from reverse engineering a hash back to its original state. At the same time, two keys can also generate an identical hash. This phenomenon is called a collision.
- A good hash function never produces the same hash value from two different inputs. As such, a hash function that comes with an extremely low risk of collision is considered acceptable.
- To further ensure the uniqueness of encrypted outputs, cybersecurity professionals can also add random data into the hash function. This approach, known as "salting," guarantees a unique output even when the inputs are identical. Salting obstructs bad actors from accessing non-unique passwords. This is because each hash value is unique, even when users reuse their passwords. Salting adds another layer of security to thwart rainbow table attacks.
- 

## Sources

- <https://www.techtarget.com/searchdatamanagement/definition/hashing>
- <https://www.thesslstore.com/blog/difference-encryption-hashing-salting>