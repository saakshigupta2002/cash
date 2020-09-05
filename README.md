#include <cs50.h>
#include <stdio.h>
#include <math.h>

int main(void)
{
int count=0; // count represents no. of coins needed to give
float dollars;
do
{
 dollars = get_float("change owed : \n");
}
while(dollars<=0);


int cents = round(dollars*100);

//loop continue until no change left
while(cents>0)
{
  if(cents>=25)
  {
    cents -= 25;
    count++;
  }
  else if(cents>=10)
  {
    cents -=10;
    count++;
  }
  else if(cents>=5)
  {
    cents -=5;
    count++;
  }
  else
  {
    cents -=1;
    count++;
  }
 
}
    //displays the total number of coins needed to give
  printf(" you owe  %i coins \n" , count);   
}

