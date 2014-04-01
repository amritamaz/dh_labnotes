# Week 8
3-25-2014

## Administrative overview
+ spring break recap
+ requirements of the class
	- submit a lab notebook with your weekly notes from lab, due as a markdown file on github
	- write at least 1 post per week on piazza
	- midterm:
		- use zotero for an annotated bibliography
		- 10-15 canonical essays on the topic of your choosing from the syllabus
		- if there are 2 or 3 of you, it's 10-15 essays per person
		- maybe one person does older and the other does recent
		- refer to the philosophy papers link sent out for the model of what to write, how to 
		- start with articles rather than books
		- if you use a book, you don't have read/cite the whole book, maybe just an introductory chapter
	- the final assignment is a project proposal that pushes off the annotated bibliography, the way to pitch an article to an editor, start of business plan, etc.
		- motivation: why anyone would care
		- data you might use
		- dataset that could help address the problem in python
		- final document: 3-10 pages long, brainstorming pleasant document
	- lab notebook and final project are due in markdown
	
## Timothy May - Crypto Anarchist Manifesto
- there might be a double standard with cash, which levels the same complaints about bad guys, and cryptography
- glazed over the distinction between physical and non-physical
- aaron swarz piece is definitely modelling the language of this piece
- where does the money come from? is this some big libertarian philosophy?
- can we equate economic information and other types of information? can money be conveyed in a message? 
- when financial information is conveyed through electronic means, should we be linked to real world identities, or ananonymous identities based on trust
- is crypto anarchism a little like communism?

### technological determinism
- certain technology will definitely cause social or economic change, certainly
- that's the determinism part of it
- it's problematic because we believe certain technologies cause social change, but not all of it is controversial (?)
- are things caused by the technology or the zeitgeist of it? there needs to be a subtle analysis
- strong determinism is too explicit, but no determinism is also too simplistic and too strong of an argument
- the question becomes "too what extent do these technologies cause social change" especially the cryptographic technologies
- weird tension between the increased need for identity and anonymity - also privacy and encryption and open access
- if all bitcoin transactions are published, that might be like open access, but there's still the real name persona conflict

## what is bitcoin?
+ if i have a physical dollar, and I want to give you a dollar, then I give you the physical dollar
+ with virtual dollars, I could give you and a friend that same dollar, and you might not know they were the same dollar - this is called **double spending** and it is a problem with virtual money
+ bitcoin solves double spending by forcing the user to publicly announce every single transaction, and so if i try to double spend, the swarm community will label one transaction as valid (the first one, based on a timestamp) and the rest as fraudulent transactions
+ the transaction ledger contains a lot of cryptographic smarts
+ the big innovation is that "im going to announce this, and everyone else will verify the transaction"
+ the clever bit - if everyone transacts all their money, all these transactions and all the verification becomes a verify expensive operation - realizing computational power is expensive, people in the bitcoin cloud are rewarded for verifying transactions
	- start a server that verifies transacations
	- the process of verifying bitcoin is **mining** and you win a lottery - the reward is calibrated to the price of electricity and compute power, and is calibrated to introduce new money at appropriate points
	- the amount of currency is connected to the amount of computational power
	- the way money is created is by people verifying the ledger, and in this process you occasionally win money - enocouraging the user to help
	- if you are able to get a hold of a lot of computers to verify a fake transactions, the only way you can really cheat is by having the majority computational power (more than 50%), then he can definitively verify the transaction
	- it is a definitive transaction, does not require a third party to control or verify transaction, or to control the amount of currency in the system (goodbye central banking)
	- the amount of money in the world is tied to the amount of computational power in the world
	- is bitcoin illegal in the US? you aren't allowed to print currency that competes with the dollar
	- bitcoin exists in a huge gray area right now

## Understanding Private and Public Key Encryption
+ 