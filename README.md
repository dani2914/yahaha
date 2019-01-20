# YAHAHA !

### Cloud Computing Team Project ![Awesome](https://cdn.rawgit.com/sindresorhus/awesome/d7305f38d29fed78fa85652e3a63e154dd8e8829/media/badge.svg)

YAHAHA is a secondary E-market platform for students to circulate things on campus. Whereas currently students have to buy a lot of furniture when coming to new campus, YAHAHA lets students bypass the frustration of picking out inexpensive furniture with good quality that is the right for them. 
Our secondary E-market platform is based on [AWS web services](https://aws.amazon.com/) together with [common market transaction dataset]() for association rule mining to recommend relevant furniture for students, so it will facilitate the search process.  
In particular, given a set of courses that a student has already taken, a professor that the student would like to work with or a topic that student is interest in, VergilPlus outputs the courses that fit these constraints.  

## Build: <br />
```
Vergilplus is managed by maven. To build our project:
1. Open terminal enter project directory.
2. run "mvn install". All the unit test cases will run automatically and if all use cases passed, the project is built successfully.
```

## Install: <br />
```
Download the source code and use mvn install to install our project, like stated before.
Load Mysql database using sql file in data/vergilplus.sql.  We assume your database username is "dbuser", and password is also "dbuser".
Our software uses Amazon AWS Lex, which requires a private key. Please contact us if you want to obtain our key.
```

## Test: <br />
```
Our project uses JUnit test tool and Jacoco for testing. To test our project simply run mvn test
```

## Operation:<br />
1. Vergilplus will greet user by welcome message.<br />
2. User can type the following sentences to start searching<br />
    &nbsp;&nbsp;&nbsp;&nbsp;a. Tell me about Professor + "Professor name" / I am interested in professor + "Professor name"<br />
    &nbsp;&nbsp;&nbsp;&nbsp;b. I am interested in + "course topics, like machine learning"<br />
    &nbsp;&nbsp;&nbsp;&nbsp;c. I want course recommendation<br />
3. Vergilplus then asks for the specifics of the chosen functionality.  If the user chooses to inquiry about a professor, then VergilPlus prompts for professor name.  If the user chooses to inquiry about a topic, then VergilPlus prompts for topic.  If the user chooses the third functionality, then VergilPlus directly continues to step 4.   
4. VergilPlus asks for previous taken courses, which users may input using course number, preferably in the format of "COMSW4111".
5. Vergilplus then will perform correlated functionalities<br />
    &nbsp;&nbsp;&nbsp;&nbsp;a. It will search sentimental words of the professor in our database and tell the user what courses th professor teaches.
    &nbsp;&nbsp;&nbsp;&nbsp;b. It will search all courses in our database that are related to the specified topic.<br />
    &nbsp;&nbsp;&nbsp;&nbsp;c. It will recommend courses based on our sentiment analysis of previous course reviews.<br />
    All course recommendations take into account the student's previous courses.
<br />

***Technologies and tools used: Java, Google NLP, Amazon AWS Lex, Mysql, Travis CI, Maven, Spring, JUnit, Python, SonarClound, PMD, Jacoco&Codecov.***

## Interesting Stats: <br />
![stats](stats.png)