#include <fstream>
#include<iostream>
#include <oleidl.h>
#include <ostream>
#include <stdio.h>
#include <stdlib.h>
#include<string>
#include<Windows.h>
#include <synchapi.h>
#include<cstdlib>
#include <winuser.h>
#include<algorithm>
#include<ostream>
#include<random>//
#include<ctime>
#include<array>
#include<conio.h>
#include<vector>
using namespace std;
string name_draft;
int player_choice;
/*Rows And Collums*/
int rows;
int collums;
int rows2;
int collums2;
bool Is_Draw = true;
string winner;
bool game_end;
int collumn_bot_move;
int row_bot_move;
int collumn_bot_move2;
int rows_bot_move2;

//////////////////////
//----------------------------//
/*Displaying board*/ 

void bot() {

}
void creator() {
 ofstream Creator("Creator_Social_Media_Links.html");
 Creator << "<html>" << endl;
 Creator << "<head><title>Creators Social Media</title></head>" << endl;
 Creator << "<body>\n";
 Creator << "<h1>Facebook: https://www.facebook.com/profile.php?id=100024820629634 </h1>\n";
 Creator << "<h2>Discord: Lewiz#3507 <h2>\n";
 Creator << "<body>Youtube Channel</title>\n";
 Creator << "<body><p>MrGhostler || https://www.youtube.com/channel/UCHhKngvY6NJxP23AZk6awrA</p></body>\n";
 Creator << "</html>\n";
 Creator.close();
 string cmd = "Start Creator_Social_Media_Links.html";
 system(cmd.c_str());
}
//////////////////////
////////game rules////



void game_rules() {
string rules[][3] = {{"1. Respect"},
                    {"2. No Provokes"},
                    {"3. No Mad"}};
cout << rules[0][0] << endl;
cout << rules[1][0] << endl;
cout << rules[2][0] << endl;
cout << "Press ESC to Return" << endl;
while (true) {
    if(_kbhit()) {
        char key = _getch();
        if (key == 27) {
            system("exit");
        }
    }
  }
} 
//////////////////////





random_device rd;
mt19937 g(rd());
mt19937 e(rd());
////////Random System////;
//////PLayers/////////
int Player_1_Scores;
int Player_2_Scores;
string Player_1;
string Player_2;
string draftplr;
string Player_Names[2] = {Player_1, Player_2};
///////////////////////Choices////////////////////////////////////
string choices[][3] = {{"1. Start"},
                      {"2. Game's Regulations"},
                      {"3. Game's Foundation And Creator"}};

////////////////////////////////////////////////////////////////////////////////
////////////////////////////Rock Paper Scissor System///////////////////////////
int ran[2] = {1, 2};
int size_of_ran = sizeof(ran)/sizeof(int);
string dots[3] = {".", "..", "..."};
int count = 0;
int newnumbername = rand() % 1000 + 1;
////////////////////////////////////////////////////////////////////////////////////////////
////////////////////////////////////////////////////////////////////////////////////////////




void rock_paper_scissor() {
    cout << "You Will Have 2 Int Numbers Which Is 1 and 2, These Will Be Randomizely Rolled" << endl;
    Sleep(500);
    cout << "Please Press Enter Again To Start The Roll" << endl;
    if (getchar() == '\n') {
        Sleep(10000);
        cout << "Randomizing Your Number";
        for (int i = 0; i <= 3; i++) {
        Sleep(2000);
        cout << dots[i] << endl;
        }
    cout << "Roll Is Being Conducted..." << endl;
    Sleep(1000);
    }
}






void leaderstats() {
/*Score Board/ Leaderstats*/
    cout << "-------------------LeaderStats-----------------" << endl;
    cout << "-----------------------------------------------" << endl;
    cout << "Player Name " << " || " << " Scores " << " || " << endl;
    cout << "-----------------------------------------------" << endl;
    cout <<  Player_1 << " || " <<    Player_1_Scores   << " || " << endl; 
    cout <<  Player_2 << " || " <<    Player_2_Scores   << " || " << endl; 
    cout << "-----------------------------------------------" << endl;
    cout << "-----------------------------------------------" << endl;
    }
    ///////
//////////////////////////////////////////////////////////////////////////////////////////////////

/////////////////////////
///////TIC TAC TOE SYSTEM ////
     
     
     
     
     char board[5][5] = {{' ', ' ', ' ', ' ', ' '},
                        {' ', ' ', ' ', ' ', ' '},
                        {' ', ' ', ' ', ' ', ' '},
                        {' ', ' ', ' ', ' ', ' '},
                        {' ', ' ', ' ', ' ', ' '}};
    const char nil = ' ';
    const int size_of_rows = 5;
    const int size_of_collums = 5;










void DisplayBoard() {
cout << "      |      |      |      |      |      " << endl;
cout << board[0][0] << "     | " << board[0][1] << "    | " <<  board[0][2] << "    | " << board[0][3] << "    | " << board[0][4] << "    | "  << endl;
cout << "______+" << "______+" << "______+" << "______+" << "______+" << "__end__+" << endl;
cout << "      |      |      |      |      |      " << endl;
cout << board[1][0] << "     | " << board[1][1] << "    | " <<  board[1][2] << "    | " << board[1][3] << "    | " << board[1][4] << "    | "  << endl;
cout << "______+" << "______+" << "______+" << "______+" << "______+" << "__end__+" << endl;
cout << "      |      |      |      |      |      " << endl;
cout << board[2][0] << "     | " << board[2][1] << "    | " <<  board[2][2] << "    | " << board[2][3] << "    | " << board[2][4] << "    | "  << endl;
cout << "______+" << "______+" << "______+" << "______+" << "______+" << "__end__+" << endl;
cout << "      |      |      |      |      |      " << endl;
cout << board[3][0] << "     | " << board[3][1] << "    | " <<  board[3][2] << "    | " << board[3][3] << "    | " << board[3][4] << "    | "  << endl;
cout << "______+" << "______+" << "______+" << "______+" << "______+" << "__end___+" << endl;
cout << "      |      |      |      |      |      " << endl;
cout << board[4][0] << "     | " << board[4][1] << "    | " <<  board[4][2] << "    | " << board[4][3] << "    | " << board[4][4] << "    | "  << " end " << endl;
}
    int Choosing_Boxes;
    int row, columns;
    const char X = 'X';
    const char O = 'O';
     int n = rand() % 2;

bool gameoverforbotiffirst() {
        for (int i = 0; i <= 4; i++) {
            if (board[i][0] != ' ' && board[i][0] == board[i][1] && board[i][0] == board[i][2] && board[i][0] == board[i][3] && board[i][0] == board[i][4]) {
                if (board[i][0] == O) {
                cout << "The Winner Is: BOT" << newnumbername << endl;
                Sleep(2000);
                cout << "quitting the program..." << endl;
                return true;
                }
                if (board[i][0] == X) {
                cout << "You Won!!!" << endl;
                Sleep(2000);
                cout << "quitting the program..." << endl;
                return true;
                }
            }
        }
        for (int e = 0; e <= 4; e++) {
            if (board[0][e] != ' ' && board[0][e] == board[1][e] && board[0][e] == board[2][e] && board[0][e] == board[3][e] && board[0][e] == board[4][e]) {
                if (board[0][e] == O) {
                    cout << "The Winner Is: BOT" << newnumbername << endl;
                    Sleep(2000);
                    cout << "quitting the program..." << endl;
                return true;
                }
                if (board[0][e] == X) {
                    cout << "You Won!!!" << endl;
                    Sleep(2000);
                    cout << "quitting the program..." << endl;
                return true;
                }
            }
        }
            if (board[0][0] != ' ' && board[0][0] == board[0][1] && board[0][0] == board[0][2] && board[0][0] == board[0][3] && board[0][0] == board[0][4]) {
                if (board[0][0] == O) {
                    cout << "The Winner Is: BOT" << newnumbername << endl;
                    Sleep(2000);
                    cout << "quitting the program..." << endl;
                return true;
                }
                if (board[0][0] == X) {
                    cout << "You Won!!!" << endl;;
                    Sleep(2000);
                    cout << "quitting the program..." << endl;
                    return true;
                }
            }
            if (board[0][4] != ' ' && board[0][4] == board[0][3] && board[0][4] == board[0][2] && board[0][4] == board[0][1] && board[0][4] == board[0][0]) {
                if (board[0][4] == O) {
                    cout << "The Winner Is: BOT" << newnumbername << endl;
                    Sleep(2000);
                    cout << "quitting the program..." << endl;
                    return true;
                }
                if (board[0][4] == X) {
                    cout << "You Won" << endl;
                    Sleep(2000);
                    cout << "quitting the program..." << endl;
                    return true;
                }
            }
            for (int i = 0; i <= 4; i++) {
                for (int j = 0; j <=4; j++) {
                    if (board[i][j] == ' ') {
                        Is_Draw = false;
                        return false;
                        break;
                    }
                }
            }
            if (!Is_Draw) {
                return false;
            }
            if (Is_Draw) {
                cout << "Game Ends with a draw" << endl;
                Sleep(2000);
                return true;
            }

            return false;
}





bool gameoverforbotifsecond() {
        for (int i = 0; i <= 4; i++) {
            if (board[i][0] != ' ' && board[i][0] == board[i][1] && board[i][0] == board[i][2] && board[i][0] == board[i][3] && board[i][0] == board[i][4]) {
                if (board[i][0] == X) {
                cout << "The Winner Is: BOT" << newnumbername << endl;
                Sleep(2000);
                cout << "quitting the program..." << endl;
                return true;
                }
                if (board[i][0] == O) {
                cout << "You Won!!!" << endl;
                Sleep(2000);
                cout << "quitting the program..." << endl;
                return true;
                }
            }
        }
        for (int e = 0; e <= 4; e++) {
            if (board[0][e] != ' ' && board[0][e] == board[1][e] && board[0][e] == board[2][e] && board[0][e] == board[3][e] && board[0][e] == board[4][e]) {
                if (board[0][e] == X) {
                    cout << "The Winner Is: BOT" << newnumbername << endl;
                    Sleep(2000);
                    cout << "quitting the program..." << endl;
                return true;
                }
                if (board[0][e] == O) {
                    cout << "You Won!!!" << endl;
                    Sleep(2000);
                    cout << "quitting the program..." << endl;
                return true;
                }
            }
        }
            if (board[0][0] != ' ' && board[0][0] == board[0][1] && board[0][0] == board[0][2] && board[0][0] == board[0][3] && board[0][0] == board[0][4]) {
                if (board[0][0] == X) {
                    cout << "The Winner Is: BOT" << newnumbername << endl;
                    Sleep(2000);
                    cout << "quitting the program..." << endl;
                return true;
                }
                if (board[0][0] == O) {
                    cout << "You Won!!!" << endl;;
                    Sleep(2000);
                    cout << "quitting the program..." << endl;
                    return true;
                }
            }
            if (board[0][4] != ' ' && board[0][4] == board[0][3] && board[0][4] == board[0][2] && board[0][4] == board[0][1] && board[0][4] == board[0][0]) {
                if (board[0][4] == X) {
                    cout << "The Winner Is: BOT" << newnumbername << endl;
                    Sleep(2000);
                    cout << "quitting the program..." << endl;
                    return true;
                }
                if (board[0][4] == O) {
                    cout << "You Won" << endl;
                    Sleep(2000);
                    cout << "quitting the program..." << endl;
                    return true;
                }
            }
            for (int i = 0; i <= 4; i++) {
                for (int j = 0; j <=4; j++) {
                    if (board[i][j] == ' ') {
                        Is_Draw = false;
                        return false;
                        break;
                    }
                }
            }
            if (!Is_Draw) {
                return false;
            }
            if (Is_Draw) {
                cout << "Game Ends with a draw" << endl;
                Sleep(2000);
                return true;
            }

            return false;
}



bool GameOver() {
        for (int i = 0; i <= 4; i++) {
            if (board[i][0] != ' ' && board[i][0] == board[i][1] && board[i][0] == board[i][2] && board[i][0] == board[i][3] && board[i][0] == board[i][4]) {
                if (board[i][0] == O) {
                cout << "The Winner Is: " << Player_Names[n] << endl;
                Sleep(2000);
                cout << "quitting the program..." << endl;
                return true;
                }
                if (board[i][0] == X) {
                cout << "The Winner Is: " << Player_Names[(int) (!(bool) n)] << endl;
                Sleep(2000);
                cout << "quitting the program..." << endl;
                return true;
                }
            }
        }
        for (int e = 0; e <= 4; e++) {
            if (board[0][e] != ' ' && board[0][e] == board[1][e] && board[0][e] == board[2][e] && board[0][e] == board[3][e] && board[0][e] == board[4][e]) {
                if (board[0][e] == O) {
                    cout << "The Winner Is: " << Player_Names[n] << endl;
                    Sleep(2000);
                    cout << "quitting the program..." << endl;
                return true;
                }
                if (board[0][e] == X) {
                    cout << "The Winner Is: " << Player_Names[(int) (!(bool) n)];
                    Sleep(2000);
                    cout << "quitting the program..." << endl;
                return true;
                }
            }
        }
            if (board[0][0] != ' ' && board[0][0] == board[0][1] && board[0][0] == board[0][2] && board[0][0] == board[0][3] && board[0][0] == board[0][4]) {
                if (board[0][0] == O) {
                    cout << "The Winner Is: " << Player_Names[n] << endl;
                    Sleep(2000);
                    cout << "quitting the program..." << endl;
                return true;
                }
                if (board[0][0] == X) {
                    cout << "The Winner Is: " << Player_Names[(int) (!(bool) n)];
                    Sleep(2000);
                    cout << "quitting the program..." << endl;
                    return true;
                }
            }
            if (board[0][4] != ' ' && board[0][4] == board[0][3] && board[0][4] == board[0][2] && board[0][4] == board[0][1] && board[0][4] == board[0][0]) {
                if (board[0][4] == O) {
                    cout << "The Winner Is: " << Player_Names[n] << endl;
                    Sleep(2000);
                    cout << "quitting the program..." << endl;
                    return true;
                }
                if (board[0][4] == X) {
                    cout << "The Winner Is: " << Player_Names[(int) (!(bool) n)];
                    Sleep(2000);
                    cout << "quitting the program..." << endl;
                    return true;
                }
            }
            for (int i = 0; i <= 4; i++) {
                for (int j = 0; j <=4; j++) {
                    if (board[i][j] == ' ') {
                        Is_Draw = false;
                        return false;
                        break;
                    }
                }
            }
            if (!Is_Draw) {
                return false;
            }
            if (Is_Draw) {
                cout << "Game Ends with a draw" << endl;
                Sleep(2000);
                return true;
            }

            return false;
}
   
    bool draw = false;
    bool valid = true;
/*Board System*/
void tic_tac_toe_system() {
Sleep(3000);
cout << "This is our board, the origin is located at the first upper box on the left side " << endl;
Sleep(2000);
cout << "Type number of the collum, rows to move" << endl;
cout << "Hope you enjoy and good luck!" << endl;
cout << " " << endl;
cout << " " << endl;
cout << " " << endl;
cout << name_draft << " Gonna go first with O" << endl;
cout << " " << endl;
DisplayBoard();
cout << " " << endl;
cout << " " << endl;
cout << "Please Enter the number of the row and collum to move on" << endl;
cout << "Enter the rows and collums with interger number between 0 and 4 only!" << endl;
}
/**/
/*Returning*/
/*************************/
int main() { 
    shuffle(Player_Names->begin(), Player_Names->end(), g);
    cout << "**********************************" << endl;
    cout << "X -------Tic Tac Toe 5X------- O " << endl;
    cout << "**********************************" << endl;
    Sleep(5000);
    cout << "Please Enter to Continue to the game!" << endl;
    if (getchar() == '\n') {
    cout << "Game is Loading, Please Wait A Few Seconds" << endl;
    Sleep(10000);
    cout << "Game Succesfully Loaded!(*^_^*)" << endl;
    Sleep(1000);
    cout << "Please Enter Your Name both players" << endl;
    cout << "Player_1: ";
    getline(cin, Player_1);
    Player_Names[0] = Player_1;
    cout << "Player_2: ";
    getline(cin, Player_2);
    Player_Names[1] = Player_2;
    if (Player_1 == Player_2) {
        cout << "Please don't use the same name, or you could add numbers at the end to easily differitate it" << endl;
        cout << "Name suggestion for Player_1: ";
        cout << Player_1  << rand() % 1000 + 1 << endl;

        return 0;
    }
    cout << "Proccessing Each Player's Data" << endl; 
    Player_1_Scores = 0;
    Player_2_Scores = 0;
    Sleep(1000);
    leaderstats();
    Sleep(1000);
    cout << "Press Enter again to continue to the game" << endl;
    if (getchar() == '\n') {
        Sleep(2000);
        cout << "By Deciding Who go First, Let's Show it through the Roll" << endl;
        cout << "Each Players's Rolls Will Be Randomized, who has the highest number 1 rolled will go first!" << endl;
        rock_paper_scissor();
       cout <<  Player_Names[n] << " Has Rolled Into Number: " << " 1 " << endl;
       string randomplayer = Player_Names[n];
       draftplr = randomplayer;
       int CHosen_num = nil + 1;
       if (CHosen_num == 2) {
        cout << randomplayer << " Gonna Go After" << endl;
       }
       else {
        cout << randomplayer << " Gonna Go First" << endl;
       }
       Sleep(2000);
       system("cls");
    }
    Sleep(2000);
    cout << "*********Welcome to Tic Tac Toe 5X***********" << endl;
    cout << "Press the number following these choices to choose" << endl;
    cout << choices[0][0]  << endl;
    cout << choices[1][0] << endl;
    cout << choices[2][0] << endl;
    cin >> player_choice;
    int Choose_Player;
    switch(player_choice) {
        case 1: {
          tic_tac_toe_system();
            int unluck = (int) !((bool) n);
            cout << "Please Choose The Way You Want To Play: " << endl;
            cout << "1. Player VS Bot" << endl;
            cout << "2. Player VS Player" << endl;
            cin >> Choose_Player;
            if (Choose_Player == 2) {
                while (GameOver() == false) {
                    cout << Player_Names[n] << " Turn" << endl;
                    cout << "Enter The Pos Of The Rows and Collums" << endl;
                    cout << "Rows: ";
                    cin >> rows;
                    cout << " " << endl;
                    cout << "Collums: ";
                    cin >> collums;
                    while (rows < 0 || rows > 4 || collums < 0 || collums > 4 || board[collums][rows] != ' ') {
                        cout << "Invalid Number Inputed" << endl;
                        cout << "Please Try Again" << endl;
                        cin >> rows;
                        cout << "Rows: ";
                        cout << " " << endl;
                        cout << "Collums: ";
                        cin >> collums;
                    }
                    board[collums][rows] = O;
                    DisplayBoard();
                    if (GameOver() == true) {
                        cout << "quitting game..." << endl;
                        break;
                    }
                    cout << Player_Names[unluck] << " Turn" << endl;
                    cout << "Enter The Pos Of The Rows and Collums" << endl;
                    cout << "Rows: ";
                    cin >> rows2;
                    cout << " " << endl;
                    cout << "Collums: ";
                    cin >> collums2;
                    while (rows2 < 0 || rows2 > 4 || collums2 < 0 || collums2 > 4 || board[collums2][rows2] != ' ') {
                        cout << "Invalid number inputed, retry" << endl;
                        cout << "Rows: ";
                        cin >> rows2;
                        cout << " " << endl;
                        cout << "Collums: ";
                        cin >> collums2;
                    }
                    board[collums2][rows2] = X;
                    DisplayBoard();
                    if (GameOver() == true) {
                        cout << "quitting game..." << endl;
                        break;
                    }
                }
            }
            if (Choose_Player == 1) {
                Sleep(2000);
                cout << "You Will Be Playing With: BOT" << newnumbername << endl;

                Sleep(2000);
                
                cout << "Enter to roll numbers..." << endl;
                if (getchar() == '\n') {
                    Sleep(2000);
                    cout << "BOT" << newnumbername << " Has Rolled Into Number: " << rand() % 2 + 1 << endl;
                    int roll_num = rand() % 2 + 1;
                    if (roll_num == 1) {
                        cout << "BOT" << newnumbername << " Will be going first with O" << endl;
                        cout << "Here's The Board, Type Collumn And Rows Number Of Position To Move!" << endl;
                        DisplayBoard();
                        while(gameoverforbotiffirst() == false) {
                            cout << "BOT" << newnumbername << " Turn" << endl;
                            cout << "Taking Move..." << endl;
                            int n = rand() % 4;
                            int h = rand() % 4;
                            collumn_bot_move = h;
                            row_bot_move = n;
                            if (board[collumn_bot_move][row_bot_move] != ' ') {
                                cout << "Already moved!, Try Again" << endl;
                            }
                            board[collumn_bot_move][row_bot_move] = O;

                            DisplayBoard();
                            Sleep(1000);
                            cout << "Your Turn" << endl;
                            cout << "Collumn: ";
                            cin >> collums2;
                            cout << "Rows: ";
                            cin >> rows2;
                            while (rows2 < 0 or rows2 > 4 or collums2 < 0 or collums2 > 4 and board[collums2][rows2] != ' ') {
                                cout << "Invalid Number Inputed or The Box is Already Move, Retry " << endl;
                                cout << "Collumn: ";
                                cin >> collums2;
                                cout << "Rows: ";
                                cin >> rows2;
                            }
                            board[collums2][rows2] = X;
                            DisplayBoard();
                            if (gameoverforbotiffirst() == true) {
                                cout << "Quitting..." << endl;
                                Sleep(2000);
                                break;
                            }        
                        }
                    }

                        if (roll_num == 2) {
                        cout << "BOT" << newnumbername << " Will be going after with X" << endl;
                        cout << "Here's The Board, Type Collumn And Rows Number Of Position To Move!" << endl;
                        DisplayBoard();
                            while(gameoverforbotifsecond() == false) {
                                cout <<  "Your Turn" << endl;
                                cout << "Collumn: ";
                                cin >> collums;
                                cout << "Rows: ";
                                cin >> rows;
                                while (rows < 0 or rows > 4 or collums < 0 or collums > 4 and board[collums][rows] != ' ') {
                                    cout << "Invalid Number Inputed or The Box is Already Move, Retry " << endl;
                                    cout << "Collumn: ";
                                    cin >> collums;
                                    cout << "Rows: ";
                                    cin >> rows;
                                }
                                board[collums][rows] = O;
                                DisplayBoard();
                                cout << "BOT" << newnumbername << " Turn" << endl;
                                int heightt = rand() % 4;
                                int horii = rand() % 4;
                                collumn_bot_move2 = heightt;
                                rows_bot_move2 = horii;
                                if (board[collumn_bot_move2][rows_bot_move2] != ' ') {
                                    cout << "Already Moved!, try again" << endl;
                                }
                                board[collumn_bot_move2][rows_bot_move2] = X;
                                DisplayBoard();
                                if (gameoverforbotifsecond() == true) {
                                    cout << "Quitting" << endl;
                                    Sleep(2000);
                                    break;
                                }
                            }
                        }
                }
                break;
            }
        }
        case 2: {
            game_rules();
            break;
        }
        case 3: {
            cout << "Founder And Creator: " << "Lewiz" << endl;
            cout << "Press E to Show More" << endl;
            while(true) {
                if(_kbhit()) {
                    char Key = _getch();
                    if(Key == 101) {
                        creator();
                        Sleep(5000);
                    }
                }
            }
            break;
        }
        default:
        cout << "Uhh Something Goes Wrong Bud" << endl;
        break;
    }
    return 0;
}
}
