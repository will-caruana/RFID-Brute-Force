# RFID-Brute-Force

There are a lot better ways to find a password but I havent seen anyone talk about using normal password lists against RFID tags.

A better dictionary to use is:

https://github.com/RfidResearchGroup/proxmark3/tree/master/client/dictionaries

T55xx password list is 4 characters  
Sample password 50524F58 spells out PROX.
This wouldnt be found in not the most common password list but would be seen in the upercase dictionary.

iClass is 8 characters 
Mifare is 12 characters 
Mifare pluse is 16 characters 
