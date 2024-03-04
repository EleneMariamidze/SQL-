CREATE TABLE Organization (  
id int NOT NULL PRIMARY KEY,  
name VARCHAR (30),  
employees int ) ;

INSERT INTO Organization VALUES (1, 'SKILLWILL', 200) ;

CREATE TABLE Departments (  id NOT NULL PRIMARY KEY,  dep_name VARCHAR (25)  );                   

INSERT INTO Departments VALUES (1, 'HR'), (2, 'SALES'), (3, 'FINANCIAL'), (4, 'TECH'), (5, 'MARKETING');

CREATE TABLE Employees (  
id int NOT NULL PRIMARY KEY,    
name VARCHAR (20),   
 last_name VARCHAR (30),  
salary DECIMAL,  
mail VARCHAR UNIQUE );

INSERT INTO Employees VALUES (1, 'Giorgi', 'Kharatishvili', 5000, 'gk@hmail.com'), (2,'Eka', 'Maisuradze', 5200, 'em@gmail.com'), (3, 'Nino', 'Eloshvili', 3500, 'ne@gmail.com'), (4, 'Dato', 'Datiashvili', 3700, 'dd@gmail.com'), (5, 'Luka','Kikiladze', 2000, 'lk@gmail.com'), (6, 'Salome', 'Svanadze', 2500, 'ss@gmail.com'), (7, 'Keti', 'Kokaia', 3000, 'kk@gmail.com'), (8, 'Shota', 'Davitaia', 3000, 'shd@gmail.com'), (9, 'Nuca', 'Kiladze', 2500, 'nk@gmail.com') ;

CREATE TABLE employees_department ( 
id NOT NULL PRIMARY KEY,  
employees_id INT,  departments_id INT,  
FOREIGN KEY (employees_id) REFERENCES Employees (id),  
FOREIGN KEY (departments_id) REFERENCES Departments (id) );

INSERT INTO Employees_department VALUES (1, 1, 4), (2, 2, 2), (3, 3, 1), (4, 4, 5), (5, 5, 1), (6, 6, 5), (7, 7, 2), (8, 8, 4), (9, 9, 2) ;
