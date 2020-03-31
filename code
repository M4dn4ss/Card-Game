import os#for screen clear
import random#for shuffling
import getpass#for invisible input

#screen clear
os.system('clear')

class Card:
	def __init__(self,suite,value):
		self.suite = suite
		self.value = value


#suites
suites = ["diamond","spade","heart","club"]

#values of card
values = ["A","2","3","4","5","6","7","8","9","10","K","Q","J"]

#list to store cards
cards = []

#making cards
for suite in suites:
	for value in values:
		x = Card(suite,value)
		cards.append(x)

#shuffling cards
random.shuffle(cards)

#empty list of cards for both players
player1_cards=[]
player2_cards=[]

#distributing cards among players
for i in range(0,52):
	if i<26:
		player1_cards.append(cards[i])
	else:
		player2_cards.append(cards[i])

no_of_cards = 52

#function to cards of each player
#'\t' is tabspace character. It will print one tabspace. Similarly '\n' is newline character. It will print a new line
def print_cards():
	print "Player 1 has :\t\t\tPlayer 2 has:"
	for i in range(0,no_of_cards/2):
		print str(player1_cards[i].value)+"\t"+str(player1_cards[i].suite)+"\t\t\t"+str(player2_cards[i].value)+"\t"+str(player2_cards[i].suite)

print_cards()

#score of player 1 and 2
p1_score = 0
p2_score = 0


#gameplay
for i in range(0,no_of_cards):
	if i%2 == 0:#player 1 will choose first

		while True:

			#getpass for invisible input
			x1 = getpass.getpass("\nPlayer 1 : Enter value and type ENTER and then enter type of card\n")
			y1 = getpass.getpass("")

			#to check entered correct or not
			correct1 = 0

			#checking if entered card is in cards of player 1 or not
			for j in player1_cards:
				if j.suite == y1 and j.value == x1:

					#deleteing entered card
					del(player1_cards[player1_cards.index(j)])
					correct1 = correct1+1

					#now number of cards is 1 less
					no_of_cards = no_of_cards-1

			if correct1==0:
				print "ENTER CORRECT CARD"
			else:
				#Correct card is entered. So, break while
				break;

		while True:

			x2 = getpass.getpass("\nPlayer 2 : Enter value and type ENTER and then enter type of card\n")
			y2 = getpass.getpass("")

			#to check entered card is correct or not
			correct2 = 0

		#checking if entered card is in cards of player 1 or not
			for j in player2_cards:
				if j.suite == y2 and j.value == x2:

					#deleteing entered card
					del(player2_cards[player2_cards.index(j)])
					correct2 = correct2+1

					#now number of cards is 1 less
					no_of_cards = no_of_cards-1

			if correct2==0:
				print "ENTER CORRECT CARD"
			else:
				#Correct card is entered
				break

		#checking if value both both cards matches or not
		if x1==x2:
			p2_score=p2_score+10

	else:#player 2 will choose first

		while True:

			x2 = getpass.getpass("\nPlayer 2 : Enter value and type ENTER and then enter type of card\n")
			y2 = getpass.getpass("")

			#to check entered correct or not
			correct2 = 0

			#checking if entered card is in cards of player 1 or not
			for j in player2_cards:
				if j.suite == y2 and j.value == x2:

					#deleteing entered card
					del(player2_cards[player2_cards.index(j)])
					correct2 = correct2+1

					#now number of cards is 1 less
					no_of_cards = no_of_cards-1

			if correct2==0:
				print "ENTER CORRECT CARD"
			else:
				#Correct card is entered. So, break while
				break;

		while True:

			x1 = getpass.getpass("\nPlayer 1 : Enter value and type ENTER and then enter type of card\n")
			y1 =getpass.getpass("")

			#to check entered card is correct or not
			correct1 = 0

		#checking if entered card is in cards of player 1 or not
			for j in player1_cards:
				if j.suite == y1 and j.value == x1:

					#deleteing entered card
					del(player1_cards[player1_cards.index(j)])
					correct1 = correct1+1

					#now number of cards is 1 less
					no_of_cards = no_of_cards-1

			if correct1==0:
				print "ENTER CORRECT CARD"
			else:
				#Correct card is entered
				break

		#checking if value both both cards matches or not
		if x1==x2:
			p1_score=p1_score+10
	print_cards()
	print "Player1 score :",p1_score,"Player2 score :",p2_score


if p1_score>p2_score:
	print "PLAYER 1 WINS"
elif p2score>p1score:
	print "PLAYER 2 WINS"
else:
	print "MATCH DRAWS"
