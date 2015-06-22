# rps1
rock paper scissors

////////////////////////////////////////////////
/*   Provided Code - Please Don't Edit   */
////////////////////////////////////////////////
'use strict';

function getInput() {
    console.log("Please choose either 'rock', 'paper', or 'scissors'.");
    return prompt();
}
function randomPlay() {
    var randomNumber = Math.random();
    if (randomNumber < 0.33) {
        return "rock";
    } else if (randomNumber < 0.66) {
        return "paper";
    } else {
        return "scissors";
    }
}
////////////////////////////////////////////////
/*           Write Your Code Below            */
////////////////////////////////////////////////

function getPlayerMove(move) {
    return move || getInput();
}

function getComputerMove(move) {
    return move || randomPlay();
}

var playerMove = getPlayerMove();
var computerMove = getComputerMove();
var winner;
/*I don't get line above or below think it should be var winner = function(getWinner(playerMove,computerMove))*/
function getWinner(playerMove,computerMove) {
    var winner = function (getPlayerMove, getComputerMove) {
        if(playerMove === computerMove) {
            return "Tie";
        } else if (playerMove === "rock") {

            if(computerMove === "scissors") {
                return "playerWins"; 
        } else { 
            return "computerWins";
            } 
        } else if(playerMove === "paper") { 
            if(computerMove === "rock") {
                return "playerWins"; 
            } else { 
                return "computerWins"; 
            }   
        }
        else if(playerMove === "scissors") {
            if (computerMove === "paper") {
                return "playerWins";
            } else { 
                return "computerWins";
            }
        }
    }
    /*don't get below line*/
    return winner;
}

function playToFive() {
    console.log("Let's play Rock, Paper, Scissors");
    var playerWins = 0;
    var computerWins = 0;

`       while (playerWins !== 5 || computerWins !==5) {
        if(playerMove || computerMove === "Tie") {
            null
        } else if (playerMove === playerWins) {
            playerWins ++
        } else {
            computerWins ++
        }
}
    return [playerWins, computerWins];


