# Vault-Door-Training

## Approach 
> I started by running the java file on the terminal

![java](/rev/vault-door-training/vault/run.png)

>to see what was happening i opened the code in vs code and thats where i got the flag

## Solution

>firstly open the java file in vs code 

```js
import java.util.*;

class VaultDoorTraining {
    public static void main(String args[]) {
        VaultDoorTraining vaultDoor = new VaultDoorTraining();
        Scanner scanner = new Scanner(System.in); 
        System.out.print("Enter vault password: ");
        String userInput = scanner.next();
	String input = userInput.substring("academy{".length(),userInput.length()-1);
	if (vaultDoor.checkPassword(input)) {
	    System.out.println("Access granted.");
	} else {
	    System.out.println("Access denied!");
	}
   }

    // The password is below. Is it safe to put the password in the source code?
    // What if somebody stole our source code? Then they would know what our
    // password is. Hmm... I will think of some ways to improve the security
    // on the other doors.
    //
    // -Minion #9567
    public boolean checkPassword(String password) {
        return password.equals("w4rm1ng_Up_w1tH_jAv4_c02db1ca2a4");
    }
}
```

>on seeing the code the user input is in the format academy{} adn the string in side th {} is written below as indicated by the hint 

## Flag
 academy{w4rm1ng_Up_w1tH_jAv4_c02db1ca2a4}

 ## Takeaway

 check the code once to see the password or the flag is in the code itself