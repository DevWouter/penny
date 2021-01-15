# Penny
A personal assistant is utterly dedicated and who understands perfectly what you need

## Origin
The name is a reference to [Miss Moneypenny](https://en.wikipedia.org/wiki/Miss_Moneypenny), the private secretary of the head of MI6 in the James Bond universe.
It will run on your system, receive notifications, proces them and finally notify you.

## Basic idea (WIP)
1. Penny: Somewhere on a machine/server you have a service running which will keep recieve all notifications. This can be in the cloud but also on your local machine
2. Agents: Somewhere on a device (think phone/Windows/MacOS) you have an agent which will receive messages based on the state of your machine. These can be not notifications ("Your martini is ready") or requests ("How would you like your Martini: Shaken or stirred?"). You can always "ignore" (the default), "delegate to later" (remind me later), "delegate to another agent" (send to my phone/boss/wife) , "delay until conditions are right" (allows you to setup some come conditions then time alone). An agent can also send demands.
3. Operators: Somewhere on a machine/server/device you have an operator which we will send information and requests but also can proces the response of a request.

Every agent can tell Penny which notifications are relevant and/or setup automatic delays and delegated based on circumstancs. That being said: An agent can send messages to penny.
Penny will also decide if the information of an operator is:
- all-shared: The first agent to respond will respond for all, removing the need to act for other agents. ("Who will answer the door?")
- all-unique: Every agent can determine it's action. ("What is your name?")
- group-shared: Same as `all-shared` except penny decides which agents are included or excluded from the message
- group-unique: Same as `all-unique` except penny decides which agents are included or excluded from the message
- single: Only one agent will receive a message.

## Examples (WIP)
- Example operators:
  - Informing you about RSS feeds
  - Informing you about a change to an HTML page
  - Informing you about a system status
  - Informing you about time
  - Informing you about timer that has completed
  - Informing you about your agenda
  - Informing you about events
  - Requesting you what do to do on a build failure on AZ
 
## What is it not and why? (WIP)
- IFTT, operators should not respond to other operators. Everything should involve an agent. This is about communicating.
  - Or do we want automation?
- Chat, agents should not contact other agents through penny.
  - Why not actually? It would be easy to create a workaround for that.
  
## To think about (WIP)
- Security of identity
- Security of communication
- System requirements for Penny
- Plugin architecture
- How to easily create a new operator
- Onboarding developers
