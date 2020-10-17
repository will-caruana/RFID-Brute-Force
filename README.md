# RFID-Brute-Force

These are text password lists that can be used to brute force RFID passwords. There are a lot better ways to find a password, but I haven't seen anyone talk about using normal password lists against RFID tags or publishing a list exlusively for this purpose.


char.txt files are extracted from the top 10 million password list.

word.txt files are extracted from a common English dictionary.



**Todo list:**

Covert everything to HEX ending in .dic

Covert word.txt two files Uppercase and lower and then into HEX ending in .dic




**A better dictionary to use is:**

https://github.com/RfidResearchGroup/proxmark3/tree/master/client/dictionaries

These are shorter lists and known default keys. My lists are to be used after the dictionary lists have been exhausted, and after other possible attacks have failed.




**Some examples on what my lists could be used for:**

T55xx and the em4305 chips use a 4 character password

iClass uses a 8 characters password

Mifare Classic uses a 12 characters passowrd

Mifare Pluse uses a 16 characters password




**Examples where my list could have helped find:**

50524F58 spells out PROX

50415353 spells out PASS

These wouldn't be found in the most common password list, but they would be in the upercase dictionary. Again, the more efficent way to do this would have been to run the t55xx_default_pwds.dic from https://github.com/RfidResearchGroup/proxmark3/tree/master/client/dictionaries. If they had not published that great default password list, then we still would have been able to find these passwords without needing to try all possiblities.
 
When looking at the Mifare Plus list, we see that there is some corresponding to ASCII with the passwords: 

404142434445464748494a4b4c4d4e4f = @ABCDEFGHIJKLMNO

303132333435363738393a3b3c3d3e3f = 0123456789:;<=>?

605F5E5D5C5B5A59605F5E5D5C5B5A59 = `_^]\[ZY`_^]\[ZY

Those would not appear in any of the above lists, but this just shows more evidence of an ASCII collocation.
