
<p align="center">
    <img alt="karma" src="https://i.imgur.com/C3zISlU.gif"/>
</p>

Find leaked emails with your passwords.


## Installation

Install dependencies (Debian/Ubuntu):
```
sudo apt install tor python3 python3-pip
```

## Building from Source

Clone this repository (Original repo is not working), and:
```
git clone https://github.com/cf-iperez/karma.git ; cd karma
sudo -H pip3 install -r requirements.txt
python3 setup.py build
sudo python3 setup.py install
```



### Usage

Start by printing the available actions by running `karma --help`. It's also necessary to start the **Tor** service `sudo service tor start`. Then you can perform the following tests:

1. Search emails with the password: `123456789`
```
karma search '123456789' --password -o test1
```

2. Search emails with the local-part: `johndoe`
```
karma search 'johndoe' --local-part -o test2
```

3. Search emails with the domain: `hotmail.com`
```
karma search 'hotmail.com' --domain -o test3
```

4. Search email password: `johndoe@unknown.com`
```
karma target 'johndoe@unknown.com' -o test4
```

>  % is wildcard character (it is better to use wildcards toward the end of the string)

5. Search email password using a wildcard for the domain (The wildcard can be used for any part of the email `%@%.%`):
```
karma target 'johndoe@%.com' -o test5
```


### Disclaimer

Usage this program for attacking targets without prior consent is illegal. It's the end user's responsibility to obey allapplicable local, state and federal laws. Developers assume no liability and are not responsible for any misuse or damage caused by this program.

