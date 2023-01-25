# OMG! The password manager site I've depended on was breached!

Don't you hate when that happens? If you're concerned about any passwords you've stored somewhere being leaked ([ahem](https://www.pcmag.com/news/lastpass-suffers-another-breach-and-this-time-customer-data-is-affected)), do the following now:

1. Change the passwords for any site you care about: banking, health insurance, social media. See below about choosing passwords.
2. Activate two-factor authentication (2FA) wherever possible[^1]; prefer an app like Google Authenticator over codes sent by SMS.
3. Find another password manager.

## Choosing great passwords

We should be familiar by now with the best practices surrounding passwords:

* Make them long (all of mine are at least 25 characters, except for the boneheaded sites that have a shorter length limit).
* Make them complex (include letters, numbers, and choose from _all_ symbols allowed for the site).
* Make them unique -- do _not_ use the same password for multiple sites.
* Make them random -- and not with the weeny pseudo-randomness that your laptop uses[^2]. Use a site like [Random.org's password generator](https://www.random.org/passwords/?mode=advanced), which uses atmospheric chaos to generate random things (though you'll need to add special characters -- randomly of course).
* Store them in a password manager.
* Let's get meta: Protect the password manager list of great passwords with an equally great password. Never going to remember 25 random characters? Darn right you won't; you probably can't remember a 10-digit phone number anymore. One solution is to generate a text file containing at least 100 passwords (the Random site does this with ease). Use a password from the file, and you'll only have to remember what line number it's on.

## What password manager can I trust?

Now that is becoming a personal question. What's important is that you use one and have great passwords. Use anything that hits all of these points:

* Is vetted (or better yet, created) by respectable security people.
* Uses a _currently_ vetted, approved encryption algorithm. E.g. AES with 256-bit key, elliptic curve, Twofish. Do _not_ use anything that employs DES, 3DES, Blowfish, or any older hash algorithms like MD5 or SHA-1 (or earlier).
* Open source. This is so that anyone -- bad or good -- who has the time can find and expose its weaknesses.
* Currently maintained. Nothing ruins a great app faster than no one keeping track of bugs and security issues.
* Allows for local storage rather than in the Cloud. (Remember, "the Cloud" is just a term for "someone else's storage space". And other peoples' storage is harder to protect.)
* Is backupable and portable, so if your computer dies your passwords don't go to the digital Great Beyond.

### Encryption

The currently NIST-approved algorithm AES (originally called Rijndael) is widely used which is great, since the more an algorithm is exercised, the more it gets tested and the more likely problems will surface. Some more conspiracy-minded security folks won't trust it due to suspicions of NIST working a bit too closely with some government TLAs[^3]. Most of us not running crime syndicates shouldn't worry about such things, though if the NSA did indeed insert backdoors into AES, that does by definition weaken the algorithm for all.

Whatever algorithm gets used, know that someday it will be broken. Choosing longer passwords helps protect against this; as experience has shown me, brute-forcing an 8-character random code takes much longer than a 7-character one. Brute-forcing 25+ characters should take longer than the universe will live with 2020s-era technology.

## Conclusion

If you've been caught up in a password breach, you should have already done the steps in the first section. Following this guide will help protect against any future breaches, and those will never end. 

[^1]: If your financial institution does not allow 2FA, dump it and find another. There is no excuse for this level of stupidity.
[^2]: Yes, there are secure random number generators that application developers can use, but then you rely on the application to do the right thing. [OWASP](https://cheatsheetseries.owasp.org/cheatsheets/Cryptographic_Storage_Cheat_Sheet.html) has a good technical writeup about encryption that all developers should read.
[^3]: TLA: Three-Letter Agency
