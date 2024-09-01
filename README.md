import string
import secrets

def code(parts):
    count=0
    for i in mess:
        count=count+1
    if count > 1:
        codeds=[]
        for i in parts:
            final=i[0]
            rest=i[1:]+i[0]
            randomletter=''.join(secrets.choice(string.ascii_letters)for x in range(3))
            randomletters=''.join(secrets.choice(string.ascii_letters)for x in range(3))
            coded=randomletter+rest+randomletters
            codeds.append(coded)
        print(' '.join(codeds))
def decode():
    codes=[]
    mess=input("Entert he message for decrypted : ")
    parts=mess.split(' ')
    for i in parts:
        code=i[3:-3]
        rest=code[-1]
        final=rest+code[:-1]
        codes.append(final)
    print(' '.join(codes))
coded=[]
finals=[]
print("Choose the following option : \n 1. Code \n 2. Decode")
choose=input("Choose : ")

if choose == '1':
    mess=input("Enter the message : ")
    parts=mess.split(' ')
    code(parts)
    
elif choose == '2':
    decode()
else :
    print("Invalid Input !")
