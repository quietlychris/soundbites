# soundbites

This is a quick Python program that uses GTTS to turn a text file of Q&A flashcards
into a collection of MP3 files. This can be a useful way to study or learn new
material using audio aides instead of visual ones.  

Dependencies include having Google's Text-to-Speech libraries, which can be done
fairly simply using

    pip install gTTS
    
Additionally, Python's os and sys imports are used. Hopefully someone else
might find this useful as well!

### Instructions

To use, simply create a .txt file, with the following structure:

    title-of-mp3
    Question: You should put a question here
    Answer: You should put an answer here!

Then run:

    python soundnotes.py <name-of-flashcard.txt> <directory-name>

The program will take every 3 lines, turn the first one into the title of the
generated .mp3 file, and then read the next two lines back-to-back. Don't skip
a line between the answer of one card and the title of the next, since there's
nothing implemented yet to make that more useful.
