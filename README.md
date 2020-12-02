function game() {
   var games;  
   let playerScore;
let computerScore;

    
function playRound(playerSelection, computerAnswer){
  var computerAnswer = computerPlay();
  var playerSelection = prompt("Choose your weapon", "Rock Paper Scissors");
  playerSelection = playerSelection.toLowerCase();
 

   //testing to see whether I can put the computerPlay function inside the playRound function; i did this but did not like undefined vars... computersocre an player score so now added.. afer adding playerScore and computerScore var.s no error message: next step... can i add the case changer?...added lines re: playerSeledtion and changing to lower case...added games() with loop for five games it works... next step... show who wins... added report playerScore... when i add this i get a reference error should i move variables to top? when i do this get computerPlay is not defined... moved computerPlay inside playRound function...got report is not defined...changed report to alert and played one game reported score and then stopped//
    

function computerPlay(computerSelection)
{var computerSelection = ["rock", "paper", "scissors"];
return computerSelection[Math.floor(Math.random()*computerSelection.length)];    
}
    
  if (playerSelection == "rock" && computerAnswer == "paper"){
    computerScore++;
    alert ("You lose. Paper smothers rock.")
  } else if
    (playerSelection == "rock" && computerAnswer == "scissors") {
      playerScore++;
      alert ("You win. Rock smashes scissors.")
    } else if
      (playerSelection == "paper" && computerAnswer == "scissors") {
        computerScore++;
        alert ("You lose. Scissors cut paper.")
      } else if 
        (playerSelection == "paper" && computerAnswer == "rock"){ 
          playerScore++;
          alert ("You win. Paper smothers rock.")} else if
          (playerSelection == "scissors" && computerAnswer == "rock") {
            computerScore++;
            alert ("You lose. Rock smashes scissors.")
          } else if
          (playerSelection == "scissors" && computerAnswer == "paper") {
            playerScore++;
            alert ("You win. Scissors cut paper.")
          }
  else 
      {alert ("Tie game.")
 //moving playerscore stuff here?? wondering if that's why it's not cumulative.. when i move it here it gives result only after tie game//         
      } 
      
  //in this location it returns score for each game but not cumulative//  
   }
  playerScore=0;
  computerScore=0;
for (games = 0; games < 5; games++) {playRound();
                                     
 }
  alert ("You scored " + playerScore +";" + "Computer scored " + computerScore);
  //the game() function needs to 1.add up player wins and computer wins 2.gigure out which is the most 3.report the winner; just lifted this code from someone on t//
   
}
