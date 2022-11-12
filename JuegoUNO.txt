package juegouno;
import java.util.Scanner;
import java. util.Random;
public class JuegoUNO {
    public static void main(String[] args) {
        
        //menu del juego
        System.out.println("Bienvenido al juego UNO");
        System.out.println("Ingrese la cantidad de jugadores");
        System.out.println("minimo 1 y maximo 4");
        Scanner leer = new Scanner (System.in);
        int jugadores = leer.nextInt();
        
        int carta = 0;
        Random ale = new Random();
        int baraja[][] = new int[30][40];
        
        for (int i = 1; i < baraja.length; i++) {
            for (int j = 0; j < baraja.length; j++) {
                baraja [i][j] = cartasAleatorias(); 
            }
        }
        
        
        //imprimir matriz
        System.out.println("MAtriz 30 * 40\n");
        
        String imprimir = "";
        for (int i = 0; i < baraja.length; i++) {
            for (int j = 0; j < baraja.length; j++) {
                imprimir = imprimir + "/ " + baraja[i][j];
            }
            
            imprimir = imprimir + " /\n";
            
        }System.out.println(imprimir);

        
            //escaneo de jugadores y bots

            while (jugadores == 1) {

            System.out.println("Ingrese Nombre");
            Scanner readName1 = new Scanner(System.in);
            String name1 = readName1.nextLine();

            System.out.println("Desea agregar bots 1 - 3");
            System.out.println("1 selecciona 1 bot");
            System.out.println("2 selecciona 2 bots");
            System.out.println("3 selecciona 3 bots");
            System.out.println("4 no hay bots");
            Scanner readBotardos = new Scanner(System.in);
            int bots = readBotardos.nextInt();
            
            if(bots == 3){
                System.out.println("se jugara sin bots");
            }

            int barajas[] = new int[120];

            System.out.println("Repartiendo cartas...");

            for (int i = 0; i < 120; i++) {
                barajas[i] = cartasAleatorias();
            }

            for (int i = 1; i < 120; i++) {
                System.out.println(barajas[i]);
            }
            
            System.out.println("Cartas del jugador" + name1);
            for (int x = 1; x <= 7; x++) {
                System.out.println(barajas[x]);
            }
            
            if(bots == 1){
                System.out.println("Cartas de bot1;");
                for (int x = 30; x <= 36; x++) {
                System.out.println(barajas[x]);
                }
            }
            
            if(bots == 2){
                System.out.println("Cartas de bot1;");
                for (int x = 30; x <= 36; x++) {
                System.out.println(barajas[x]);
                }
                System.out.println("Cartas de bot2;");
                for (int x = 30; x <= 36; x++) {
                System.out.println(barajas[x]);
                }
            }
            
            if(bots == 3){
                System.out.println("Cartas de bot1;");
                for (int x = 30; x <= 36; x++) {
                System.out.println(barajas[x]);
                }
                System.out.println("Cartas de bot2;");
                for (int x = 80; x <= 86; x++) {
                System.out.println(barajas[x]);
                }
                System.out.println("Cartas de bot3;");
                for (int x = 70; x <= 76; x++) {
                System.out.println(barajas[x]);
                }
            }
            
            System.out.println("******START******");
            System.out.println("Presione 1 para iniciar");
            Scanner readInicio = new Scanner (System.in);
            int iniciarPartida = readInicio.nextInt();
            
            if (iniciarPartida == 1) {
                
                for (int i = 0; i <= 1;) {
                    
                    pausa();
                    System.out.println("Jugador "+ name1);
                    for (int x = 1; x <= 7; x++) {
                    System.out.println("Cartas: "+barajas[x]);
                    }
                    System.out.println("Carta a colocar: ");
                    carta = leer.nextInt();
                    for (int x = 1; x <= 7; x++) {
                    if(barajas[x] == carta){
                    }
                    }  
                    System.out.println("la ultima carta jugada: " + carta);
         
                                
                    if(bots == 1){
                    
                    pausa();
                    System.out.println("Botardo 1");
                    for (int x = 24; x <= 30; x++) {
                    System.out.println("Cartas: "+barajas[x]);
                    }
                    System.out.println("Ayuda al botardo: ");
                    carta=leer.nextInt();
                    for (int x = 1; x <= 7; x++) {
                    if(barajas[x]==carta){      
                    }
                    }
                    System.out.println("la ultima carta jugada: " + carta);
                }
                    if(bots == 2){
                    pausa();
                    System.out.println("Botardo 1");
                    for (int x = 24; x <= 30; x++) {
                    System.out.println("Cartas: "+barajas[x]);
                    }
                    System.out.println("Ayuda al botardo: ");
                    carta=leer.nextInt();
                    for (int x = 1; x <= 7; x++) {
                    if(barajas[x]==carta){      
                    }
                    }
                    System.out.println("la ultima carta jugada: " + carta);
                    
                    pausa();
                    System.out.println("Botardo 2");
                    for (int x = 24; x <= 30; x++) {
                    System.out.println("Cartas: "+barajas[x]);
                    }
                    System.out.println("Ayuda al botardo: ");
                    carta=leer.nextInt();
                    for (int x = 1; x <= 7; x++) {
                    if(barajas[x]==carta){      
                    }
                    }
                    System.out.println("la ultima carta jugada: " + carta);
                    
                }
                    
                    if(bots == 3){
                    pausa();
                    System.out.println("Botardo 1");
                    for (int x = 24; x <= 30; x++) {
                    System.out.println("Cartas: "+barajas[x]);
                    }
                    System.out.println("Ayuda al botardo: ");
                    carta=leer.nextInt();
                    for (int x = 1; x <= 7; x++) {
                    if(barajas[x]==carta){      
                    }
                    }
                    System.out.println("la ultima carta jugada: " + carta);
                    
                    pausa();
                    System.out.println("Botardo 2");
                    for (int x = 80; x <= 86; x++) {
                    System.out.println("Cartas: "+barajas[x]);
                    }
                    System.out.println("Ayuda al botardo: ");
                    carta=leer.nextInt();
                    for (int x = 1; x <= 7; x++) {
                    if(barajas[x]==carta){      
                    }
                    }
                    System.out.println("la ultima carta jugada: " + carta);
                    
                    pausa();
                    System.out.println("Botardo 3");
                    for (int x = 70; x <= 76; x++) {
                    System.out.println("Cartas: "+barajas[x]);
                    }
                    System.out.println("Ayuda al botardo: ");
                    carta=leer.nextInt();
                    for (int x = 1; x <= 7; x++) {
                    if(barajas[x]==carta){      
                    }
                    }
                    System.out.println("la ultima carta jugada: " + carta);
                    
                }
                    
            }  
        }    
    }
       
        while (jugadores == 2) {            
            System.out.println("Ingrese Nombre del jugador 1");
            Scanner readName1 = new Scanner(System.in);
            String name1 = readName1.nextLine();

            System.out.println("Ingrese Nombre del jugador 2");
            Scanner readName2 = new Scanner(System.in);
            String name2 = readName2.nextLine();
            
            System.out.println("Desea agregar bots 1 - 2");
            System.out.println("1 selecciona 1 bot");
            System.out.println("2 selecciona 2 bots");
            System.out.println("3 no hay bots");
            Scanner readBotardos = new Scanner(System.in);
            int bots = readBotardos.nextInt();
            
            if(bots == 3){
                System.out.println("se jugara sin bots");
            }
            
            int barajas[] = new int[120];

            System.out.println("Repartiendo cartas...");
            
            for (int i = 0; i < 120; i++) {
                barajas[i] = cartasAleatorias();
            }

            for (int i = 1; i < 120; i++) {
                System.out.println(barajas[i]);
            }
            
            System.out.println("Cartas del jugador" + name1);
            for (int x = 1; x <= 7; x++) {
                System.out.println(barajas[x]);
            }
            
            System.out.println("Cartas del jugador" + name2);
            for (int x = 10; x <= 16; x++) {
                System.out.println(barajas[x]);
            }
            
            if(bots == 1){
                System.out.println("Cartas de bot1;");
                for (int x = 30; x <= 36; x++) {
                System.out.println(barajas[x]);
                }
            }
            
            if(bots == 2){
                System.out.println("Cartas de bot1;");
                for (int x = 30; x <= 36; x++) {
                System.out.println(barajas[x]);
                }
                System.out.println("Cartas de bot2;");
                for (int x = 80; x <= 86; x++) {
                System.out.println(barajas[x]);
                }
            }
            
            System.out.println("******START******");
            System.out.println("Presione 1 para iniciar");
            Scanner readInicio = new Scanner (System.in);
            int iniciarPartida = readInicio.nextInt();
            
            if (iniciarPartida == 1) {
                
                for (int i = 0; i <= 1;) {
                    
                    pausa();
                    System.out.println("Jugador "+ name1);
                    for (int x = 1; x <= 7; x++) {
                    System.out.println("Cartas: "+barajas[x]);
                    }
                    System.out.println("Carta a colocar: ");
                    carta=leer.nextInt();
                    for (int x = 1; x <= 7; x++) {
                    if(barajas[x]==carta){
                    }
                    }  
                    System.out.println("la ultima carta jugada: " + carta);
         
                    pausa();
                    System.out.println("Jugador "+ name2);
                    for (int x = 10; x <= 16; x++) {
                    System.out.println("Cartas: "+barajas[x]);
                    }
                    System.out.println("Carta a colocar: ");
                    carta=leer.nextInt();
                    for (int x = 1; x <= 7; x++) {
                    if(barajas[x]==carta){
                    }
                    }
                    System.out.println("la ultima carta jugada: " + carta);
                                
                    if(bots == 1){
                        /*
                    System.out.println("Cartas de bot1;");
                    for (int x = 30; x <= 36; x++) {
                    System.out.println(baraja[x]);
                    }*/
                    
                    pausa();
                    System.out.println("Botardo 1");
                    for (int x = 24; x <= 30; x++) {
                    System.out.println("Cartas: "+barajas[x]);
                    }
                    System.out.println("Ayuda al botardo: ");
                    carta=leer.nextInt();
                    for (int x = 1; x <= 7; x++) {
                    if(barajas[x]==carta){      
                    }
                    }
                    System.out.println("la ultima carta jugada: " + carta);
                }
                    if(bots == 2){
                        /*
                    System.out.println("Cartas de bot1;");
                    for (int x = 30; x <= 36; x++) {
                    System.out.println(baraja[x]);
                    }
                    
                    System.out.println("Cartas de bot2;");
                    for (int x = 80; x <= 86; x++) {
                    System.out.println(baraja[x]);
                    }
                    */
                    pausa();
                    System.out.println("Botardo 1");
                    for (int x = 24; x <= 30; x++) {
                    System.out.println("Cartas: "+barajas[x]);
                    }
                    System.out.println("Ayuda al botardo: ");
                    carta=leer.nextInt();
                    for (int x = 1; x <= 7; x++) {
                    if(barajas[x]==carta){      
                    }
                    }
                    System.out.println("la ultima carta jugada: " + carta);
                    
                    pausa();
                    System.out.println("Botardo 2");
                    for (int x = 24; x <= 30; x++) {
                    System.out.println("Cartas: "+barajas[x]);
                    }
                    System.out.println("Ayuda al botardo: ");
                    carta=leer.nextInt();
                    for (int x = 1; x <= 7; x++) {
                    if(barajas[x]==carta){      
                    }
                    }
                    System.out.println("la ultima carta jugada: " + carta);
                    
                }
            }  
        }               
    }
        
        while (jugadores == 3){
            System.out.println("Ingrese Nombre del jugador 1");
            Scanner readName1 = new Scanner(System.in);
            String name1 = readName1.nextLine();

            System.out.println("Ingrese Nombre del jugador 2");
            Scanner readName2 = new Scanner(System.in);
            String name2 = readName2.nextLine();
            
            System.out.println("Ingrese Nombre del jugador 3");
            Scanner readName3 = new Scanner(System.in);
            String name3 = readName3.nextLine();
            
            System.out.println("Desea agregar bots 1 - 2");
            System.out.println("1 selecciona 1 bot");
            System.out.println("2 sin bots");
            Scanner readBotardos = new Scanner(System.in);
            int bots = readBotardos.nextInt();
            
            if(bots == 2){
                System.out.println("se jugara sin bots");
            }
            
            int barajas[] = new int[120];

            System.out.println("Repartiendo cartas...");
            
            for (int i = 0; i < 120; i++) {
                barajas[i] = cartasAleatorias();
            }

            for (int i = 1; i < 120; i++) {
                System.out.println(barajas[i]);
            }
            
            System.out.println("Cartas del jugador" + name1);
            for (int x = 1; x <= 7; x++) {
                System.out.println(barajas[x]);
            }
            
            System.out.println("Cartas del jugador" + name2);
            for (int x = 10; x <= 16; x++) {
                System.out.println(barajas[x]);
            }
            
            System.out.println("Cartas del jugador" + name3);
            for (int x = 24; x <= 30; x++) {
                System.out.println(barajas[x]);
            }

            System.out.println("******START******");
            System.out.println("Presione 1 para iniciar");
            Scanner readInicio = new Scanner (System.in);
            int iniciarPartida = readInicio.nextInt();
            
            if (iniciarPartida == 1) {
                
                for (int i = 0; i <= 1;) {
                    
                    pausa();
                    System.out.println("Jugador "+ name1);
                    for (int x = 1; x <= 7; x++) {
                    System.out.println("Cartas: "+barajas[x]);
                    }
                    System.out.println("Carta a colocar: ");
                    carta=leer.nextInt();
                    for (int x = 1; x <= 7; x++) {
                    if(barajas[x]==carta){
                    }
                    }  
                    System.out.println("la ultima carta jugada: " + carta);
         
                    pausa();
                    System.out.println("Jugador "+ name2);
                    for (int x = 10; x <= 16; x++) {
                    System.out.println("Cartas: "+barajas[x]);
                    }
                    System.out.println("Carta a colocar: ");
                    carta=leer.nextInt();
                    for (int x = 1; x <= 7; x++) {
                    if(barajas[x]==carta){
                    }
                    }
                    System.out.println("la ultima carta jugada: " + carta);
                    
                    pausa();
                    System.out.println("Jugador "+ name3);
                    for (int x = 24; x <= 30; x++) {
                    System.out.println("Cartas: "+barajas[x]);
                    }
                    System.out.println("Carta a colocar: ");
                    carta=leer.nextInt();
                    for (int x = 1; x <= 7; x++) {
                    if(barajas[x]==carta){      
                    }
                    }
                    System.out.println("la ultima carta jugada: " + carta);
                    
                    if(bots == 1){
                    System.out.println("Cartas de bot1;");
                    for (int x = 30; x <= 36; x++) {
                    System.out.println(barajas[x]);
                    }
                    
                    pausa();
                    System.out.println("Botardo ");
                    for (int x = 24; x <= 30; x++) {
                    System.out.println("Cartas: "+barajas[x]);
                    }
                    System.out.println("Ayuda al botardo: ");
                    carta=leer.nextInt();
                    for (int x = 1; x <= 7; x++) {
                    if(barajas[x]==carta){      
                    }
                    }
                    System.out.println("la ultima carta jugada: " + carta);
                    
                }
            }  
        }
    }
        
        while (jugadores == 4) {

            System.out.println("Ingrese Nombre del jugador 1");
            Scanner readName1 = new Scanner(System.in);
            String name1 = readName1.nextLine();

            System.out.println("Ingrese Nombre del jugador 2");
            Scanner readName2 = new Scanner(System.in);
            String name2 = readName2.nextLine();

            System.out.println("Ingrese Nombre del jugador 3");
            Scanner readName3 = new Scanner(System.in);
            String name3 = readName3.nextLine();

            System.out.println("Ingrese Nombre del jugador 4");
            Scanner readName4 = new Scanner(System.in);
            String name4 = readName4.nextLine();

            int barajas[] = new int[120];

            System.out.println("Repartiendo cartas...");
            
            for (int i = 0; i < 120; i++) {
                barajas[i] = cartasAleatorias();
            }

            for (int i = 1; i < 120; i++) {
                System.out.println(barajas[i]);
            }
            
            System.out.println("Cartas del jugador" + name1);
            for (int x = 1; x <= 7; x++) {
                System.out.println(barajas[x]);
            }

            System.out.println("Cartas del jugador" + name2);
            for (int x = 10; x <= 16; x++) {
                System.out.println(barajas[x]);
            }
            
            System.out.println("Cartas del jugador" + name3);
            for (int x = 24; x <= 30; x++) {
                System.out.println(barajas[x]);
            }
 
            System.out.println("Cartas del jugador" + name4);
            for (int x = 30; x <= 36; x++) {
                System.out.println(barajas[x]);
            }
            
            System.out.println("******START******");
            System.out.println("Presione 1 para iniciar");
            Scanner readInicio = new Scanner (System.in);
            int iniciarPartida = readInicio.nextInt();
            
            if (iniciarPartida == 1) {
                
                for (int i = 0; i <= 1;) {
                    
                    pausa();
                    System.out.println("Jugador "+ name1);
                    for (int x = 1; x <= 7; x++) {
                    System.out.println("Cartas: "+barajas[x]);
                    }
                    System.out.println("Carta a colocar: ");
                    carta=leer.nextInt();
                    for (int x = 1; x <= 7; x++) {
                    if(barajas[x]==carta){
                    }
                    }  
                    System.out.println("la ultima carta jugada: " + carta);
         
                    pausa();
                    System.out.println("Jugador "+ name2);
                    for (int x = 10; x <= 16; x++) {
                    System.out.println("Cartas: "+barajas[x]);
                    }
                    System.out.println("Carta a colocar: ");
                    carta=leer.nextInt();
                    for (int x = 1; x <= 7; x++) {
                    if(barajas[x]==carta){
                    }
                    }
                    System.out.println("la ultima carta jugada: " + carta);
                    
                    pausa();
                    System.out.println("Jugador "+ name3);
                    for (int x = 24; x <= 30; x++) {
                    System.out.println("Cartas: "+barajas[x]);
                    }
                    System.out.println("Carta a colocar: ");
                    carta=leer.nextInt();
                    for (int x = 1; x <= 7; x++) {
                    if(barajas[x]==carta){      
                    }
                    }
                    System.out.println("la ultima carta jugada: " + carta);
                    
                    pausa();
                    System.out.println("Jugador "+ name4);
                    for (int x = 30; x <= 36; x++) {
                    System.out.println("Cartas: "+barajas[x]);
                    }
                    System.out.println("Carta a colocar: ");
                    carta=leer.nextInt();
                    for (int x = 1; x <= 7; x++) {
                    if(barajas[x]==carta){
                    }
                    }
                    System.out.println("la ultima carta jugada: " + carta);
                    
                }          
            }           
        }    
    }
    //funcion numeros randoms
    public static int cartasAleatorias() {
        Random land = new Random();
        int rand = land.nextInt(9 - 0 + 1) + 0;
        return rand;
    }
    
    private static Scanner teclado = new Scanner(System.in);
    
    private static void pausa() {
        System.out.println("\n\t\tPULSA ENTER PARA CONTINUAR\n");
        teclado.nextLine();
    }        
    //funciones usadas
    
    
        
    
    
    //Se termia la funcion
        
        
        
        
        
        
        
        
        
        
        
        
        
        
        
       

    
    }    
    
    
