Installation : 

This module requires installation of yara-python.

1) Install it using : yum -y install yara-python (In case of any issue, install forensics reporitory for your OS (https://forensics.cert.org/) and then try using below command.

	yum -y --enablerepo=forensics install yara-python
2) Clone this repository and then run the program as python ./NoMoreXOR.py

NoMoreXOR.py
=============

Tool to help guess a files 256 byte XOR key by using frequency analysis.

Usage
-----
	usage: NoMoreXOR.py [-h] [-a] [-c] [-xor key] [-g] [-o outfile] [-y YARARULES]
						Path

	Tool to help guess a files 256 byte XOR key by using frequency analysis.

	positional arguments:
	Path                  Path to file to be analyzed

	optional arguments:
	-h, --help            show this help message and exit
	-a, --analyze         Auto analyze the specified file by looking for all
						  possible XOR keys then apply each of them & scan with
					      YARA to try and determine if it's the correct XOR key
						 (requires an output file)
	-c, --convert         Convert the input file to a hex_file (requires an
						  output file)
	-xor key              XOR the file with the supplied XOR key (requires an
						  output file)
	-g, --guess           Print out information from the hex_file including most
						  common characters and possible SHA256 keys
	-o outfile, --out outfile
						  Name of output file to create
	-y YARARULES, --yararules YARARULES
						  Path to YARA rules to be used during auto analysis if
						  different than what's hardcoded

