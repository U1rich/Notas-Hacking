## Descripción

Can you make a CoreWars warrior that always loses, no ties? Your opponent is the Imp. The source is available [here](https://artifacts.picoctf.net/c/314/imp.red). If you wanted to pit the Imp against himself, you could download the Imp and connect to the CoreWars server like this: `nc saturn.picoctf.net 53323 < imp.red`

## Hints

1.  CoreWars is a well-established game with a lot of docs and strategy
2.  Experiment with input to the CoreWars handler or create a self-defeating bot

## Solución

```
ttktv-picoctf@webshell:[~/pico2023]: nc saturn.picoctf.net 53323 
Submit your warrior: (enter 'end' when done)

mov 0, 0
mov 0, 0
end
end
Warrior1:
mov 0, 0
end

Warning:
        Missing ';assert'. Warrior may not work with the current setting
Number of warnings: 1

Rounds: 100
Warrior 1 wins: 0
Warrior 2 wins: 100
Ties: 0
You did it!
picoCTF{h3r0_t0_z3r0_4m1r1gh7_e1610ed2}
```

## Bandera

```
picoCTF{h3r0_t0_z3r0_4m1r1gh7_e1610ed2}
```
## Notas adicionales
## Referencias
