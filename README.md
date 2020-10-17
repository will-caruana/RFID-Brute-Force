# RFID-Brute-Force

There are a lot better ways to find a password but I havent seen anyone talk about using normal password lists against RFID tags.


char.txt files are extracted from the top 10 million password list.

word.txt files are extracted from a common English dictionary.

List to do:

Covert everything to HEX

Covert word.txt two files Uppercase and lower and then into HEX



A better dictionary to use is:

https://github.com/RfidResearchGroup/proxmark3/tree/master/client/dictionaries


What are this list for?
T55xx password list is 4 characters  
Sample password 50524F58 spells out PROX.
This wouldnt be found in not the most common password list but would be seen in the upercase dictionary. The more efficent way would have been to run the t55xx_default_pwds.dic from https://github.com/RfidResearchGroup/proxmark3/tree/master/client/dictionaries. These files are a last resort effort to crack a card when other options wont work.

iClass is 8 characters 

Mifare is 12 characters 

Mifare pluse is 16 characters 

