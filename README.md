# Dominik-R
praca dodatkowa

create TABLE Products (
	id int  AUTO_INCREMENT NOT null,
    nazwa varchar(20),
    opis varchar(30),
    cena double,
    dostepnosc  INT(1),
    PRIMARY KEY(id)
);

create TABLE Customers (
	id int  AUTO_INCREMENT NOT null,
    imie varchar(20),
    nazwisko varchar(30),
    adres varchar(30),
    e_mail varchar(30),
    PRIMARY KEY(id)
);

create TABLE Orders (
	id int  AUTO_INCREMENT NOT null,
    zamowienie int,
    data_zamowienia date,
    klient int,
    produkt int,
    PRIMARY KEY(id)
    );

create TABLE Employees (
	id int  AUTO_INCREMENT NOT null,
    imie varchar(20),
    nazwisko varchar(30),
    stanowisko varchar(30),
    wynagrodzenie double,
    PRIMARY KEY(id)
);

create TABLE Employee_Actions (
	id int  AUTO_INCREMENT NOT null,
    id_klienta int,
    id_pracownika int,
    id_products int,
    typ_akcji varchar(20),
    PRIMARY KEY(id)
);

INSERT into customers(id,adres,e_mail,imie,nazwisko) values 
("1","weglowa","SzJan@wp.pl","Jan","Szwed"),
("2","coalowa","Mkrol@gmail.com","Mateusz","Krol"),
("3","młodych","TowarekT@gmail.com","Toamsz","Towarek"),
("4","tebowa","AgatkaCI@wp.pl","Agata","Ciepluh"),
("5","złota","JHajs@wp.pl","Jakub","Hajs"),
("6","wiadrowa","WiaderkoMateusz@gmail.com","Mateusz","Wiaderko"),
("7","kotuńska","DecembergA@o2.pl","Alan","Decemberg"),
("8","gymowa","JewP@gmail.com","Pablo","Jew"),
("9","dzikowa","KarliOlaf@wp.pl","Olaf","Karli"),
("10","fryzjerska","TakKarol@gmail.com","Karol","Tak");

INSERT into employees(id,stanowisko,wynagrodzenie,imie,nazwisko) values 
("1","spawacz podwodny","15000","Olaf","Spaw"),
("2","nauczyciel","2000","Iwona","Ziemniak"),
("3","kierowca","9300","Adrian","Sytrzy"),
("4","informatyk","6660","Adam","Ileroz"),
("5","informatyk","5000","Józef","Stanin"),
("6","informatyk","4200","Arek","Pieczarek"),
("7","nauczyciel","8300","Dorian","Łoś"),
("8","nauczyciel","2800","Kuba","Fromaś"),
("9","nauczyciel","7600","Brajan","Bogdan"),
("10","konserwator","3000","Dominik","Świder");

INSERT into employee_actions(id,id_klienta,id_pracownika,id_products,typ_akcji) values 
("1","2","4","10","usuniecie"),
("2","4","1","9","utworzenie"),
("3","5","5","8","dodanie"),
("4","3","2","7","dodanie"),
("5","1","3","6","usuniecie"),
("6","7","9","5","usuniecie"),
("7","9","7","4","edycja"),
("8","8","6","3","edycja"),
("9","10","8","2","zmiana"),
("10","6","10","1","zmiana");

INSERT into orders(id,data_zamowienia,klient,produkt,zamowienie) values 
("1","2017-09-21","4","5","001"),
("2","2011-02-27","1","4","999"),
("3","2012-11-30","5","3","888"),
("4","2014-12-11","2","2","777"),
("5","2010-01-18","3","1","666"),
("6","2007-11-17","6","8","555"),
("7","2020-06-10","7","10","444"),
("8","2022-01-29","9","9","333"),
("9","2010-01-11","10","7","222"),
("10","2022-02-01","8","6","111");

INSERT into products(id,cena,dostepnosc,nazwa,opis) values 
("1","1333","0","kabel","aux"), 
("2","2111","0","kabel","hdmi"), 
("3","6621","1","kabel","cinch"), 
("4","2551","1","klawiatura","steelseries"), 
("5","1111","0","słuchawki","steelseries"),
("6","1133","0","myszka","steelseries"), 
("7","9981","0","podkładka","steelseries"), 
("8","2002","1","klawiatura","madog"), 
("9","2324","1","myszka","logitech"), 
("10","3240","0","glosniki","genesis");
