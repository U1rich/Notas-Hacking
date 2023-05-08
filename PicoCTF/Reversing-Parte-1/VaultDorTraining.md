## Description
Your mission is to enter Dr. Evil's laboratory and retrieve the blueprints for his Doomsday Project. The laboratory is protected by a series of locked vault doors. Each door is controlled by a computer and requires a password to open. Unfortunately, our undercover agents have not been able to obtain the secret passwords for the vault doors, but one of our junior agents obtained the source code for each vault's computer! You will need to read the source code for each level to figure out what the password is for that vault door. As a warmup, we have created a replica vault in our training facility. The source code for the training vault is here: [VaultDoorTraining.java](https://jupiter.challenges.picoctf.org/static/1afdf83322ee9c0040f8e3a3c047e18b/VaultDoorTraining.java)

## Hints

## Solution
Se descarga  el programa del link y como es un progra,a basta con hacerle un cat para ver su codigo fuente.

```bash
┌──(ulrich㉿DasMausoleum)-[~/Documentos/Apuntes 8vo Semestre/Reversing]
└─$ wget https://jupiter.challenges.picoctf.org/static/1afdf83322ee9c0040f8e3a3c047e18b/VaultDoorTraining.java
--2023-05-02 08:34:57--  https://jupiter.challenges.picoctf.org/static/1afdf83322ee9c0040f8e3a3c047e18b/VaultDoorTraining.java
Resolviendo jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)... 3.131.60.8
Conectando con jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)[3.131.60.8]:443... conectado.
Petición HTTP enviada, esperando respuesta... 200 OK
Longitud: 943 [application/octet-stream]
Grabando a: «VaultDoorTraining.java»

VaultDoorTraining.j 100%[===================>]     943  --.-KB/s    en 0s      

2023-05-02 08:35:06 (8.84 MB/s) - «VaultDoorTraining.java» guardado [943/943]

                                                                                
┌──(ulrich㉿DasMausoleum)-[~/Documentos/Apuntes 8vo Semestre/Reversing]
└─$ ls
VaultDoorTraining.java
                                                                                
┌──(ulrich㉿DasMausoleum)-[~/Documentos/Apuntes 8vo Semestre/Reversing]
└─$ cat VaultDoorTraining.java   
import java.util.*;

class VaultDoorTraining {
    public static void main(String args[]) {
        VaultDoorTraining vaultDoor = new VaultDoorTraining();
        Scanner scanner = new Scanner(System.in); 
        System.out.print("Enter vault password: ");
        String userInput = scanner.next();
	String input = userInput.substring("picoCTF{".length(),userInput.length()-1);
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
        return password.equals("w4rm1ng_Up_w1tH_jAv4_eec0716b713");
    }
}

```

## Flag
picoCTF{w4rm1ng_Up_w1tH_jAv4_eec0716b713}

## Aditional Notes

## References
