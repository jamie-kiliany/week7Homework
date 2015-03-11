# week7Homework
This was me playing around with our project on 3/11/15. Try looking at the code and following the instructions when you run the program! It's pretty fun, I think. Of course we can change anything and shift the questions.

boolean button=false;

PImage curtainTexture;
PImage RegalCinemas;
PImage LowesVillage;
PImage Angelika;
PImage IFC;
PImage CinemaVillage;
PImage CinemaEastVillage;
PImage FilmForum;
PImage TheatreForANewCity;
PImage MinettaLane;
PImage GeneFrankel;

PFont font;

float RegalCinemasX;
float RegalCinemasY;
float RCW;
float RCH;

float LowesVillageX;
float LowesVillageY;
float LVW;
float LVH;

float AngelikaX;
float AngelikaY;
float AW;
float AH;

float IFCX;
float IFCY;
float IFCW;
float IFCH;

float CinemaVillageX;
float CinemaVillageY;
float CinemaVillageW;
float CinemaVillageH;

float CEVX;
float CEVY;
float CEVW;
float CEVH;

float FFX;
float FFY;
float FFW;
float FFH;

float NewCityX;
float NewCityY;
float NewCityW;
float NewCityH;

float MLX;
float MLY;
float MLW;
float MLH;

float GFX;
float GFY;
float GFW;
float GFH;

int centerX=650;
int centerY=350;

int smallW=200;
int smallH=150;

int largeW=400;
int largeH=300;

int counter=0;

void setup() {
  size(1300,700);
  smooth();
   curtainTexture=loadImage("curtainTexture.jpg");
   RegalCinemas = loadImage("RegalCinemas.jpg");
   LowesVillage = loadImage("LowesVillage.jpg");
   Angelika = loadImage("angelikaCROPPED.jpg");
   IFC = loadImage("IFC.jpg");
   CinemaVillage = loadImage("cinemaVillageCROPPED.jpg");
   CinemaEastVillage = loadImage("cinemaEastVillage.jpg");
   FilmForum = loadImage("filmForum.jpg");
   TheatreForANewCity = loadImage("theatreForANewCity.jpg");
   MinettaLane = loadImage("minettaLane.jpg");
   GeneFrankel = loadImage("geneFrankel.jpg");
   imageMode(CENTER);
   frameRate(30);
}

void draw() {

if(counter==0){  
 //instructions page
    background(0);
    image(curtainTexture,width/2,height/2);
    fill(255);
    font=loadFont("CourierNewPSMT-48.vlw");
    textFont(font,48);
    text("Place the cursor over an image to enlarge it",10,300);
    text("To make your selection, press enter",150,height/2);
    text("To start over, click the mouse",200,400);
    textFont(font,72);
    text("PRESS SHIFT TO BEGIN",225, 600);
  }
  
if(button==true){//begins the program when shift is pressed
  
  if(counter==1) {
  
  background(0);
  
  fill(255);
  textFont(font,32);
  text("Which theatre",525,275); 
  text("are you",575,325);
  text("most drawn to?",525,375);
  
  //top row
  
  image(RegalCinemas,RegalCinemasX,RegalCinemasY,RCW,RCH);

  if((mouseX>50)&&(mouseX < 250)&&(mouseY>25)&&(mouseY < 175)){
    RegalCinemasX=centerX;
    RegalCinemasY=centerY;
    RCW=largeW;
    RCH=largeH;
  }else{
    RegalCinemasX=150;
    RegalCinemasY=100;
    RCW=smallW;
    RCH=smallH;
  }
  
  image(LowesVillage,LowesVillageX,LowesVillageY,LVW,LVH);
  
  if((mouseX>250)&&(mouseX<450)&&(mouseY>25)&&(mouseY<175)){
    LowesVillageX=centerX;
    LowesVillageY=centerY;
    LVW=largeW;
    LVH=largeH;
  }else{
    LowesVillageX=400;
    LowesVillageY=100;
    LVW=smallW;
    LVH=smallH;
  }
  
  image(Angelika,AngelikaX,AngelikaY,AW,AH);
  
  if((mouseX>550)&&(mouseX<750)&&(mouseY>25)&&(mouseY<175)){
    AngelikaX=centerX;
    AngelikaY=centerY;
    AW=300;
    AH=300;
  }else{
    AngelikaX=650;
    AngelikaY=100;
    AW=150;
    AH=150;
  }

  image(IFC,IFCX,IFCY,IFCW,IFCH);
  
  if((mouseX>800)&&(mouseX<1000)&&(mouseY>25)&&(mouseY<175)){
    IFCX=centerX;
    IFCY=centerY;
    IFCW=largeW;
    IFCH=largeH;
  }else{
    IFCX=900;
    IFCY=100;
    IFCW=smallW;
    IFCH=smallH;
  }
  
  image(CinemaVillage,CinemaVillageX,CinemaVillageY,CinemaVillageW,CinemaVillageH);
  
  if((mouseX>1050)&&(mouseX<1250)&&(mouseY>25)&&(mouseY<175)){
     CinemaVillageX=centerX;
     CinemaVillageY=centerY;
     CinemaVillageW=300;
     CinemaVillageH=300;
  }else{
    CinemaVillageX=1150;
    CinemaVillageY=100;
    CinemaVillageW=150;
    CinemaVillageH=150;
  }
  
  //bottom row
  image(CinemaEastVillage,CEVX,CEVY,CEVW,CEVH);
  
   if((mouseX>50)&&(mouseX < 250)&&(mouseY>525)&&(mouseY < 675)){
    CEVX=centerX;
    CEVY=centerY;
    CEVW=largeW;
    CEVH=largeH;
  }else{
   CEVX=150;
  CEVY=600;
  CEVW=smallW;
  CEVH=smallH;
  }
  
  image(FilmForum,FFX,FFY,FFW,FFH);

  if((mouseX>300)&&(mouseX < 500)&&(mouseY>525)&&(mouseY < 675)){
    FFX=centerX;
    FFY=centerY;
    FFW=largeW;
    FFH=largeH;
  }else{
     FFX=400;
  FFY=600;
  FFW=smallW;
  FFH=smallH;
  }
  
  image(TheatreForANewCity,NewCityX,NewCityY,NewCityW,NewCityH);
  
  if((mouseX>550)&&(mouseX < 750)&&(mouseY>525)&&(mouseY < 675)){
    NewCityX=centerX;
    NewCityY=centerY;
    NewCityW=largeW;
    NewCityH=largeH;
  }else{
    NewCityX=650;
    NewCityY=600;
    NewCityW=smallW;
    NewCityH=smallH;
  }
  
  image(MinettaLane,MLX,MLY,MLW,MLH);
  
  if((mouseX>800)&&(mouseX < 1000)&&(mouseY>525)&&(mouseY < 675)){
    MLX=centerX;
    MLY=centerY;
    MLW=largeW;
    MLH=largeH;
  }else{
    MLX=900;
    MLY=600;
    MLW=smallW;
    MLH=smallH;
  }
  
  image(GeneFrankel,GFX,GFY,GFW,GFH);
  
   if((mouseX>1050)&&(mouseX < 1250)&&(mouseY>525)&&(mouseY < 675)){
     GFX=centerX;
     GFY=centerY;
     GFW=largeW;
     GFH=largeH;
   }else{
    GFX=1150;
    GFY=600;
    GFW=smallW;
    GFH=smallH;
   }
  }
  
  if(counter==12){ //this is placed before other counters in order to completely cover the window - no lingering photos, this is the second question
    background(0);
    textFont(font,48);
    text("How many Oscar-nominated films",250,325);
    text("did you see this year?",325,375);
  }
  
  if (counter==2){
    background(0);
    image(RegalCinemas,RegalCinemasX,RegalCinemasY,RCW,RCH);
    RegalCinemasX=centerX;
    RegalCinemasY=centerY;
    RCW=largeW;
    RCH=largeH;
    textFont(font,32);
    text("Regal Cinemas",10,350);
    text("Press right arrow",10,400); 
    text("to continue",10,450);
  }
  if (counter==3){
    background(0);
    image(LowesVillage,LowesVillageX,LowesVillageY,LVW,LVH);
    LowesVillageX=centerX;
    LowesVillageY=centerY;
    LVW=largeW;
    LVH=largeH;
    textFont(font,32);
    text("Lowes Village",10,350);
    text("Press right arrow",10,400); 
    text("to continue",10,450);
  }
  if(counter==4){
    background(0);
    image(Angelika,AngelikaX,AngelikaY,AW,AH);
    AngelikaX=centerX;
    AngelikaY=centerY;
    AW=300;
    AH=300;
    textFont(font,32);
    text("The Angelika",10,350);
    text("Press right arrow",10,400); 
    text("to continue",10,450);
  }
  if(counter==5){
    background(0);
    image(IFC,IFCX,IFCY,IFCW,IFCH);
    IFCX=centerX;
    IFCY=centerY;
    IFCW=largeW;
    IFCH=largeH;
    textFont(font,32);
    text("IFC",10,350);
    text("Press right arrow",10,400); 
    text("to continue",10,450);
  }
  if(counter==6){
    background(0);
    image(CinemaVillage,CinemaVillageX,CinemaVillageY,CinemaVillageW,CinemaVillageH);
    CinemaVillageX=centerX;
    CinemaVillageY=centerY;
    CinemaVillageW=300;
    CinemaVillageH=300;
    textFont(font,32);
    text("Cinema Village",10,350);
    text("Press right arrow",10,400); 
    text("to continue",10,450);
  }
  if(counter==7){
    background(0);
    image(CinemaEastVillage,CEVX,CEVY,CEVW,CEVY);
    CEVX=centerX;
    CEVY=centerY;
    CEVW=largeW;
    CEVH=largeH;
    textFont(font,32);
    text("Cinema Village East",10,350);
    text("Press right arrow",10,400); 
    text("to continue",10,450);
  }
  if(counter==8){
    background(0);
    image(FilmForum,FFX,FFY,FFW,FFH);
    FFX=mouseX;//just playing around with options here
    FFY=mouseY;
    FFW=largeW;
    FFH=largeH;
    textFont(font,32);
    text("Film Forum",10,350);
    text("Press right arrow",10,400); 
    text("to continue",10,450);
  }
  if(counter==9){
    background(0);
    image(TheatreForANewCity,NewCityX,NewCityY,NewCityW,NewCityH);
    NewCityX=centerX;
    NewCityY=centerY;
    NewCityW=largeW;
    NewCityH=largeH;
    textFont(font,32);
    text("Theatre for a",10,300);
    text("New City",10,350);
    text("Press right arrow",10,400); 
    text("to continue",10,450);
  }
  if(counter==10){
    background(0);
    image(MinettaLane,MLX,MLY,MLW,MLH);
    MLX+=1;//animates the photo across the x-axis starting in the center
    MLY=centerY;
    MLW=largeW;
    MLH=largeH;
    textFont(font,32);
    text("Minetta Lane Theatre",10,350);
    text("Press right arrow",10,400); 
    text("to continue",10,450);
  }
  if(counter==11){
    background(0);
    image(GeneFrankel,GFX,GFY,GFW,GFH);
    GFX=centerX;
    GFY-=10;
    GFW=largeW;
    GFH=largeH;
    if(GFY<-150){//plays with animating the photo upwards on centerY, loops back around
      GFY=850;
    }
    textFont(font,32);
    text("Gene Frankel",10,350);
    text("Press right arrow",10,400); 
    text("to continue",10,450);
  
  }
  
  println("counter:"+counter);
}
}


void keyPressed() {
  
  if(key==CODED){
    if(keyCode==SHIFT){
      button=!button;
      counter++;
    }
  }
  
  if((key==ENTER)&&(RegalCinemasX==centerX)&&(RegalCinemasY==centerY)){
    counter++;
  }
  if((key==ENTER)&&(LowesVillageX==centerX)&&(LowesVillageY==centerY)){
    counter+=2;
  }
  if((key==ENTER)&&(AngelikaX==centerX)&&(AngelikaY==centerY)){
    counter+=3;
  }
  if((key==ENTER)&&(IFCX==centerX)&&(IFCY==centerY)){
    counter+=4;
  }
  if((key==ENTER)&&(CinemaVillageX==centerX)&&(CinemaVillageY==centerY)){
    counter+=5;
  }
  if((key==ENTER)&&(CEVX==centerX)&&(CEVY==centerY)){
    counter+=6;
  }
  if((key==ENTER)&&(FFX==centerX)&&(FFY==centerY)){
    counter+=7;
  }
  if((key==ENTER)&&(NewCityX==centerX)&&(NewCityY==centerY)){
    counter+=8;
  }
  if((key==ENTER)&&(MLX==centerX)&&(MLY==centerY)){
    counter+=9;
  }
  if((key==ENTER)&&(GFX==centerX)&&(GFY==centerY)){
    counter+=10;
  }if(key == CODED) {
    if ((keyCode == RIGHT)&&((counter==2)||(counter==3)||(counter==4)||(counter==5)||(counter==6)||(counter==7)||(counter==8)||(counter==9)||(counter==10)||(counter==11))) {
    counter=12;
  }
  }
}

void mousePressed() { //resets the program to the beginning
  button=false;
  counter=0;
}

