# comp110-worksheet-B

targetWord <-- "WORD"
secretWord <-- ""
likenessScore <-- 0
wordLength <-- 4
attemptsRemaining <-- 3

if (player clicked on a word)
{
	secretWord <-- clickedWord
	//runs a loop for an amount of times which is equal to the value of the wordLength variable
	//stores each number the loop is going through in a variable called number
	for number in wordLength
	{
		if (secretWord.letter(with position of number) is equal to targetWord.letter(with position of number))
			likenessScore = likenessScore + 1
	}
	//compares the likeness score to the length of the word
	if (likenessScore is smaller than wordLength)
	{
		//checks the number of attempts left
		if (attemptsRemaining is bigger than 1)
		{
			attemptsRemaining = attemptsRemaining - 1
			display("Entry denied.")
			display("Likeness=" + likenessScore)
			likenessScore <-- 0		//resets the likenessScore variable for the next run
		}
		else
		{
			display("Game Over.")
			End Program
		}
	}
	else
	{
		display("Password Accepted.")
		Execute Winning Condition
		End Program
	}
}

![alt text](https://github.com/JoachimRayski/comp110-worksheet-B/blob/master/Terminal%20Hacking%20Flowchart.png?raw=true)
