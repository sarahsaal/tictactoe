# tictactoe 


import java.util.Scanner;

public class Main {
    static Scanner s = new Scanner(System.in);

    static char[] arrayboard = {'_','_','_','_','_','_','_','_','_'};
    static char turn = 'x';
    static boolean gameover = false;


    public static void main(String[] args) {
        update();

    }
    public static void showboard (){
        for (int i = 0; i < arrayboard.length; i++) {
                System.out.print(arrayboard[i]);
                if ((i+1) %3 == 0){
                    System.out.println();
            }

        }
    }

    public static void update (){
        int place=0;
        while (!gameover){
            System.out.println();
            System.out.println("\"" + turn + "\"" + " is playing");
            showboard();

            do {
                System.out.println("enter a number between 1-9 ");
                place = s.nextInt();

            }while (place<1 || place > 9);
            if (arrayboard[place-1] == '_' ){
                arrayboard[place-1]=turn;
                winchek();
            }else if (arrayboard[place-1] != '_'){
                System.out.println("you can't put here");
            }
                if (turn == 'x'){
                    turn = '0';
                }else {
                    turn = 'x';
                }
            }
          }

    public static void winchek () {
        if (arrayboard[0] == 'x' && arrayboard[1] == 'x' && arrayboard[2] == 'x') {  xwin();
        } else if (arrayboard[3] == 'x' && arrayboard[4] == 'x' && arrayboard[5] == 'x') {  xwin();
        } else if (arrayboard[6] == 'x' && arrayboard[7] == 'x' && arrayboard[8] == 'x') {  xwin();
        } else if (arrayboard[0] == 'x' && arrayboard[4] == 'x' && arrayboard[8] == 'x') {  xwin();
        } else if (arrayboard[2] == 'x' && arrayboard[4] == 'x' && arrayboard[6] == 'x') {  xwin();
        } else if (arrayboard[0] == 'x' && arrayboard[3] == 'x' && arrayboard[6] == 'x') {  xwin();
        } else if (arrayboard[1] == 'x' && arrayboard[4] == 'x' && arrayboard[7] == 'x') {  xwin();
        } else if (arrayboard[2] == 'x' && arrayboard[5] == 'x' && arrayboard[8] == 'x') {  xwin();
        }else
        if (arrayboard[0] == '0' && arrayboard[1] == '0' && arrayboard[2] == '0') {  the0win();
        } else if (arrayboard[3] == '0' && arrayboard[4] == '0' && arrayboard[5] == '0') {  the0win();
        } else if (arrayboard[6] == '0' && arrayboard[7] == '0' && arrayboard[8] == '0') {  the0win();
        } else if (arrayboard[0] == '0' && arrayboard[4] == '0' && arrayboard[8] == '0') {  the0win();
        } else if (arrayboard[2] == '0' && arrayboard[4] == '0' && arrayboard[6] == '0') {  the0win();
        } else if (arrayboard[0] == '0' && arrayboard[3] == '0' && arrayboard[6] == '0') {  the0win();
        } else if (arrayboard[1] == '0' && arrayboard[4] == '0' && arrayboard[7] == '0') {  the0win();
        } else if (arrayboard[2] == '0' && arrayboard[5] == '0' && arrayboard[8] == '0') {  the0win();
        }
    }

    public static void xwin (){
        gameover = true;
        System.out.println("player  " + "'x'" + "  win!!!");
        showboard();
    }

    public static void the0win (){
        gameover = true;
        System.out.println("player  " + "'0'" + "  win!!!");
        showboard();
    }

         }

