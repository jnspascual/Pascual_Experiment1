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

            a = input("Please enter your letters: ")  _#Prompt the user to enter letters_
            
            b = ''.join(sorted(a)) _#Sort the entered letters and joins them_ 
            
            print(b) _#Print the output_

**EMOTICON PROBLEM**
Create a function that changes specific words into emoticons. Given a sentence as a string, replace the words, smile, grin, sad and mad with their corresponding emoticons.

            def emote(sentence): _#Define the dictionary of emoticons where keys are words and values are their corresponding emoticons_
            
                emoticons = {
                    "smile":":)",
                    "grin":":D",
                    "sad":":((",
                    "mad":">:("
                }
                words = sentence.split() _#Split the sentence into words_
                
                replace = [emoticons.get(word, word) for word in words] _#Replace the words with their corresponding emoticons in the dictionary_
                
                return ' '.join(replace) _#Join the words back into a single sentence with the emoticons_
            
            print(emote("Make me smile")) _#Print "Make me smile" replacing smile with the emoticon ":)"_
            
            print(emote("I am mad")) _#Print "I am mad" replacing mad with the emoticon ">:("_

**UNPACKING LIST PROBLEM**
Unpack the list writeyourcodehere into three variables, being first, middle, and last, with the middle being everything in between the first and last element. Then print all three variables.

            items = input("Please enter your list of items.") _#Prompt the user to enter their list of items_
            
            items = items.replace(',', ' ') _#Remove the commas in the list and replace it with spaces_
            
            list = items.split() _#Split list into separate items_
            
            def unpack(list):
            
                if len(list) == 0: _#Check if the list it empty then prompt the user to enter their list again_
                    print("The list is empty. Please try again.")
                    
                else: 
                    first, *middle, last = list _#Unpack the list into their first, middle and last items_
                    
                    print("first: ", first) _#Print the first item_
                    
                    print("middle: ", ' '.join(middle)) _#Print the middle items joined into a string separated by spaces_
                    
                    print("last:" , last) _#Print the last item_
            
            unpack(list) _#Call the unpack function with the new list_
