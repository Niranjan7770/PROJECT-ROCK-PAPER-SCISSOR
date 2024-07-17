#PROJECT ROCK PAPER SCISSOR

#include<bits/stdc++.h>

#define Rock 1
#define Paper 2
#define Scissor 3

using namespace std;

int main() {
  
srand((unsigned int) time(NULL));
 
 int player_throw = 0;
 int ai_throw = 0;
 bool draw = false;
 
 do{
cout<<"Select Your Throw :" <<endl;
cout<<"1.Rock " <<endl;
cout<<"2.Paper" <<endl;
cout<<"3.Scissor" <<endl;
cout<<"Selection  :" <<endl;
cin>>player_throw;

cout<<endl;

ai_throw = (rand() % 3) + 1;

if(ai_throw == Rock){
    cout<<"ai throws Rock"<<endl;
}
else if(ai_throw == Paper){
    cout<<"ai throws Paper"<<endl;
}
else if(ai_throw == Scissor){
    cout<<"ai throws Scissor"<<endl;
}
draw = false;
if(player_throw == ai_throw){
    draw = true;
    cout<<"draw! Play again"<<endl;
}
else if((player_throw == Rock) && (ai_throw == Scissor)){
    cout<<"Rock beats scissors. You win"<<endl;
}
else if((player_throw == Scissor) && (ai_throw == Rock)){
    cout<<"Rock beats Scissor. You Lose"<<endl;
}
else if((player_throw == Rock) && (ai_throw == Paper)){
    cout<<"Paper beats Rock. You Lose"<<endl;
}
else if((player_throw == Paper) && (ai_throw == Rock)){
    cout<<"Paper beats Rock. You Win"<<endl;
}
else if((player_throw == Scissor) && (ai_throw == Paper)){
    cout<<"Scissor beats Paper. You Win"<<endl;
}
else if((player_throw == Paper) && (ai_throw == Scissor)){
    cout<<"Scissor beats Paper. You Lose"<<endl;
}
 }while(draw);
 
    return 0;
}

