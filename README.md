# Karel-home
/*
 * This program has Karel paint a checkerboard
 */
function start(){
	paintFloor();
	turnNorth();
	lastRow();
	drawHouse();
	makeSun();
	goHome();
}
function paintFloor(){
    paint(Color.black);
    move();
    while(frontIsClear()){
        paint(Color.black);
        move();
    }
    if(frontIsBlocked()){
        paint(Color.black);
    }
    paint(Color.black);
}
function turnNorth(){
    while(notFacingNorth()){
        turnLeft();
    }
    move();
    if (rightIsBlocked()){
        turnLeft();
    } else {
        turnRight();
    }
}
function lastRow(){
    paint(Color.black);
    move();
    while(frontIsClear()){
        paint(Color.black);
        move();
    }        
    if(frontIsBlocked()){
        paint(Color.black);
    }
    paint(Color.black);
}
function drawHouse(){
    if(frontIsBlocked()){
        turnRight();
    }
    move();
    turnRight();
    bottomHouse();
    turnLeft();
    move();
    turnLeft();
    bottomHouse();
    turnRight();
    move();
    turnRight();
    roofHouse();
    turnRight();
    for(var i = 0; i < 8; i++){
        move();
    }
    turnRight();
    for(var i = 0; i < 6; i++){
        move();
    }
}
function bottomHouse(){
    for(var i = 0; i < 7; i++){
        move();
    }
    paint(Color.black);
    move();
    paint(Color.black);
    move();
    move();
    paint(Color.black);
    move();
    paint(Color.black);
    for(var i = 0; i < 7; i++){
        move();
    }
}
function roofHouse(){
    for(var i = 0; i < 6; i++){
        move();
    }
    paint(Color.black);
    move();
    paint(Color.black);
    move();
    paint(Color.black);
    move();
    paint(Color.black);
    move();
    paint(Color.black);
    move();
    paint(Color.black);
    move();
    paint(Color.black);
    turnLeft();
    move();
    turnLeft();
    move();
    paint(Color.black);
    move();
    paint(Color.black);
    move();
    paint(Color.black);
    move();
    paint(Color.black);
    move();
    paint(Color.black);
    turnRight();
    move();
    turnRight();
    move();
    paint(Color.black);
    move();
    paint(Color.black);
    move();
    paint(Color.black);
    turnLeft();
    move();
    turnLeft();
    move();
    paint(Color.black);
}
function makeSun(){
    for(var i = 0; i < 2; i++){
        putBall();
        move();
        putBall();
        move();
        putBall();
        move();
        putBall();
        turnLeft();
        move();
        turnLeft();
        putBall();
        move();
        putBall();
        move();
        putBall();
        move();
        putBall();
        turnRight();
        move();
        turnRight();
    }
}
function goHome(){
    turnRight();
    for(var i = 0; i < 17; i++){
        move();
    }
    turnRight();
    for(var i = 0; i < 6; i++){
        move();
    }
    turnAround();
}
