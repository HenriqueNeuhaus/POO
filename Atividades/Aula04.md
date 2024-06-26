
# Exercício 3 - Triângulo
- Lados: é definido por três segmentos de reta que conectam os vértices do triângulo.
- Base: é o lado que faz contato direto com o ângulo reto e é paralelo à linha do solo ou a um eixo de referência.
- Altura: é o lado que é perpendicular à base e se estende do vértice oposto ao ângulo reto até a base.
- Ângulo: possui um ângulo interno de exatamente 9 raus. Esse ângulo é chamado de ângulo reto e é formado pela interseção da base e da altura do triângulo.

- Calcular a Área:
  - $A =$ $(base * altura)\over2$


- Classe Principal
``` Java
package poligono;

public class Principal {

    public static void main(String[] args) {
        //Triangulo
        Triangulo t1 = new Triangulo(4,5);
        Triangulo t2 = new Triangulo(10,4);
        
        //calculando área de t1
        System.out.println("Area t1: " + t1.areaTriangulo());
        
        //obtendo valores do t2
        System.out.println("O objeto T2 possui altura = " + t2.getAlturaTriangulo() + " e base = " + t2.getBaseTriangulo());
        
        //alterando valores do t2
        t2.setAlturaTriangulo(6);
        t2.setBaseTriangulo(2);
        System.out.println("O objeto T2 possui altura = " + t2.getAlturaTriangulo() + " e base = " + t2.getBaseTriangulo());
        
        //calculando área de t2
        System.out.println("Area t2: " + t2.areaTriangulo());
              
    }
}
```

- Classe Triângulo
``` Java

package poligono;

public class Triangulo {
    
    //atributos
    private int baseTriangulo;
    private int alturaTriangulo;

    //Contrutor vazio
    public Triangulo() {
        
    }

    //Contrutor com parametros
    public Triangulo(int baseTriangulo, int alturaTriangulo) {
        this.baseTriangulo = baseTriangulo;
        this.alturaTriangulo = alturaTriangulo;
    }

    //Acessar os metodos
    //obter dados do objetos
    public int getBaseTriangulo() {
        return baseTriangulo;
    }

    public int getAlturaTriangulo() {
        return alturaTriangulo;
    }
    
    //alterar dados do objetos
    public void setBaseTriangulo(int baseTriangulo) {
        this.baseTriangulo = baseTriangulo;
    }

    public void setAlturaTriangulo(int alturaTriangulo) {
        this.alturaTriangulo = alturaTriangulo;
    }
    
    //Comportamento do triangulo
    public double areaTriangulo(){
        return (baseTriangulo*alturaTriangulo)/2;
    }
}
```
