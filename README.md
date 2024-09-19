**EXPERIMENT 1: INTRODUCTION TO PYTHON PROGRAMMING**

Jasmine Nicole S. Pascual

2ECE-B

August 26, 2024
##
**I. Intended Learning Outcomes:**
1. To identify the basic codes and functions in Python Programming
2. To be able to apply the different codes and functions in creating a Python Program
##
**II. Instructions:**
Write a Python script/code in the Jupyter Notebook to do the given problems. You may submit your Jupyter notebook in the dedicated submission bin.

**ALPHABET SOUP PROBLEM**
Create a function that takes a string and returns a string with its letters in alphabetical order.

            a = input("Please enter your letters: ")  #Prompt the user to enter letters
            
            b = ''.join(sorted(a)) #Sort the entered letters and joins them
            
            print(b) #Print the output

**EMOTICON PROBLEM**
Create a function that changes specific words into emoticons. Given a sentence as a string, replace the words, smile, grin, sad and mad with their corresponding emoticons.

            def emote(sentence): #Define the dictionary of emoticons where keys are words and values are their corresponding emoticons
            
                emoticons = {
                    "smile":":)",
                    "grin":":D",
                    "sad":":((",
                    "mad":">:("
                }
                words = sentence.split() #Split the sentence into words
                
                replace = [emoticons.get(word, word) for word in words] #Replace the words with their corresponding emoticons in the dictionary
                
                return ' '.join(replace) #Join the words back into a single sentence with the emoticons
            
            print(emote("Make me smile")) #Print "Make me smile" replacing smile with the emoticon ":)"
            
            print(emote("I am mad")) #Print "I am mad" replacing mad with the emoticon ">:("

**UNPACKING LIST PROBLEM**
Unpack the list writeyourcodehere into three variables, being first, middle, and last, with the middle being everything in between the first and last element. Then print all three variables.

            items = input("Please enter your list of items.") #Prompt the user to enter their list of items
            
            items = items.replace(',', ' ') #Remove the commas in the list and replace it with spaces
            
            list = items.split() #Split list into separate items
            
            def unpack(list):
            
                if len(list) == 0: #Check if the list it empty then prompt the user to enter their list again
                    print("The list is empty. Please try again.")
                    
                else: 
                    first, *middle, last = list #Unpack the list into their first, middle and last items
                    
                    print("first: ", first) #Print the first item
                    
                    print("middle: ", ' '.join(middle)) #Print the middle items joined into a string separated by spaces
                    
                    print("last:" , last) #Print the last item
            
            unpack(list) #Call the unpack function with the new list
