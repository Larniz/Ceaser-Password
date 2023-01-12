# Ceaser-Password

#include <stdio.h>
#include <stdlib.h>
#include <string.h>


 

void sezarSifrele ( char *ptr, int key  ) 
{
	while( *ptr!='\0' )
	{
		*ptr = *ptr +key  ; 
		ptr++; 		
	}
	
}

void sezarSifreCoz ( char *ptr, int key  ) 
{
	while( *ptr!='\0' )
	{
		*ptr = *ptr - key  ; 
		ptr++; 		
	}
	
}


int main() 
{
	char metin[100]; 
	int key =3 ; 
	
	printf("Sifrelenecek metni giriniz : ") ; scanf(" %[^\n]s", metin ); 
	printf("Key : ") ; scanf("%d", &key ); 
	
	sezarSifrele(metin, key);  
	
	printf("\nSifrelenmis Metin : %s \n", metin ) ; 
	
	
	sezarSifreCoz (metin, key);  
	
	printf("\nCozulmus    Metin : %s \n", metin ) ; 
	
	
	return 0; 
}
