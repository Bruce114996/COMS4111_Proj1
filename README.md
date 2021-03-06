# COMS4111_Project 1

# Movie Database Design:
<span style="color:red">Zhihan Yang, Bowen Han
# Inspiration and Design of the Database:
We plan to design the online movie database and interaction system for all kinds of users. Our inspiration comes from the website called Douban in China. The interesting part is to provide the movie profiles and its corresponding actors to the user. Besides, the user can make comments on the movies and they can also use check the movie’s basic information such as languages, crew, genres. Finally, they can add the movies to the like-list and they can choose to share it to other users or just make it private.
# ER diagram
![COMS4111 PROJECT ER DIAGRAM drawio (3)](https://user-images.githubusercontent.com/59796732/163073076-89211db6-2086-4e09-a8b5-646239cd520f.png)
# The real word constraints
1. A user can make a lot of comments on different movies and they can also make comments for many times in the same movie. The ratings must between 1 to 10. Even if the user’s account has been deleted, their comments will exist. 
  
2. For the movies, they have several languages versions, companies, crew and genres corresponding to them. In addition, there is no doubt that language, company, genre and crew can correspond to many movies. 
  
3. Actor can cast many movies and a movie can have many actors cast on them. Users can follow many actors and actors can also be followed be many users. 
  
4. An actor may cast several roles in the same movie and movie has many actors. 
  
5. Like_list folder is a weak entity of users and if the user’s account has been deleted, the like_list will also disappear. 
  
6. Users can make their like_list to be either public or private and only the public one can be shared to other users.

# Structure of the Web Database:
Design: We design the web front-end considering the user's angle. Firstly,the first page is login page and they can both login and create a new account. Then for the main page, it contains user part and movie part. For the movie part, the user can check the movie profiles and actor profiles including information like movie's languages, genres, actor's name etc. Besides, they can makeg some comments, add movies into their likelist as well as follow other actors. For the user part, the users can also check both their likelist and other user's likelist and create the new likelist(public or private) for themselves. For users themselves, they can check both their actor list and like list, but for other users if they set the likelist to private other users cannot see which movie they like. 

 ![project1 part3 web process](https://user-images.githubusercontent.com/59796732/163474953-4aa7bd31-06fb-46db-b918-6dbca08223f8.png)

(Upper Line means there has link on it and red word with upper line means interaction operation for users.)
  
# View of the page:
  
# Main page:
![Main page](https://user-images.githubusercontent.com/59796732/163076606-1dd04289-fff9-40d0-a272-670646aeaf0f.PNG)
# Movie's Main Page:
![Movie main page](https://user-images.githubusercontent.com/59796732/163076643-53bdbc2b-6097-47f3-becc-480e4e36fc2a.PNG)
# User's Main Page:
![User main page](https://user-images.githubusercontent.com/59796732/163076671-c032480d-aa8a-4e97-a703-08e5daf8834d.PNG)

# How to work 

## Organisation of this directory 
```
COMS4111_Proj1/webserver/
├── static/
├── templates/
├── create_db.py
├── funcs.py
├── server.py       
└── requirements.txt
requirements: Packages need to install
create_db.py: create and insert the values into database. 
funcs.py: create the class for the interaction part including creating new user, comments and add movie to likelist. 
server.py: build the front-end system for the web 

```
 
