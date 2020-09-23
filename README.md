<div align="center">

## lcpri\.c


</div>

### Description

How many prime numbers are there between 1 and X? You just have to choose X and this program will do the rest. Click Luke to go to my Web Page: other source code available...
 
### More Info
 
an integer number

the number of prime numbers lower than X


<span>             |<span>
---                |---
**Submitted On**   |
**By**             |[Luke](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByAuthor/luke.md)
**Level**          |Beginner
**User Rating**    |3.3 (10 globes from 3 users)
**Compatibility**  |C
**Category**       |[Math](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByCategory/math__3-12.md)
**World**          |[C / C\+\+](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByWorld/c-c.md)
**Archive File**   |[](https://github.com/Planet-Source-Code/luke-lcpri-c__3-494/archive/master.zip)





### Source Code

```
/*
 Save this file as lcpri.c
*/
#include <stdio.h>
#include <stdlib.h>
int main()
{
 ldiv_t dividi;
 int n, totprimi, primo;
 int cont1, cont2;
 printf("\n\tEnter an integer (>= 1): ");
 scanf("%d", &n);
 if (n < 1)
 {
 printf("\n\t...I said >= 1...bye!\n");
 return(-1);
 }
 totprimi = 0;
 for(cont1 = 1; cont1 < n; cont1++)
 {
 primo = 1;
 for(cont2 = 2; cont2 <= (cont1 / 2); cont2++)
 {
  dividi = ldiv(cont1, cont2);
  if (dividi.rem == 0)
  {
  primo = 0;
  break;
  }
 }
 if (primo) ++totprimi;
 }
 printf("\n\tThere are %d prime numbers lower than %d\n", totprimi, n);
 return 0;
}
```

