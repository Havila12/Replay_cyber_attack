# Replay_cyber_attack
A replay attack is a kind of man-in-the-middle attack in which an attacker sniffs messages being sent on a channel to intercept them and resend them under the cloak of authentic messages. What makes the replay attack particularly harmful is that the attacker does not even need to decrypt the message they resend but can still fool the receiver into thinking that the received message is legitimate. A replay attack is 'passive' in nature (no active manipulation of data in transit) and it is 'online' meaning it occurs when the attacker captures the data is enroute to the authentication server.
# Intro
Start by installing pip and python3. 

# Dependencies
Pycryptodome package which can be installed with:
pip install pycryptodome

**Start Bob, Mallory, and Alice in "Mac-only" configuration.**
Open 3 terminal windows. In window 1 for Bob type:
```
python3 Bob.py localhost 10000 --mac
```
In window 2 for Mallory type:
```
python3 Mallory.py localhost 10000 localhost 10001 
```
In window 3 for Alice type:
```
python3 Alice.py localhost 10001 --mac
```

**Send messages from Alice to Mallory to Bob.**
Follow the prompts to send messages from Alice to Mallory, then press enter to send messages from Mallory to Bob.

**Use Mallory to replay an old message.**
Send a message from Alice to Mallory. Then at the prompt, enter "r" into Mallory and specify the message number of the message you want to replay. 

**Use Mallory to delete a message and pass the next message through.**
Send a message from Alice to Mallory. Then at the prompt, enter "d" into Mallory to delete the message. Send another message and hit enter in Mallory's window.

**Use Mallory to modify a message.**
Send a message from Alice to Mallory. Then at the prompt, enter "m" into Mallory and specify the new message contents. Hit enter to send.
