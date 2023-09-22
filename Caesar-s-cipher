# Caesar's cipher


logo = """
 ,adPPYba, ,adPPYYba,  ,adPPYba, ,adPPYba, ,adPPYYba, 8b,dPPYba,
a8"     "" ""     `Y8 a8P_____88 I8[    "" ""     `Y8 88P'   "Y8
8b         ,adPPPPP88 8PP"""""""  `"Y8ba,  ,adPPPPP88 88
"8a,   ,aa 88,    ,88 "8b,   ,aa aa    ]8I 88,    ,88 88
 `"Ybbd8"' `"8bbdP"Y8  `"Ybbd8"' `"YbbdP"' `"8bbdP"Y8 88
            88             88
           ""             88
                          88
 ,adPPYba, 88 8b,dPPYba,  88,dPPYba,   ,adPPYba, 8b,dPPYba,
a8"     "" 88 88P'    "8a 88P'    "8a a8P_____88 88P'   "Y8
8b         88 88       d8 88       88 8PP""""""" 88
"8a,   ,aa 88 88b,   ,a8" 88       88 "8b,   ,aa 88
 `"Ybbd8"' 88 88`YbbdP"'  88       88  `"Ybbd8"' 88
              88
              88
"""



def txt_cipher(choice, key, original_txt):
    if key >= 26 or key <= -26:
        key = key % 26

    cipher_txt = []
    original_lst = list(original_txt)

    if choice == 'encode':
        for i in original_lst:
            if i.isalpha():
                num = ord(i) + key
                if i == ' ':
                    cipher_txt += ' '
                elif 97 <= num <= 122:
                    cipher_txt += chr(ord(i) + key)
                elif num < 97:
                    cipher_txt += chr(ord(i) + key + 26)
                elif num > 122:
                    cipher_txt += chr((ord(i) + key) - 26)
            else:
                cipher_txt += i
    elif choice == 'decode':
        for i in original_lst:
            if i.isalpha():
                num = ord(i) - key
                if 97 <= num <= 122:
                    cipher_txt += chr(ord(i) - key)
                elif num < 97:
                    cipher_txt += chr(ord(i) - key + 26)
                elif num > 122:
                    cipher_txt += chr((ord(i) - key) - 26)
            else:
                cipher_txt += i

    encoded_text = ""
    decoded_text = ""

    if choice == 'encode':
        print(f"Here is the encoded result: {encoded_text}")

    elif choice == 'decode':
        print(f"Here is the decoded result: {decoded_text}")

    print(''.join(cipher_txt))


# main function starts here 

print(logo)
choice = ""
while choice != 'encode' and choice != 'decode':
    choice = input("Type 'encode' to encrypt, type 'decode' to decrypt: \n").lower()
original_txt = ""
while original_txt == "":
    original_txt = input("Type your message: \n").lower()
# error for empty string(key): Python cannot convert empty str to int, if user did not type any number it will throw an error

num = False
key = None
while num == False:
    shift = input("Type the shift number: \n")
    if shift.isdigit():
        key = int(shift)
        num = True
    else:
        for i in range(0, len(shift)):
            if not shift[i].isdigit:
                if not i == 0:
                    break
            else:
                if i == len(shift) - 1:
                    num = True
                    key = int(shift)

txt_cipher(choice, key, original_txt)
