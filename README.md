# Programowanie_obiektowe-Alan_Stelmach
#include <stdio.h>
#include <stdlib.h>

struct trojkat{
    float a;
    float b;
    float c;
};

float fun(struct trojkat troj1)
{
    float x=troj1.a + troj1.b + troj1.c;
    return x;
}
void fun1(struct trojkat troj1, struct trojkat *troj2)
{
    troj2=&troj1;
}

int main()
{
    float obwod;
    struct trojkat troj1;
    troj1.a=6.0;
    troj1.b=5.0;
    troj1.c=11.6;

    struct trojkat *troj2=(struct trojkat*) malloc(sizeof(struct trojkat));

    obwod=fun(troj1);
    fun1(troj1, troj2);
    printf("%f", obwod);
    free(troj2);
    return 0;
}
