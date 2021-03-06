# ClientSubnetOption

Class to add [RFC 7871 - Client Subnet in DNS Queries](https://tools.ietf.org/html/rfc7871) support to [dnspython](http://www.dnspython.org).

## Installation

`pip install clientsubnetoption`

## Requirements

* [python](http://www.python.org) 2.7 or later
* [dnspython](http://www.dnspython.org) 1.10.0 or later

**Note**: If you are installing dnspython on Python3, use `pip install dnspython3`

## Changelog

### 2.1.1
 * Better default for bitmask values (@DarkDeviL)

### 2.1.0
 * Correctly set scope in `to_wire` (@rgacogne)
 * CLI Improvements:
   * Option to set Recursion Desired flag on the message
   * Won't fail completely on nameserver timeout

### 2.0.0
 * Python 3 compatible (tested with 3.4.3 & 2.7.10)
 * Can be installed via pip: `pip install clientsubnetoption`
 * Family is now auto-detected
 * IPs must be given as strings (versus their unpacked form)
  * `ClientSubnetOption('192.168.1.1')` vs `ClientSubnetOption(struct.unpack('!L', socket.inet_aton('192.168.1.1'))[0])`
