# RFID-Brute-Force

These are text password lists that can be used to brute force RFID passwords. There are a lot better ways to find a password, but I haven't seen anyone talk about using normal password lists against RFID tags or publishing a list exclusively for this purpose.


char.txt files are extracted from the top 10 million password list.

word.txt files are extracted from a common English dictionary.

charUP.txt and wordUP.txt Since most evidence (how ever small) shows that uppercase passwords are normally used with RFID these lists have been added.

**Todo list:**

Covert all lists to HEX ending in .dic



**A better dictionary to use is:**

https://github.com/RfidResearchGroup/proxmark3/tree/master/client/dictionaries

These are shorter lists and known default keys. My lists are to be used after the dictionary lists have been exhausted, and after other possible attacks have failed.




**Some examples on what my lists could be used for:**

T55xx and the em4305 chips use a 4 character password

iClass uses an 8 characters password

Mifare Classic uses a 12 characters password

Mifare Pluse uses a 16 characters password




**Examples where my list could have helped find:**
```
50524F58 spells out PROX

50415353 spells out PASS
```
These wouldn't be found in the most common password list, but they would be in the upercase dictionary. Again, the more efficent way to do this would have been to run the t55xx_default_pwds.dic from https://github.com/RfidResearchGroup/proxmark3/tree/master/client/dictionaries. If they had not published that great default password list, then we still would have been able to find these passwords without needing to try all possiblities which could take years.
 
When looking at the Mifare Plus list in mfp_default_keys.dic, we see that there is some corresponding to ASCII with the passwords: 
```
404142434445464748494a4b4c4d4e4f = @ABCDEFGHIJKLMNO

303132333435363738393a3b3c3d3e3f = 0123456789:;<=>?

605F5E5D5C5B5A59605F5E5D5C5B5A59 = `_^]\[ZY`_^]\[ZY
```
Those would not appear in any of the above lists, but this just shows more evidence of an ASCII collocation.



**iClass_Other.dic**

When reviewing default passwords from other lists you start seeing common password schemes being using. For example:

```
a0a1a2a3a4a5 
b0b1b2b3b4b5
from mfc_default_keys.dic

a0a1a2a3a4a5a6a7a0a1a2a3a4a5a6a7
b0b1b2b3b4b5b6b7b0b1b2b3b4b5b6b7
from mfp_default_keys.dic
```

As you can see there are some common themes in the above case its a0 then a1 ect. In these default password lists I took those themes and expanded them to fit the iClass key space. If you combine this with the other list https://github.com/RfidResearchGroup/proxmark3/blob/master/client/dictionaries/iclass_default_keys.dic It still only takes 1 second to run through all 86 keys.
