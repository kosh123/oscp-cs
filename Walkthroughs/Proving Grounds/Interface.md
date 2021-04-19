## Steps and Guides for Interface

### Open Ports available:

![image](https://user-images.githubusercontent.com/20929896/115129919-89d26d00-9fb8-11eb-8805-a5ec13dadec5.png)

### WebPage Enumeration:

gobuster dir -u http://192.168.52.106/ -w /usr/share/wordlists/dirbuster/directory-list-2.3-medium.txt


### GET Request observed while browsing to the website:

GET Request mentions the '/api/settings' and '/api/users' directory. Attempting to browse the directories gives an 'Unauthorized' response for '/api/settings' but gives a list of users while browsing to '/api/users'. There are about 1991 users mentioned in this directory. 

![image](https://user-images.githubusercontent.com/20929896/115130115-c1421900-9fba-11eb-983f-b39f220960c6.png)
![image](https://user-images.githubusercontent.com/20929896/115130155-1120e000-9fbb-11eb-8ea6-4239f3a421a8.png)

Running wget against the url gave a list of users to possibly bruteforce:

![image](https://user-images.githubusercontent.com/20929896/115130391-71188600-9fbd-11eb-9935-4c1c9d316276.png)


Browsing to the webpage gave a list of top users, I attempted to bruteforce the users mentioned in the following list but wasn't able to get a useful password. 
I used 'rockyou.txt' for the passsword list and used burpsuite to guess the passwords in the form. This didn't give any results however. 

![image](https://user-images.githubusercontent.com/20929896/115130471-14699b00-9fbe-11eb-9452-f07c4f6f51cd.png)

![image](https://user-images.githubusercontent.com/20929896/115130435-cb194b80-9fbd-11eb-966b-283cd9a7a87d.png)


Given the user list provided, extended my password brute force attemtps to all the users:





















