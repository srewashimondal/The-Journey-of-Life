#include <iostream>
#include <string>
#include <vector>
#include <cstdlib>
#include <ctime>
#include <cctype>
using namespace std;

/*
  Name: Srewashi Mondal, Saanavi Goyal
  Finished at 3:29AM! LOL 
*/

int score = 0;

void GameIntro(string& name)
{
    cout << "Hi! Welcome to the game 'The Journey of Life'! What is your first name?" << endl;
    cin >> name;
    cout << "Welcome " << name << "! Imagine, you have been rude to your family and friends, wasting food and items, and spending lavishly only on yourself. To teach you a lesson, the world decides that today you will wake up in a dream reality you can't escape➰." << endl;
cout << endl;
cout << "Here, you are lost without your family and resources😮. You must explore the 10 given locations and win each scenario so you can get food and water🍱. You need get a score of 10, 1 from each location to be able to return back to your lavish lifestyle🤩. This game will teach you to be grateful and appreciative of the people and resources around you. You will learn to work hard!" << endl;

    cout << endl;
    cout << "Here is a map of your Alternate Reality🗺️:" << endl;
    cout << endl;

    // cout << "|--------------------------------|" << endl;
    // cout << "|  HILL⛰️  |       FOREST🍂       |" << endl;
    // cout << "|--------------------------------|" << endl;
    // cout << "|    SCHOOL🏫    |    RIVER🗾    |" << endl;
    // cout << "|--------------------------------|" << endl;
    // cout << "|   BUILDING🌆    |     DESERT🌵 |" << endl;
    // cout << "|--------------------------------|" << endl;
    // cout << "|    CAVE🗿     |     BEACH 🏖️    |" << endl;
    // cout << "|------------------------------- |" << endl;
    // cout << "|    VILLAGE🌾  |     CASTLE🏰   |" << endl;
    // cout << "|------------------------------- |" << endl;

    cout << endl;
    cout << "Choose a place from the map. Where do you want to go first, " << name << "? Use UPPERCASE only." << endl;
}

class Player
{
public:
    string name;
    int score = 0;

    string getName()
    {
        return name;
    }

    int getScore()
    {
        return score;
    }

    void setScore(int newScore)
    {
        score = newScore;
    }

    // void incrementScore()
    // {
    //     score++;
    //     cout << "Your current score is: " << score << endl;
    // }
};

class MapLocation
{
public:
    string location;
    const string river = "RIVER";
    const string hill = "HILL";
    const string forest = "FOREST";
    const string building = "BUILDING";
    const string beach = "BEACH";
    const string desert = "DESERT";
    const string castle = "CASTLE";
    const string village = "VILLAGE";
    const string school = "SCHOOL";
    const string cave = "CAVE";

    void selectLocation()
    {
        cin >> location;
    }
};

void CoinFlip(Player player)
{
    string guess;
    srand(time(0));
    int flip = rand() % 2;

    cout << endl;
    cout << "Let's play Coin Flip game!🪙 I will spin the coin and you have to guess if it's Heads or Tails. You have only one try." << endl;
    cout << "I spin the coin. Make your guess! Is it Heads or Tails? Write your answer below. (Use UPPERCASE)" << endl;

    cout << endl;
    cin >> guess;

    string coinResult;

    if (flip == 0)
    {
      coinResult = "HEADS";
    }
    else
    {
      coinResult = "TAILS";
    }
  
    cout << "The coin landed on: " << coinResult << endl;

    while (guess != coinResult)
    {
      cout << "Oops! You guessed it wrong. Try again!🥲" << endl;
      cout << "Make your guess! Is it Heads or Tails? Write your answer below. (Use UPPERCASE)" << endl;

    cin >> guess;

    string coinResult;
    }
  
    if (guess == coinResult)
    {
      cout << "Congratulations! You guessed it right!🤩" << endl;
      // player.incrementScore();
      score++;
      cout << "Your current score is: " << score << endl;
    }
    
}

void RockPaperGame(Player& player) // hill
{
  const int ROCK = 1;
  const int PAPER = 2;
  const int SCISSORS = 3;

  cout << "Rock, Paper, and Scissors Game! "<< endl;

  int userRPS;
  bool gameOver = false;

  while (!gameOver)
  {
    cout << "Choose one of the following options: rock, paper, or scissors (just type in the corresponding number of your choice)" << endl;
    cout << "1. Rock🪨" << endl;
    cout << "2. Paper📄" << endl;
    cout << "3. Scissors✂️" << endl;
    cin >> userRPS;

    srand(time(0));
    int computerPick = rand() % 3 + 1;

    if (userRPS == ROCK && computerPick == PAPER)
    {
      cout << "Computer Wins!🖥️ Paper wraps Rock.Try again." << endl;
    }
    else if (userRPS == PAPER && computerPick == SCISSORS)
    {
      cout << "Computer Wins!🖥️ Scissors cut Paper. Try again." << endl;
    }
    else if (userRPS == SCISSORS && computerPick == ROCK)
    {
      cout << "Computer Wins!🖥️ Rock smashes Scissors. Try again." << endl;
    }
    else if (userRPS == ROCK && computerPick == SCISSORS)
    {
      cout << "You Win!🎈 Rock smashes Scissors." << endl;
      score++;
      cout << "Your current score is: " << player.getScore() << endl;
      gameOver = true;
    }
    else if (userRPS == PAPER && computerPick == ROCK)
    {
      cout << "You Win!🎈 Paper wraps Rock." << endl;
      score++;
      cout << "Your current score is: " << score << endl;
      gameOver = true;
    }
    else if (userRPS == SCISSORS && computerPick == PAPER)
    {
      cout << "You Win!🎈 Scissors cut Paper." << endl;
      score++;
      cout << "Your current score is: " << player.getScore() << endl;
      gameOver = true;
    }
    else if (userRPS == computerPick)
    {
      cout << "It's a tie!🫠 Let's play again." << endl;
      cout << endl;
    }
  }
}

void NumberGuessing(Player player)
{
    int userGuess = 0;
	srand(time(0));
	int computerNum = rand() % 51;
 
  cout << "Let's play a Random Number Guessing game." << endl;
  cout << "Guess a number and I will tell you if it's too high or low to guide you!" << endl;
  cout << "Hmm I am thinking of an integer between 0 and 50. What number am I thinking of?" << endl;

	while (userGuess != computerNum)
	{
		cout << "Enter your guess!";
    cout << endl;
		cin >> userGuess;

		if (userGuess == computerNum)
    {
			cout << "Yes, the number is\t" << computerNum << endl;
      score++;
      cout << "Your current score is: " << score << endl;
    }
		else if (userGuess > computerNum)
    {
			cout << "Your number is too high📈" << endl;
    }
		else
    {
			cout << "Your number is too low📉" << endl;
    }
	}
}

void LetterGuessingGame(Player player)
{
    srand(time(0));
	char randomLetter = 'A' + rand() % 26;
  char inputLetter;
  //upper only!
  
  cout << "Let's play a Letter Guessing Game! Chose a letter to make a guess!🤔" << endl;

	while (inputLetter != randomLetter)
	{
    cout << endl;
    cin >> inputLetter;
    if (inputLetter < 'A' || inputLetter > 'Z')
    {
        cout << "Invalid input! Please enter a letter from A to Z." << endl;
    }
    else if (randomLetter > inputLetter)
    {
        cout << "Your guess is too low. Try again!" << endl;
    }
    else if (randomLetter < inputLetter)
    {
        cout << "Your guess is too high. Try again!" << endl;
    }
    else
    {
        cout << "Congratulations!🤗 You guessed the Secret Letter '" << randomLetter << "'!" << endl;
      //player.incrementScore();
      score++;
      cout << "Your current score is: " << score << endl;
  }
}
}

void LetterGuessingGame2 (Player player)
{
    srand(time(0));
	char randomLetter = 'A' + rand() % 26;
  char inputLetter;
  //upper only!
  
  cout << "Let's play a Letter Guessing Game! Chose a letter to make a guess!🤔" << endl;

	while (inputLetter != randomLetter)
	{
    cout << endl;
    cin >> inputLetter;
    if (inputLetter < 'A' || inputLetter > 'Z')
    {
        cout << "Invalid input! Please enter a letter from A to Z." << endl;
    }
    else if (randomLetter > inputLetter)
    {
        cout << "Your guess is too low. Try again!" << endl;
    }
    else if (randomLetter < inputLetter)
    {
        cout << "Your guess is too high. Try again!" << endl;
    }
    else
    {
        cout << "Congratulations!🤗 You guessed the Secret Letter '" << randomLetter << "'!" << endl;
      cout << endl;
      //player.incrementScore();
      score++;
      cout << "Your current score is: " << score << endl;
  }
}
}

void RiddleGameOne(Player player)
{
    string riddle1Input;
    
  cout << "C'mon, let's answer a riddle now! Here is the riddle: " << endl;
  cout << endl;
  cout << "I am taken for granted, yet I'm truly one of a kind," << endl;
  cout << "I provide endless opportunities, and memories I bind.🫣" << endl;
  cout << "From the beauty of nature to loved ones near," << endl;
  cout << "I am a precious gift, make it crystal clear💎." << endl;
  cout << "What am I? Type your one word answer below." << endl;

  cout << endl;
  cin >> riddle1Input;

  while (riddle1Input != "time" && riddle1Input != "Time" && riddle1Input != "TIME")
  {
    cout << "Try again! Hint: It has four letters and it never stops for anyone. Tick tock tick tock. ____ is ticking⏰!" << endl;
    cin >> riddle1Input;
  }
  
  cout << "Correct! The answer was time! Time is a precious gift that we should appreciate and make the most of every day." ;
  cout << "Be grateful of the time you have with your loved ones.🫶🏻" << endl;
  cout << endl;
  //player.incrementScore();
  score++;
  cout << "Your current score is: " << score << endl;
}

void RiddleGameTwo(Player player)
{
  string riddle2Input;
    
  cout << "C'mon, let's answer a riddle now! Here is the riddle: " << endl;
  cout << "I'm something we consume each day," << endl;
  cout << "On plates and bowls, I often lay.🍽️" << endl;
  cout << "A tasty treat, a delight for all," << endl;
  cout << "Appreciate me, big or small.🥡" << endl;
  cout << "What am I? Type your one word answer below." << endl;

  cout << endl;

  cin >> riddle2Input;

  while (riddle2Input != "food" && riddle2Input != "Food" && riddle2Input != "FOOD")
  {
    cout << "Try again! Hint: It has four letters. Starts with the letter F and ends with D! It's for breakfast, lunch, and dinner!🌮";
    cout << endl;
    cin >> riddle2Input;
  }

  cout << "Correct! The answer was food 🍲! We need to eat healthy food ti nourish our bodies. We cannot be wasteful of food and instead, be grateful." << endl;
  cout << endl;
  //player.incrementScore();
  score++;
  cout << "Your current score is: " << score << endl;
    
}

void RiddleGameThree(Player player)
{
  string guessForRiddle;
  
  cout << endl;
  cout << "C'mon, let's answer a riddle now! Here is the riddle: " << endl;
  cout << endl;
  cout << "I am a resource, both finite and grand" << endl;
  cout << "In hands of the wise, I multiply like sand⏳." << endl;
  cout << "If spent with caution, I bring joy and gain, But squandered recklessly, I cause only pain." << endl;
  cout << "To secure your future, and make dreams come true.🫀 What am I? Type your one word answer below."; 
  cout << "Note: Use UPPERCASE only!" << endl;

  cout << endl;
  cin >> guessForRiddle;
  cout << endl;

  while (guessForRiddle != "MONEY" && guessForRiddle != "Money" && guessForRiddle != "money")
  {
     cout << "Sorry! Your guess is not quite right! Hint: It starts with M, ends with Y and has 5 letters. It is accepted as payment for goods and services🤑. We trade in _____ for whatever we want to buy." << endl;
    cout << "Try again!" << endl;

    cout << endl;
    cin >> guessForRiddle;
  }
  
  cout << "YAY! You guessed the answer right! Money is a resource that is finite and valuable. When managed wisely, money can multiply and bring joy and gain. However, if money is squandered recklessly 🤑 or spent without caution, it can lead to financial difficulties and pain." << endl;
cout << endl;
    
cout << "By spending money 💰 wisely, individuals can secure their future, fulfill their dreams, and ensure a stable financial situation.You can now move on to the next location in the map!" << endl;
  cout << endl;
  //player.incrementScore();
  score++;
  cout << "Your current score is: " << score << endl;
}

void MCQOne(Player player)
{
    string mcqResponse1;
  cout << endl;
  cout << "Here, you have to answer a multiple choice question correctly to earn a point." << endl;
  cout << endl;
  cout << "Here is the scenario: You are walking down the street and you see a homeless man on the road. You already had your lunch, but you were offered a whole box of pizza 🍕 as well, 5 minutes ago. What will you do now since now you have extra food?" << endl;
  cout << "Option 1: Be selfish. Walk away from homeless man and eat the pizza yourself." << endl;
  cout << "Option 2: Go up to homeless man and be rude to him." << endl;
  cout << "Option 3: Be kind to the homeless man and share your pizza with him." << endl;
  cout << endl;
  cout << "Which option will you pick? Just type the number (1,2,3) of the option you choose below." << endl;

  cout << endl;
  cin >> mcqResponse1;

  while (mcqResponse1 != "3")
  {
    cout << "Try again! Which answer is correct? Just type the number of the option you choose below." << endl;
    cin >> mcqResponse1;
  }

  cout << "Correct! Option 3 is correct. We should be kind to everyone around us." << endl;
  //player.incrementScore();
  score++;
  cout << "Your current score is: " << score << endl;
}

void MCQTwo(Player player)
{
    string mcqResponse2;
  cout << endl;
  cout << "Here, you have to answer a multiple choice question correctly to earn a point." << endl;
  cout << endl;
  cout << "Here is the scenario: You are walking through a mall and an old lady smiles and holds the door for you. What should you say/do in return?" << endl;
  cout << "Option 1: Smile and politely say Thank you!" << endl;
  cout << "Option 2: Walk away." << endl;
  cout << "Option 3: Roll your eyes and walk through the door without saying anything." << endl;
  cout << endl;
  cout << "Which option will you pick? Just type the number (1,2,3) of the option you choose below." << endl;

  cout << endl;

  cout << endl;
  cin >> mcqResponse2;

  while (mcqResponse2 != "1")
  {
    cout << "Try again! Which answer is correct? Just type the number of the option you choose below." << endl;
    cin >> mcqResponse2;
  }

  cout << "Correct! Option 1 is correct. We should be kind to everyone around us." << endl;
  //player.incrementScore();
  score++;
  cout << "Your current score is: " << score << endl;
}

int main()
{
  // bool isGameOver = false;
  
  string playerName;
  GameIntro(playerName);

  Player player;
  player.name = playerName;

  MapLocation mapLocation;
  //mapLocation.location = mapLocation.startingLocation;

  while (score < 10)
  {
    // if (player.getScore() == 10)
    // {
    //   isGameOver = true;
    // }
    
    cout << "|--------------------------------|" << endl;
    cout << "|  HILL⛰️  |       FOREST🍂       |" << endl;
    cout << "|--------------------------------|" << endl;
    cout << "|    SCHOOL🏫    |    RIVER🗾    |" << endl;
    cout << "|--------------------------------|" << endl;
    cout << "|   BUILDING🌆    |     DESERT🌵 |" << endl;
    cout << "|--------------------------------|" << endl;
    cout << "|    CAVE🗿     |     BEACH 🏖️    |" << endl;
    cout << "|------------------------------- |" << endl;
    cout << "|    VILLAGE🌾  |     CASTLE🏰   |" << endl;
    cout << "|------------------------------- |" << endl;

    cout << endl;
    
    cout << "Choose your next location from the map:" << endl;
    mapLocation.selectLocation();
    
    cout << endl;
    cout << "---------------------------------------------" << endl;
    cout << "You are currently at: " << mapLocation.location << endl;
    cout << endl;

    if (mapLocation.location == mapLocation.river)
    {
      cout << "You find yourself near a river!🗾 The natural soundtrack calls in for a game of coin flip! Win the game, get a point and get to move on to the next location! The sooner you score 9 points, the sooner you get home! " << endl;
      CoinFlip(player);
    }
    else if (mapLocation.location == mapLocation.hill)
    {
      cout << "You find yourself on the top of the hill!⛰️ The sky is above you, and the ground reality seems too far away. You still are not back home, maybe its time for a Rock Paper Scissors Game. Let's Go!!" << endl;
      cout << endl;
      RockPaperGame(player);
    }
    else if (mapLocation.location == mapLocation.forest)
    {
      cout << "There are tall dark trees all around you, and you find yourself in a forest.🪵 You are not home anymore but I know you want to be. Win this Number Guessing Game and get home sooner!" << endl;
      NumberGuessing(player);
    }
    else if (mapLocation.location == mapLocation.building)
    {
       cout << "This time, you are in a tall building🌆. There is only one way you can get out of this building, guess the letter correctly!" << endl;
      LetterGuessingGame(player);
    }
    else if (mapLocation.location == mapLocation.beach)
    {
      cout << "There is water and sand, you knew you came to a beach!🏖️ Well, you are here until you solve the next riddle." << endl;
    cout << endl;
      RiddleGameOne(player);
    }
    else if (mapLocation.location == mapLocation.desert)
    {
      cout << "The sun is hot and there is no living thing that can be seen anymore.🌵 You're in desert now! To get out, you must guess the seccret letter for Letter Guessing Game! Once you win, you might be able to get home." << endl;
      RiddleGameTwo(player);
    }
    else if (mapLocation.location == mapLocation.castle)
    {
      cout << "It is a large building, looks like your home. You thought you already here? Not yet. It is a castle🏰 built with dreams, and you are caged here. You can solve this riddle and get your way out!" << endl;
      RiddleGameThree(player);
    }
    else if (mapLocation.location == mapLocation.village)
    {
      cout << "It's easy to live in luxury, but the struggles at a village are real.🌾 You are lucky that you don't have to live here, but you should know it is difficult to get out of here. Answer the multiple choice below, and get to your luxuries ASAP!" << endl;
      MCQOne(player);
    }
    else if (mapLocation.location == mapLocation.school)
    {
      cout << "Back to School! You want to be home, but we all need to get the degree!🏫 Don't worry, it won't be four years long, just one right answer to the Multiple Choice. You know how exams are!" << endl;
      MCQTwo(player);
    }
    else if (mapLocation.location == mapLocation.cave)
    {
      cout << "Its dark here in this cave, and trust me you want to get home soon!🗿 Guess the secret letter once more, and you will be out of here. The sooner you guess it, the sooner you will be back home!" << endl;
      LetterGuessingGame2(player);
    }
    else
    {
      cout << "Invalid location. Please choose a valid location from the map." << endl;
    }

    cout << "---------------------------------------------" << endl;
    cout << endl;
  }

  cout << "YAY! You reached home finally 🥳. You can live your lavish life again now. Just keep in mind the struggles of others, and be kind to the people around you. Be grateful to what you have, because you never know when you will lose it. Hopefully, this game teaches gratitude and humbleness. Thank you for playing 'The Journey of Life'! See you next time! 😊" << endl;
  cout << endl;
  cout << "Final Score: " << score << "/10 💯" << endl;

  return 0;
}
