# Tic-tac-rock-paper-toe
//Tic tac toe and also rock paper scissors

using System;

public class Program
{
	public static void Main()
	{
		//coding is very hard
		Console.Clear();
		string input;
		string anythingbesidesthat = "anything else";
		string player;
		string exit = "exit";
		string game;
		string leave = "leave";
		string reset = "reset";
		string rockpaperscissors = "rockpaperscissors";
		string tictactoe = "tictactoe";
		Console.WriteLine("(all lowercase) tictactoe or rockpaperscissors? (or type anything else to exit)");
		game = Console.ReadLine();
		if (game == rockpaperscissors)
		{
			for (game = rockpaperscissors; game == rockpaperscissors; game = rockpaperscissors)
			{
				player = Console.ReadLine();
				if (player == exit)
				{
					Console.WriteLine("bye");
					for (game = rockpaperscissors; game == rockpaperscissors; game = rockpaperscissors)
					{
					}
				}

				Random number = new Random();
				string paper = "paper";
				string rock = "rock";
				string scissors = "scissors";
				int randomValue = number.Next(0, 3);
				if (randomValue == 0)
				{
					input = paper;
				}
				else if (randomValue == 1)
				{
					input = rock;
				}
				else
				{
					input = scissors;
				}

				if (player == rock)
				{
					Console.WriteLine("The computer chose " + input);
				}
				else if (player == paper)
				{
					Console.WriteLine("The computer chose " + input);
				}
				else if (player == scissors)
				{
					Console.WriteLine("The computer chose " + input);
				}
				else
				{
					Console.WriteLine("The computer chose black hole. The computer wins");
				}

				Console.WriteLine("(all lowercase) Rock, paper, or scissors? or 'exit' to leave");
			}
		}
		else if (game == tictactoe)
		{
			string[, ] letters =
			{
				{
					"1",
					"2",
					"3"
				},
				{
					"4",
					"5",
					"6"
				},
				{
					"7",
					"8",
					"9"
				}
			};
			int number;
			string placeholder = "placeholder";
			string space;
			int horizontal;
			int vertical;
			horizontal = 1;
			for (game = tictactoe; game == tictactoe; game = tictactoe)
			{
				space = placeholder;
				for (int i = 0; i < 3; i++)
				{
					string res = "";
					for (int d = 0; d < 3; d++)
						res += "|" + letters[i, d] + "|";
					{
						Console.WriteLine("---------");
						Console.WriteLine(res);
					}
				}

				Console.WriteLine("which column u want (or type reset to reset the board or leave to leave)");
				space = Console.ReadLine();
				if (int.TryParse(space, out number))
				{
					horizontal = --number;
				}
				else if (space == leave)
				{
					Console.WriteLine("bye");
					for (game = tictactoe; game == tictactoe; game = tictactoe)
					{
					}
				}
				else if (space == reset)
				{
					letters[0, 0] = "1";
					letters[0, 1] = "2";
					letters[0, 2] = "3";
					letters[1, 0] = "4";
					letters[1, 1] = "5";
					letters[1, 2] = "6";
					letters[2, 0] = "7";
					letters[2, 1] = "8";
					letters[2, 2] = "9";
				}
				else
				{
					Console.WriteLine("thats not a number, maybe you misspelled 'leave' or 'reset' idk");
					horizontal = 1;
				}

				if (number > 2)
				{
					Console.WriteLine("pick a lower number next time");
					horizontal = 1;
				}
				else if (number < 0)
				{
					Console.WriteLine("pick a higher number next time");
					horizontal = 1;
				}

				if (space == reset)
				{
				}
				else
				{
					Console.WriteLine("which row u want");
					space = Console.ReadLine();
					if (int.TryParse(space, out number))
					{
						vertical = --number;
					}
					else
					{
						Console.WriteLine("thats not a number, maybe you misspelled 'leave' or 'reset' idk");
						vertical = 1;
					}

					if (number > 2)
					{
						Console.WriteLine("pick a lower number next time");
						vertical = 1;
					}
					else if (number < 0)
					{
						Console.WriteLine("pick a higher number next time");
						vertical = 1;
					}

					letters[vertical, horizontal] = "X";
				}

				if (space == reset)
				{
				}
				else
				{
					for (int i = 0; i < 3; i++)
					{
						string res = "";
						for (int d = 0; d < 3; d++)
							res += "|" + letters[i, d] + "|";
						{
							Console.WriteLine("---------");
							Console.WriteLine(res);
						}
					}

					Console.WriteLine("which column u want (or type 'reset' to reset the board or 'leave' to leave)");
					space = Console.ReadLine();
					if (int.TryParse(space, out number))
					{
						horizontal = --number;
					}
					else if (space == leave)
					{
						Console.WriteLine("bye");
						for (game = tictactoe; game == tictactoe; game = tictactoe)
						{
						}
					}
					else if (space == reset)
					{
						letters[0, 0] = "1";
						letters[0, 1] = "2";
						letters[0, 2] = "3";
						letters[1, 0] = "4";
						letters[1, 1] = "5";
						letters[1, 2] = "6";
						letters[2, 0] = "7";
						letters[2, 1] = "8";
						letters[2, 2] = "9";
					}
					else
					{
						Console.WriteLine("thats not a number, maybe you misspelled 'leave' or 'reset' idk");
						horizontal = 1;
					}

					if (number > 2)
					{
						Console.WriteLine("pick a lower number next time");
						horizontal = 1;
					}
					else if (number < 0)
					{
						Console.WriteLine("pick a higher number next time");
						horizontal = 1;
					}

					Console.WriteLine("which row u want");
					if (space == reset)
					{
					}
					else
					{
						space = Console.ReadLine();
						if (int.TryParse(space, out number))
						{
							vertical = --number;
						}
						else
						{
							Console.WriteLine("thats not a number, maybe you misspelled 'leave' or 'reset' idk");
							vertical = 1;
						}

						if (number > 2)
						{
							Console.WriteLine("pick a lower number next time");
							vertical = 1;
						}
						else if (number < 0)
						{
							Console.WriteLine("pick a higher number next time");
							vertical = 1;
						}

						letters[vertical, horizontal] = "O";
					}
				}
			}
		}
		else if (game == anythingbesidesthat)
		{
			Console.WriteLine("You're so funny");
		}
	}
}
