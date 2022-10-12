# java-faculdade-aula-ter-a

package calculararea;

import java.util.Scanner;

public class CalcularArea {

    public static void main(String[] args) {
        
        Retangulo novoRetangulo = new Retangulo();
        
        Scanner teclado = new Scanner(System.in);
        
        try{
            
            System.out.println("Digite a altura do retangulo");
            float valorAlturaRetangulo = teclado.nextFloat(); 

            System.out.println("Digite a largura do retangulo");
            float valorLarguraRetangulo = teclado.nextFloat();
            
            if(valorAlturaRetangulo > 0){
                novoRetangulo.setAltura(valorAlturaRetangulo);
            }
            if(valorLarguraRetangulo > 0){
                novoRetangulo.setLargura(valorLarguraRetangulo);
            }
            
            System.out.println(novoRetangulo.CalcularArea());
            System.out.println(novoRetangulo.CalcularPerimetro());
            
        }
        catch(Exception e){
            System.out.println("erro! Roda o codigo denovo " + e);
        }  
    }
}
\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\

package calculararea;
public class Retangulo {
    
    private float largura, altura;
    
        public void setLargura(float larguraParametro){
        this.largura = larguraParametro;
    }
    
    public float getLargura(){
        return largura;
    }
    
    
    public void setAltura(float alturaParametro){
        this.altura = alturaParametro;
    }
    
    public float getAltura(){
        return altura;
    }
    
    public float CalcularArea(){
        return  altura * largura;
    }
    
    public float CalcularPerimetro(){
        return  (altura * 2) + (largura * 2);   
    }
    
    
}
