---
# Part I - of How to create a simple Decentralized Application using Ethereum Blockchain?
###### '2019-04-01'
---

A simple Application that depicts how the blockchain works!

You might be like, "Blockchain what does it mean?" do not worry when I started learning on how to create a Decentralized Applications(shortly called as DApps) using the Ethereum Blockchain that was the exact question that came to my mind.

I heard somewhere, sometime before, *that learning things in a visual way can help you remember the stuff that you learned for a long time*. So here is the link of getting a mental image of how a blockchain works: [which is explained by Anders very well](https://anders.com/blockchain/hash.html).

Okay, you know got a idea on what is an blockchain. Let us dive right into making stuffs!

We will be using **Solidity** programming language to create DApps, unlike other programming language Solidity programming language contains Big gotchas, if I start talking about the gotchas in Solidity programming that would go for seperate article. We'll take it slow for know.

```solidity
pragma solidity ^0.4.17;  
contract Inbox {     
	string public message;      
	function Inbox(string initialMessage) public {         
		message = initialMessage;     
	}

	function setMessage(string newMessage) public {         
		message = newMessage;     
	}
}
```

If you came from languages like Javascript, Java, Ruby, Python, C#, and C++ this might look familiar. However we will go through this line by line.

`
pragma solidity ^0.4.17
`

This specifies the required compiler the solidity should use when this source code must be executed.

`
contract
`
This is like a class in Java, ruby, etc.,

We have a local variable declared inside our contract called as:
`
string public message;
`
Which is used to store the recent message.

```solidity
function Inbox(string initialMessage) public {         
	message = initialMessage;     
}
```
The above code is an constructor method, and it is your wish to specify a value to the constructor or not during deployment.

```solidity
function setMessage(string newMessage) public {
	message = newMessage;
}
```
Okay, now what does this *function* do as said it updates the message local variable that is contract.

To compile this and see on how it works we can use [remix](https://remix.ethereum.org).

Here is mine: ![alt text](https://i8pbgq.bn.files.1drv.com/y4mtqoZKUqLPZcr-zN6qs2YXrwuUdnarJfXBLFUteZqilLvw4BM88usGO8p7qu136LcYXsEbq2CTiZ0HYj38lQQ-zbS9uKk9ttH_X_Skm3nvx1vi3vO13AN7aAFbjHsgcbrAGf_k0vAhGk5UERopCx9xh3LQPEBbRAmbSEKU5by4K-PL0etrCKgfyQIuOwn9bPiyNMohHRU2LW-EiHFYr0aXQ?width=1912&height=929&cropmode=none "Here is mine")

Okay, now how do we test this, well don't worry remix take cares of that stuffs for you, go to the **run** tab and make sure you are going to follow the exact steps that I do:

1) Set *Environment* to *JavaScript VM*.
2) *Account* can be anything.
3) *Gas Limit* default is enough.
4) *Value* it is okay to be *0*, because we are not paying anything in this.
Here is mine: ![alt text](https://jmpbgq.bn.files.1drv.com/y4mLIHfvbi1swk3HUJJBcxEayL3G4zx6rzI9rTtovN4K5YveqfG0auUqpji0y4OlKtRWReZlDUa_rUU-WLYzpiqjuT37UJr6vMbRfFFfy3HTfHm6FADxDD6eaVApEL6c7Qy4nAjssUwYM95zC4ZMXMyjWQWQrrBuWEFkwAkohVsjvBKTztXA2jQduOIFl9itTrElzpwZBAWBvPgWYVjZ3NqgQ?width=1920&height=1080&cropmode=none)

On a side note, you might be wondering why is there is an *Account* right? That is the power of **Remix** saying that here you have a 5 random accounts just play around with it.

Okay, now what right?
We finished more than half of the hurdle. Now click on "deploy" button it will show "Transactions", and then set a message inside that, please remember to *setMessage* in double quotes, because it expects an string in the argument as we saw in our function:

```solidity
function setMessage(string newMessage) public {
	message = newMessage;
}
```
A final image to finish this, on how to see the output:

![alt text](https://jspbgq.bn.files.1drv.com/y4mr14TrV_Z7AzYWAsYWNOYVGFUn7oE5ohAGFQ6KqqOEpYsqAzo9RhdHy2CebgP7NLNNtECNDnue3SHSW48DmAe9UTZUkLEXpTr4F4WYP0EAetdok0k2NMiEwehJuzhBzg2l-MW0ZvRE8GBmV97_2aOf9ral1W6O3YW8WUCZJYaWNDkXPlqQbtJvJoK__3JFBvC67SiYjTAu-4h2vE7E5aB0g?width=1920&height=1046&cropmode=none)

After you deploy the contract you can get a clickable
`
setMessage
`

Add your required text in a **double quotes**.

That's it you just made your first contract, and deployed it on your local machine.

It is just a start we will do deploy this in our local machine and test it with **mocha** test library, which is available in *NodeJS*

See you in Part - II.
