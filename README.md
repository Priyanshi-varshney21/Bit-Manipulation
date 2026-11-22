# Bit-Manipulation
## DECIMAL TO BINARY
def decimal_to_Binary(n):
    if n==0:
        return "0"
    res=""
    while(n>0):
        if n%2==1:
            res+="1"
        else:
            res+="0"
        n=n//2
    return res[::-1]
n=int(input("Enter n:"))
ans=decimal_to_Binary(n)
print(ans)

# BINARY TO DECIMAL
def Binary_to_decimal(n):
    res=0
    pow=0
    while(n>0):
        digit=n%10
        res+=digit*(2**pow)
        pow+=1
        n=n//10
    return res
n=int(input("Enter n:"))
ans=Binary_to_decimal(n)
print(ans)
