# Quiz on Harry potter web-series.

var readlineSync = require("readline-sync");
var score = 0;
const chalk = require("chalk");
const log = console.log;
var userName = readlineSync.question("what is your name? ")
log("welcome", chalk.blue(userName))
log("Let's play the game.")
log("-----------")



var scoresHere= [
  {
    name: "jinesh",
    scored: 7,
  },
  {
    name: "lokesh",
    scored: 6,
  }
]



function quiz(question,answer){
  var list  = readlineSync.question(question.question + question.option)
  if(list === answer){
    log(chalk.yellow("Correct answer!"))
    score = score+1;
  }else{
    log(chalk.red("Wrong answer!"))
  }
  log( "your score is", chalk.green(score))
}

var questions =[
  {
    question: "Who played lord voldemort in the movie?\n",
    option: "a) jeremy irons \nb) ralph fiennes ",
    answer: "b"           
  },
  {
    question: "How do you summon a patronus?\n",
     option: "a) patronia paternus \nb) expecto patronum ",
     answer: "b"
  },
  {
    question:"Who has given Harry potter the Invisibility clock?\n",
    option: "a) Dumbledore \nb) Dobby ",
    answer: "a"
  },
  {
    question:"which professor teaches flying lessons?\n",
    option: "a) Mrs. Norris \nb) Jones ",
    answer: "a"
  },
  {
    question:"what's the name of flich's cat?\n",
    option: "a) Charity burbage \nb) Madam hooch ",
    answer: "b"
  },
  {
    question:"How many Whisely's sibling are there?\n",
    option: "a) 7 \nb) 10 ",
    answer: "a"
  },
  {
    question:"What does the spell 'Obliviate' do?\n",
    option: "a) Removes parts of someone's memory \nb) Destroy objects ",
    answer: "a"
  },
]

for(var i=0; i<questions.length; i++){ 
quiz(questions[i],questions[i].answer)
}

log(chalk.blue("Top score is"),scoresHere[0].scored, "by",chalk.blue.bgRed.bold(scoresHere[0].name))