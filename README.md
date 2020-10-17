# RFID-Brute-Force

There are a lot better ways to find a password but I havent seen anyone talk about using normal password lists against RFID tags.


char.txt files are extracted from the top 10 million password list.

word.txt files are extracted from a common English dictionary.

List to do:

Covert everything to HEX ending in .dic

Covert word.txt two files Uppercase and lower and then into HEX ending in .dic



A better dictionary to use is:

https://github.com/RfidResearchGroup/proxmark3/tree/master/client/dictionaries


What are this list for?
T55xx is 4 characters  
iClass is 8 characters 
Mifare Classic is 12 characters 
Mifare Pluse is 16 characters 

Examples on where this could have worked.
50524F58 spells out PROX
50415353 spells out PASS
These wouldnt be found in not the most common password list but would be seen in the upercase dictionary. The more efficent way would have been to run the t55xx_default_pwds.dic from https://github.com/RfidResearchGroup/proxmark3/tree/master/client/dictionaries. These files are a last resort effort to crack a card when other options wont work.

When looking at the Mifare Plus list we see that there is some corresponding to ASCII with the passwords but: 
404142434445464748494a4b4c4d4e4f = @ABCDEFGHIJKLMNO
303132333435363738393a3b3c3d3e3f = 0123456789:;<=>?
605F5E5D5C5B5A59605F5E5D5C5B5A59 = `_^]\[ZY`_^]\[ZY

Those these would not appear in the above list is does show more edivcance of an ASCII collocation.  
