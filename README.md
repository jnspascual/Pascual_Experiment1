EXPERIMENT 1: INTRODUCTION TO PYTHON PROGRAMMING
Jasmine Nicole S. Pascual
2ECE-B
August 26, 2024

# Pascual_Experiment1

ALPHABET SOUP PROBLEM

a = input("Please enter your letters: ")  #Prompt the user to enter letters

b = ''.join(sorted(a)) #Sort the entered letters and joins them 
print(b) #Print the output

EMOTICON PROBLEM
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

UNPACKING LIST PROBLEM
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
