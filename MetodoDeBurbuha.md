# Burbuja
/*
    Jose Benjamin Samayoa Villatoro
    5090-18-7483    
    Universidad Mariano Galvez
    Programacion ll
 */
package burbuja;

import java.util.Scanner;

public class Burbuja {

    public static void main(String[] args) {
         /*creacion del objeto para leer por teclado*/
        Scanner sc = new Scanner(System.in);
        /*ingreso del tamaño de arreglos*/
        System.out.print("\n Ingrese Numero de Datos a Ingresar : ");
        int tam = sc.nextInt();
        /*creacion del arreglo*/
        int arr[] = new int[tam];
        System.out.println();
        /*lectura del arreglo*/
        int j = 0;
        for (int i = 0 ; i < arr.length;i++)
        {
            j+=1;
            System.out.print("Elemento " + j + " : ");
            arr[i] = sc.nextInt();
        }
        burbuja(arr);
    }
 
    static void burbuja(int arreglo[])
    {
        for(int i = 0; i < arreglo.length - 1; i++)
        {
            for(int j = 0; j < arreglo.length - 1; j++)
            {
                if (arreglo[j] < arreglo[j + 1])
                {
                    int tmp = arreglo[j+1];
                    arreglo[j+1] = arreglo[j];
                    arreglo[j] = tmp;
                }
            }
        }
        for(int i = 0;i < arreglo.length; i++)
        {
            System.out.print(arreglo[i]+"\n");
        }
    }
}
