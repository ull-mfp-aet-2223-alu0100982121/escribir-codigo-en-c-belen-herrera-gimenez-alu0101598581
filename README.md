# Buscar-codigo
Chicos la tarea que hay que realizar es la siguiente:
<br>
Escribe cualquier codigo de c++.


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
