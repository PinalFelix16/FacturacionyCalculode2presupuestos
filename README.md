# FacturacionyCalculode2presupuestos
Desarrollar un programa que reciba datos de la factura utilizando la clase Scanner.
/*Desarrollar un programa que reciba datos de la factura utilizando la clase Scanner de la siguiente manera:
1.	Reciba el nombre de la factura o descripción.
2.	Reciba 2 precios de productos y que contenga decimales, 
3.	Calcule el total, sume ambos precios y agregue un valor de impuesto del 19%
Mostrar en un solo String el nombre de la factura, el monto total bruto (antes de impuesto), el impuesto y el monto total neto incluyendo impuesto.*/

import java.util.Scanner;
public class DetalleDeFactura {
    public static void main(String[] args) {
        Scanner leer=new Scanner(System.in);
        String nombreFactura;
        double precio1,precio2,sumPre,resImp,resFinal;
        System.out.println("Ingresa el nombre de la FACTURA ");
        nombreFactura=leer.nextLine();
        System.out.println("Ingresa el precio 1");
        precio1=leer.nextDouble();
        System.out.println("Ingresa el precio 2");
        precio2=leer.nextDouble();
        sumPre=precio1+precio2;
        resImp=sumPre*.19;
        resFinal=sumPre+resImp;

        String detalles="El nombre de la fatura es: " + nombreFactura + "\nTiene un total sin impuestos de: " + sumPre +
                "\nEl tototal de impuestos es: " + resImp + "\nTotal neto con (incluido impuesto): " + resFinal;
        System.out.println(detalles);
    }
}
