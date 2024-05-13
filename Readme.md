# Boneh-Boyen Identity-Based Encryption (IBE) Implementation

This repository contains an implementation of the Boneh-Boyen Identity-Based Encryption (IBE) scheme in Python using the Charm-Crypto library.
Charm does not work with Python 3.8+ versions, try Python 3.7 or lower

## Installation

### Tested Environment
- Ubuntu 18.04
- Python 3.6.9
- Charm-Crypto

### Installation Steps

1. **Install VirtualBox**
2. **Install Ubuntu 18.04 ISO disk**
3. **In terminal, run the following commands:**

```bash
# Make sure you are root user
# If not, then run:
su -
visudo
# Add "vboxuser ALL=(ALL) NOPASSWD: ALL" to the last line

# Prerequisite Packages
sudo apt update
sudo apt install build-essential
sudo apt install subversion
sudo apt install m4
sudo apt install flex
sudo apt install bison
sudo apt install python3
sudo apt install python3-setuptools python3-dev
sudo apt install libssl-dev
sudo apt install libgmp-dev
sudo apt install git
sudo apt install wget
pip install "pyparsing<2.4.1,>=2.1.5"

# Install the Stanford PBC Library
wget http://crypto.stanford.edu/pbc/files/pbc-0.5.14.tar.gz
tar xf pbc-0.5.14.tar.gz
cd pbc-0.5.14
./configure LDFLAGS="-lgmp"
make
sudo make install
sudo ldconfig

# Install Charm
git clone https://github.com/JHUISI/charm
cd charm
sudo ./configure.sh
sudo make
sudo make install
sudo ldconfig
```


## References

### Charm-Crypto Installation:
- Article: [Charm-Crypto Installation (Mandarin)](https://juejin.cn/post/7311562052509958180)
- Article : [How to set-up Charm on Ubuntu](https://lrusso96.github.io/blog/cryptography/2021/03/04/charm-setup.html#test)

### Boneh-Boyen Identity-Based Encryption (IBE) Scheme:
- Paper: [Efficient Selective Identity-Based Encryption Without Random Oracles (Section 4.1)](https://crypto.stanford.edu/~dabo/pubs/papers/bbibe.pdf)
  Authors: Dan Boneh, Xavier Boyen

### Other Resources on Identity-Based Encryption (IBE):
- YouTube Video: [Identity based Encryption (IBE)](https://www.youtube.com/watch?v=r6TQWORyZ0Q&t=805s)
- YouTube Video: [Identity based Encryption (IBE)](https://www.youtube.com/watch?v=kdf0u2TGgNg&t=1568s)
- Wikipedia: [Identity-based encryption](https://en.wikipedia.org/wiki/Identity-based_encryption)
- PDF: [Intro to Bilinear Maps](https://people.csail.mit.edu/alinush/6.857-spring-2015/papers/bilinear-maps.pdf)
- Wikipedia: [Pairing-based cryptograph](https://en.wikipedia.org/wiki/Pairing-based_cryptography)
- GitHub Code: [Boneh-Boyen Hierarchical Identity Based Encryption Code](https://github.com/JHUISI/charm/blob/dev/charm/schemes/hibenc/hibenc_bb04.py)

### Boneh-Franklin Scheme:
- Wikipedia: [Boneh–Franklin scheme](https://en.wikipedia.org/wiki/Boneh%E2%80%93Franklin_scheme)

### Charm-Crypto Resources:
- GitHub Repository: [Charm-Crypto](https://github.com/JHUISI/charm)
- Documentation: [Charm-Crypto Cryptographers](https://jhuisi.github.io/charm/cryptographers.html)
