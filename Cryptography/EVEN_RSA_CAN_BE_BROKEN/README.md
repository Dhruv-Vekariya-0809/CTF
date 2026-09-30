# EVEN RSA CAN BE BROKEN

## Approach 
I started by understanding rsa . used ai to understand how decryptio happens and what is the math behind it
we were given N,e and the cypher text.

![given](/Cryptography/EVEN_RSA_CAN_BE_BROKEN/rsa/main.png)

## Solution
 N=p*q where p and q are prime and N was ap per the given data . therfore one of the prime was 2,i.e.<mark> p=2 and q =(N/2)</mark>

we can find d(private key) as  
(e*d)mod(phi)=1, here phi =(p-1)(q-1)

now we can get the decimal no. as 

(decimal no.*(cyphertext^d))mod(N)=1

this can be done by the code 
```py
N = 24906551859649587303825636064457409606489183493651246701490870692842288080292655094617737429857748620009661253060664513678773152676141488212198785585713198
e = 65537
ciphertext = 12446156144891749343590249068036884382287355217488074416052624289071606958062731947163321846476321006697172722887813920542021692264924118537849156203354235

p = 2
q = N // 2
phi = (p - 1) * (q - 1)
d = pow(e, -1, phi)

deciaml= pow(ciphertext, d, N)

print(f"{deciaml}")
```
after we get this code be can convert the base to 16 making to hex and then convert it to text using .

[changing base in cypherchef](https://gchq.github.io/CyberChef/#recipe=From_Base(10)To_Base(16)&input=MjYyNTU4MDgwODQwNDc5MDI2OTg5NjE3NTAyMDgxNzA5OTU2MjUwMjcxODQzNDUyNzg4NzgwNTQxMjg2MDc2Mzc5MzAyMQ&ienc=65001&oenc=65001)

 [converting Hex to text](https://www.duplichecker.com/hex-to-text.php)

 ![changebase](/Cryptography/EVEN_RSA_CAN_BE_BROKEN/rsa/base.png)

 ![Hextotext](/Cryptography/EVEN_RSA_CAN_BE_BROKEN/rsa/hex.png)

 ## Flag
 academy{tw0_1$_pr!m3207f407f}

 ## Takeaway
 to check if the primes are easy to crack in the rsa .aslo learnt the functioning of rsa .