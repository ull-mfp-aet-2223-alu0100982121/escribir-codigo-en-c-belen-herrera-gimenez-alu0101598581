# Buscar-codigo
Chicos la tarea que hay que realizar es la siguiente:
<br>
Escribe cualquier codigo de c++.

/* BUSQUEDA EN ARREGLO
 
* Hay un arreglo de 10 numeros
* El usuario ingresara un numero y el programa buscara si
    existe en el arreglo
* Si el numero existe, mostrar valor y posicion.
* Si no, mostrar mensaje.
* Continuar programa hasta que el usuario ingrese -1
 
https://ccodigo.wordpress.com/
*/
 
#include <iostream>
using namespace std;
 
int main()
{
    const int arrayLen = 10;
    int searchArray[arrayLen] = {324,457,6789,541345,7,6,8965,12,32,4815};
     
    //searchKey es el numero que ingresa el usuario
    //location es la posicion
    int searchKey, location;
     
    while(1) {
        cout << "\nIngresa un numero: ";
        cin >> searchKey;
         
        //checar condicion para terminar programa
        if(searchKey == -1) break;
         
        //busqueda        
        for(int i=0; i<arrayLen; i++) {
            if(searchArray[i] == searchKey) {
                location = i;
                break;
            }
            location = -1;
        }
     
        //si location == -1 entonces el numero no se encontro en el arreglo
        if(location != -1) {
            cout << searchKey << " esta en la posicion [" << location << "] del arreglo.\n";
        }
        else {
            cout << searchKey << " no existe en el arreglo.\n";
        }
    }
         
    return 0;
}
