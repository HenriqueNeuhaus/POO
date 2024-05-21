# Exercício 2 – Circunferência

- Calcular a Área
  - A = $\pi$ * $raio^2$
- Perímetro
  - P = 2 * $\pi$ * raio
    
- Classe Principal

``` Java
package poligono;

public class Principal {

    public static void main(String[] args) {    
       //Circunferencia
       Circunferencia c1 = new Circunferencia(5);
       Circunferencia c2 = new Circunferencia();
       
       System.out.println("Area: " + c1.areaCirc());
       System.out.println("Area: " + c2.areaCirc());
       
       //alterou valores de c1 e c2
       c1.setRaioCirc(4);
       c2.setRaioCirc(2);
       
       System.out.println("Area: " + c1.areaCirc());
       System.out.println("Area: " + c2.areaCirc());
       
       //obteve valor do raio de c1 e c2
       System.out.println("Raio c1: " + c1.getRaioCirc());
       System.out.println("Raio c2: " + c2.getRaioCirc());  
    }
}
``` 
- Classe Circunferencia
``` Java
package poligono;

public class Circunferencia {
    //atributos - característica
    public double raioCirc;
    
    //Construtor vazio, sem parametro
    public Circunferencia() {
        
    }
    
    //Construtor com parâmetro
    public Circunferencia(double raioCirc) {
        this.raioCirc = raioCirc;
    }
    
    //Acessar os metodos
    //obter dados do objetos
    public double getRaioCirc() {
        return raioCirc;
    }

    //alterar dados do objetos
    public void setRaioCirc(double raioCirc) {
        this.raioCirc = raioCirc;
    }

    //retorna uma string que "textualmente representa" esse objeto
    @Override
    public String toString() {
        return "Circ{" + "raioCirc = " + raioCirc + '}';
    }
    
    //métodos - comportamento do objeto
    public double areaCirc(){
        return  (Math.pow(raioCirc, 2) * Math.PI);
    }
}
```
