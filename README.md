# SpringBoot2_20

To add accounts to DB, navigate to the URL http://localhost:8080/h2-console/

Click on the connect button

Enter and run the following script:

INSERT INTO ROLE VALUES(1, 'USER');
INSERT INTO ROLE VALUES(2, 'ADMIN');

INSERT INTO USER_DATA VALUES(1, 'jim@jim.com', TRUE, 'Jim', 'Jimmerson', 'password', 'jim');
INSERT INTO USER_DATA VALUES(2, 'jbob@bob.com', TRUE, 'Bob', 'Bobberson', 'password', 'bob');
INSERT INTO USER_DATA VALUES(3, 'admin@admin.com', TRUE, 'Admin', 'User', 'password', 'admin');

INSERT INTO USER_DATA_ROLES VALUES(1,1);
INSERT INTO USER_DATA_ROLES VALUES(2,1);
INSERT INTO USER_DATA_ROLES VALUES(3,1);
INSERT INTO USER_DATA_ROLES VALUES(3,2);

if you run the following script:
select * 
from USER_DATA;

You will see:

ID  	EMAIL  		      ENABLED  	FIRST_NAME  	LAST_NAME  	PASSWORD  	USERNAME  
1	    jim@jim.com	    TRUE		  Jim		        Jimmerson	  password	  jim
2	    jbob@bob.com	  TRUE		  Bob		        Bobberson	  password	  bob
3	    admin@admin.com	TRUE		  Admin		       User		    password	  admin

Now you can enter these usernames and passwords on the login page!
