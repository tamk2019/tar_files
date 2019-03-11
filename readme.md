# GnuPG (GPG)
GPG is a free, opensource implementation of the OpenPGP standard, and is thus cool. It generates big keys and has a very friendly interface unlike bits of PGP.<br />

# GnuPG is a complete and free implementation of the OpenPGP standard as defined by RFC4880 (also known as PGP). GnuPG allows you to encrypt and sign your data and communications; it features a versatile key management system, along with access modules for all kinds of public key directories.

#How to use?<br />
________________________________________
To generate a key just run %gpg --gen-key and follow the instructions. <br />

    Choose a key type, DSA and ElGamal (default) are generally appropriate. <br />

    Choose a key size, the minimum should be 1024, 4096 is best. (1024 is default) <br />

    Choose a key expiration. This is up to you and for general purpose, non-super-secret uses never is fine. Though in more important circumstances expiring keys can be useful.<br />

    When asked give gpg your real name, your email address, you can generally give the comment field a miss.<br />

    When prompted choose a passphrase, make it long enough to be secure, but make sure you remember it... numbers, letters, symbols, etc... the usual password stuff.<br />

	GPG will now begin to generate the actual key.<br />
_________________________________________
Generate a revocation key by running %gpg --gen-revoke and follow instructions. It will ask for your passphrase... Print out the generated revocation key and keep it safe somewhere. <br />
_________________________________________

Export your ascii armored public key. The term ascii armor is key in GPG land... If you do not ascii armor all output from GPG is binary, which is sometimes not so helpful (and harder to include in the body of an email message). To export your key run %gpg --armor --export "<real name>". Copy the output and put it in your .plan in your home directory, and mail it systems. <br /> 
_________________________________________

List all of the keys in your keyring run %gpg --list-keys <br />

To list a small subset of keys in your keyring then you may follow list keys by the first few characters (taken case-insensitively) of their "real name" thus to find all the people who's keys you have whose first name starts with a ''d'' just run %gpg --list-keys d <br />
_________________________________________

To sign a file run %gpg --clearsign <filename> Note: %gpg --sign <filename> will make the output binary and less useful <br />

	To verify a signature run %gpg --verify <filename> The owner of the signature's public key must be in your keyring for this to work. <br />

	To encrypt a file run %gpg --encrypt <filename> <br />

	To sign an encrypt run %gpg --sign --encrypt <filename> or for fun %gpg -se <filename> You will be asked for the name of the person you are encrypting to... <br />

	To decrypt a file run %gpg --decrypt <filename> <br />
