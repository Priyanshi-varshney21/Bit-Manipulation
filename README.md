# Bit-Manipulation
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
