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

# CHECK Ith BIT
def checkIthBit(n):
  rem=""
  while n>0:
    if n%2==0:
      rem+="0"
    else:
      rem+="1"
    n=n//2
  if i<len(rem) and rem[i]=="1":
    return True
  else:
    return False

# CHECK IF A NUMBER IS A POWER OF 2 or not
def isPowerOfTwo(self, n: int) -> bool:
        if n<=0:
            return False
        if n&(n-1)==0:
            return True
        else:
            return False

# COUNT NUMBER OF SET BITS
def countSetBits(self, n: int) -> int:
        result = [0] * (n + 1)
        for i in range(1,n+1):
            if i%2!=0:
                result[i]=result[i//2]+1
            else:
                result[i]=result[i//2]        
        return result[i]
