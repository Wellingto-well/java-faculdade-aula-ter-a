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




+++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++

outro dia


+++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++




package jokepo;

import java.util.Random;
import java.util.Scanner;

public class JokePo {
    
public static void main(String[] args) {
    
    int empate = 0;
    int vitoriaMaquina = 0;
    int vitoriaUsuario = 0;
    int escolhaDoUsuario;
    int paraParar;
    int sorteioJokePoMaquina;
    
    Random random = new Random();
    
    
    Scanner teclado = new Scanner(System.in);
    //0 pedra 1 papel 2 tesoura
    System.out.println("Digite seu nome");
    String nome = teclado.nextLine();

    do{
        
        sorteioJokePoMaquina = random.nextInt(3);
        
        
        System.out.println("\nEssa são as opções:");
        System.out.println("\n0 para Pedra");
        System.out.println("1 para papel");
        System.out.println("2 para tesoura");
        System.out.println("3 para sair");
        System.out.println("");
        System.out.println("O placar está");
        System.out.println("\nEmpate: " + empate);
        System.out.println(nome+ ": " + vitoriaUsuario);
        System.out.println("maquina: " + vitoriaMaquina);
        
        

        System.out.println("\nDigite 0 para pedra \nDigite 1 para papel \nDigite 2 para tesoura \nDigite 3 para sair ");
        escolhaDoUsuario = teclado.nextInt();

        
        if(sorteioJokePoMaquina == escolhaDoUsuario){
            empate++;
            System.out.println("Empatou!!\nMaquina Digitou:"+sorteioJokePoMaquina);
        }
        else if(sorteioJokePoMaquina == 0  && escolhaDoUsuario == 1){
            vitoriaUsuario++;
            System.out.println("Usuario ganhou\nMaquina Digitou:"+sorteioJokePoMaquina);
        }
        else if(sorteioJokePoMaquina == 0 && escolhaDoUsuario == 2){
            vitoriaMaquina++;
            System.out.println("Vitoria da maquina\nMaquina Digitou:"+sorteioJokePoMaquina);
        }
        else if(sorteioJokePoMaquina == 1 && escolhaDoUsuario == 0){
            vitoriaMaquina++;
            System.out.println("Vitoria da maquina\nMaquina Digitou:"+sorteioJokePoMaquina);
        }
        else if(sorteioJokePoMaquina == 1 && escolhaDoUsuario == 2){
            vitoriaUsuario++;
            System.out.println("Usuario ganhou\nMaquina Digitou:"+sorteioJokePoMaquina);
        }
        else if(sorteioJokePoMaquina == 2 && escolhaDoUsuario == 0){
            vitoriaUsuario++;
            System.out.println("Usuario ganhou\nMaquina Digitou:"+sorteioJokePoMaquina);
        }
        else if(sorteioJokePoMaquina == 2 && escolhaDoUsuario == 1){
            vitoriaMaquina++;
            System.out.println("Vitoria da maquina\nMaquina Digitou:"+sorteioJokePoMaquina);
        }
        
    } while(escolhaDoUsuario != 3);
   
    
    
    
    }
    
}

