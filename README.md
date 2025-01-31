
                              PROJECT: FITNESSHUB GYM

FitnessHub Gym is a new, modern gym designed for people of all fitness levels, whether you're just starting out or already a fitness expert. The gym will offer a variety of spaces and equipment to help you work on your fitness goals, with everything from weight training and cardio to group classes and personal training.

Key Features:
•	Different Workout Areas: We’ll have separate zones for weightlifting, cardio machines, group classes like yoga and cycling, and functional fitness.
•	Great Equipment: The gym will be filled with top-quality machines, weights, and accessories to suit all types of workouts.
•	Personal Training: Certified trainers will be available to help you create a workout plan tailored just for you.
•	Wellness Services: After your workout, you can relax in our wellness lounge, which offers healthy snacks, massage services, and recovery options.
•	Flexible Memberships: We’ll offer different membership plans to fit your needs, whether you come to the gym a few times a week or train every day.
•	Community: FitnessHub isn’t just a gym — it’s a place to meet others, with fitness challenges, social events, and group workouts to keep everyone motivated.
Goals:
•	Create a welcoming gym where everyone can reach their fitness goals, feel supported, and stay motivated.
•	Offer top-quality equipment and expert trainers to make every workout count.
•	Build a fitness community where people can motivate each other and achieve more together.


ENTITY RELATIONSHIP DIAGRAM(ERD)











	























LOGICAL DATA MODEL(LDM)

MEMBERS (MEMBER_ID,NAME,EMAIL,PHONE,GENDER,JOIN_DATE,MEMBERSHIP_TYPE).

TRAINERS (TRAINER_ID,NAME,SPECIALIZATION,EMAIL,PHONE).

CLASSES (CLASS_ID,CLASS_NAME,TRAINER_ID,CAPACITY).

ENROLLMENTS (ENROLLMENT_ID,MEMBER_ID,CLASS_ID,ENROLLMENT_DATE).


PAYMENTS (PAYMENT_ID, MEMBER_ID,AMOUNT,PAYMENT_DATE, PAYMENT_METHOD,PAYMENT_STATUS).




DATA DICTIONARY
ENTITIES	ATTRIBUTE	DATA TYPE	SIZE	CONSTRAINTS	DESCRIPTION



MEMBERS	MEMBER_ID	INT	11	PRIMARY KEY
NULL	MEMBER IDENTIFICATION NUMBER
	NAME	STRING	50	NULL	NAME
	EMAIL	STRING	50	NULL	EMAIL
	PHONE	STRING	10	NULL	PHONE
	GENDER	STRING	20	NULL	GENDER
	JOIN_DATE	DATE	20	NULL	JOINING DATE
	MEMBERSHIP_TYPE	STRING	40	NULL	MONTHLY,ANNUAL


TRAINERS	TRAINER_ID	INT	20	PRIMARY KEY
NULL	TRAINER
IDENTIFICATION NUMBER
	NAME	STRING	50	NULL	THE NAME OF TRAINER
	SPECIALIZATION	STRING	40	NULL	ACTIVITY SOMEONE EXPERIENCED TO DO
	EMAIL	STRING	50	NULL	EMAIL OF THE TRAINER
	PHONE	STRING	10	NULL	THE PHONE NUMBER OF TRAINER

CLASSES	CLASS_ID	INT	20	PRIMARY KEY
NULL	THE IDENTIFICATION NUMBER OF THE PLACE
	CLASS_NAME	STRING	50	NULL	
	TRAINER_ID	INT	20	FOREIGN KEY NULL

	IDENTIFICATION NUMBER OF  TRAINER
	CAPACITY	INT	20	NULL	NUMBER OF CUSTOMER EACH ROOM CAN SERVE

ENROLLMENTS
	ENROLLMENT_ID	INT	20	PRIMARY KEY
NULL	IDENTIFICATION NUMBER OF ENROLLMENT ID
	MEMBER_ID	INT	20	FOREIGN KEY NULL
	IDENTIFICATION NUMBER OF THE MEMBER
	CLASS_ID	INT	20	FOREIGN KEY NULL
	IDENTIFICATION NUMBER OF THE CLASS
	ENROLLMENT_DATE	DATE	20	NULL	TIME TO REGISTER IN CLUB


PAYMENTS	PAYMENT_ID	INT	20	PRIMARY KEY
NULL	IDENTIFICATION NUMBER THAT EXPLAIN THE USER WHOPAY
	MEMBER_ID	INT	20	FOREIGN KEY NULL
	THE IDENTIFICATION NUMBER THAT SHOW THE USER WHO PAY
	AMOUNT	INT	20	NULL	AMOUNT OF MONEY REQUIRED TO BE REGISTERED
	PAYMENT_DATE	DATE	20	NULL	DATE REQUIRED TO BE PAYED ON
	PAYMENT_METHOD	STRING	30	NULL	MODE OF PAYMENT YOU CAN USE TO PAY 
	PAYMENT_STATUS	STRING	30	NULL	WHENSOMEONE PAY  THE SYSTEM PROVIDE NOTIFICATION TO THE USER





PHYSICAL DATA MODEL

	


