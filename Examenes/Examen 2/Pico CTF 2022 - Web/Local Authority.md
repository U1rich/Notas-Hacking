## Description
Can you get the flag? Go to this [website](http://saturn.picoctf.net:55983/) and see what you can discover.

## Hints

## Solution
Me fui a red y verifique como comprobaba que la contraseña y el usuario fueran correctas y me di cuenta de que hacia una comparacion con dentro de un script js


```js
function checkPassword(username, password)
{
  if( username === 'admin' && password === 'strongPassword098765' )
  {
    return true;
  }
  else
  {
    return false;
  }
}
```

## Flag
picoCTF{j5_15_7r4n5p4r3n7_a8788e61}

## Aditional Notes

## References
