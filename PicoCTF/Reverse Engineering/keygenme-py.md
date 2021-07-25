# Keygenme-py

*No description*

This challenge came with a python script.

Looking at the script, it seems that the first part of the flag has already been given to us.
    
    username_trial = "SCHOFIELD"
    bUsername_trial = b"SCHOFIELD"

    key_part_static1_trial = "picoCTF{1n_7h3_|<3y_of_"
    key_part_dynamic1_trial = "xxxxxxxx"
    key_part_static2_trial = "}"
    
It seems the challenge is to figure out the dynamic part of the key. 

This block of code seems relevant to that:

    if key[i] != hashlib.sha256(username_trial).hexdigest()[4]:
        return False
    else:
        i += 1

    if key[i] != hashlib.sha256(username_trial).hexdigest()[5]:
        return False
    else:
        i += 1

    if key[i] != hashlib.sha256(username_trial).hexdigest()[3]:
        return False
    else:
        i += 1

    if key[i] != hashlib.sha256(username_trial).hexdigest()[6]:
        return False
    else:
        i += 1

    if key[i] != hashlib.sha256(username_trial).hexdigest()[2]:
        return False
    else:
        i += 1

    if key[i] != hashlib.sha256(username_trial).hexdigest()[7]:
        return False
    else:
        i += 1

    if key[i] != hashlib.sha256(username_trial).hexdigest()[1]:
        return False
    else:
        i += 1

    if key[i] != hashlib.sha256(username_trial).hexdigest()[8]:
        return False
        
Creating a python script to calculate and concatenate the values of the sha256 hash results in e584b363, which is the dynamic part of the key.

`flag:picoCTF{1n_7h3_|<3y_of_e584b363}`
