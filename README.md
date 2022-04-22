# Challenge18  

## Introduction

In this challenge we're going to play the role of a fintech engineer who's working at one of the largest banks, with the task to build a blockchain-based ledger system, complete with a user-friendly web interface. On this web-based ledger, users would be allowed to transfer money between each other while guaranteeing the integrity of the data in the ledger.

## Technologies 

Programming Language: 
- Python 3.7.11 loaded from the distribution [Anaconda 4.10.3](https://anaconda.org/anaconda/conda/files?version=4.10.3)

Libraries: 
- [streamlit 1.8.1](https://streamlit.io/), a library that allows to build and share data apps  
    Install through ```pip install streamlit```
- [hashlib](https://docs.python.org/3/library/hashlib.html), module that implements a common interface to many different secure hash and message digest algorithms
- [typing](https://docs.python.org/3/library/typing.html), module that provides runtime support for type hints
- [datetime](https://docs.python.org/3/library/datetime.html), module that supplies classes for manipulating dates and times

## Code

To code this app we make an extensive use of data classes, programming the app in an object oriented programming (OOP) logic. 
We define our transaction at the most elementary level through the "Record" class, which contains information of the single transaction, specifically the sender, receiver and the amount. This class will be itself an attribute of the class "Block", which have also the creator ID, the previous block's hash, a timestamp and a nonce as attributes and a method consisting in a function that encodes this information.
Next we have the "PyChain" class that contains the list of blocks' that make up our blockchain. This class contains three methods: one for the proof of work, one to add a new block and another to check if the new added block is valid.

## Testing the App

After defining the classes we'll be using, we customize our web interface with the streamlit commands.
We can try the result by opening the CLI in the directory where the script is and type:  
``` streamlit run pychain.py```  
The following pictures show how it looks like:  
  
<img width="960" alt="streamlit_interface" src="https://user-images.githubusercontent.com/86806855/164782808-21b0ea0c-0d29-41d6-8d8a-7ec99fb2319f.PNG">  
<img width="467" alt="valid_chain" src="https://user-images.githubusercontent.com/86806855/164784401-d7896d9b-1806-4e3e-be71-7a605a891186.PNG">

## License

Copyright 2022 

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
