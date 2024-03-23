#!/bin/python3

message = input('Enter the message to be decrypted: ') # encrypted message
LETTERS = 'ABCDEFGHIJKLMNOPQRSTUVWXYZ'.lower()
for key in range(len(LETTERS)):
    translated = ''
    for symbol in message:
        if symbol in LETTERS:
            num = LETTERS.find(symbol)
            num = num - key
            if num < 0:
                num = num + len(LETTERS)
            translated = translated + LETTERS[num]
        else:
            translated = translated + symbol
    print('Hacking key #%s: %s' % (key,translated))
                                                    
