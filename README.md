# Fill_in_blankMadlibs
3 levels of games.  prompt user to select level.  Once level is selected, prompt user to fill in the blank...
Easy_level =  """ The program that translates Python instructions and then executes them is the Python {__1}.

                Python has five standard data types.  Data types store numeric values is called {__2}.

                Strings and {__3} are 2 important data types in the suite of structured data types in python.

                A {__4} is a block of organized, reusable code that is used to perform a single, related action."""

medium_level = """ The {__1}  statement is used for repeated execution as long as an expression is true.
                The {__2} statement is used to iterate over the elements of a sequence (such as a string, tuple or list or other iterable object.

                We can change the value of a list after we have created it, but we cannot in case of strings, it is called {__3}.

                The {__4} statement is used for conditional execution."""

hard_level = """ If a sequence contains an expression list, it is evaluated first. Then, the first item in the sequence is assigned to the
                iterating variable iterating_var. Next, the statements block is executed. Each item in the list is assigned to iterating_var,
                and the statement(s) block is executed until the entire sequence is exhausted.  It’s a {__1} .

                If the else statement is used with a {__2}, the else statement is executed when the loop has exhausted iterating the list.

                If the else statement is used with a {__3}, the else statement is executed when the condition becomes false.

                {__4} is nothing but reserved memory location to store value. This means that when you create a {__4}
                you reserve some space in memory."""


level = {1:'easy', 2:'medium',3:'hard'}

# a list of replacement words to be passed in to the play game function.
answer_list_easy = ['interpreter', 'numbers', 'lists', 'function']
answer_list_med = ['while', 'for', 'mutation', 'if']
answer_list_hard = ['for loop', 'for loop', 'while loop', 'variable']

# the dictionary of keys answers to questions 
dict_easy = {1:'interpreter', 2:'numbers',3: 'lists', 4:'function'}
dict_med = {1:'while', 2:'for', 3:'mutation', 4:'if'}
dict_hard = {1:'for loop', 2:'for loop', 3:'while loop', 4:'variable'}

# of questions
questions = [1,2,3,4]

# to prompt user to select level of game.
def game_level():
    
        
        promptFormat = "Which level would you like: 1=easy, 2=medium, 3=hard? "
        print (promptFormat)
        response = input("level picked:")

        for i in level:
            if response == '1':
                return Easy_level
            if response == '2':
                return medium_level
            else:
                return hard_level
      

print (game_level())

def play_game(Easy_level):
        
       correct_word = []
       for i in questions:
               
               while True:
                       prompt = "What to fill in blank  " + str(i) + "?"
                       print (prompt)
                       user_input = input ("User input:" )
                       for i in answer_list_easy:
                               
                               if user_input == answer_list_easy[0]:
                                       correct_word.append(user_input)
                                       Easy_level = Easy_level.replace('{___}', 'correct_word')
                                       print(Easy_level)
                               
      
                                       
                               else:
                                       print ("Sorry, try again")
                                       user_input = input ("User input:")
                             
                                    
print (play_game(Easy_level))                               
                               
                
        


