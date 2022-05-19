import java.util.ArrayList;

public class teste{

    static final int MAX = 1000;
    int top;
    int pilha[] = new int[MAX];

    boolean isEmpty(){
        return(top < 0);
    }
    teste(){
        top = -1;
    }

    boolean adicionar(int x){
        if(top >= (MAX - 1)){
            System.out.println("Pilha vazia");
            return false;
        }
        else{
            pilha[++top] = x;
            System.out.println(x + "Adicionado a Pilha");
            return true;
        }
    }
    int remover(){
        if (top < 0) {
            System.out.println("Pilha Vazia");
            return 0;
        }
        else {
            int x = pilha[top --];
            return x;
        }
    }
    int OlharTopo(){
        if(top < 0){
            System.out.println("Pilha Vazia");
            return 0;
        }
        else {
            int x = pilha[top];
            return x;
        }
    }

class Principal {
    public static void main(String[] args) {
        
        teste st = new teste();
        st.adicionar(10);
        st.adicionar(20);
        st.adicionar(30);

        System.out.println(st.remover() + "Pilha");
    }
}

    
    
}

