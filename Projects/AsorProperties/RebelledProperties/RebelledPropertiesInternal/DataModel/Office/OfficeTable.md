# Office Table

## 3 COLUMNS
- [x] id
    - Number (Integer)
- [x] officeId
    - TEXT        
- [x] officeLocation
    - TEXT 

## EmployeeOfficeLocation Table
- [x] id
    - Number (Integer)
- [x] empId
    - Number (Integer)
    - FK that references id field of the employees table        
- [x] officeId
    - Number (Integer)
    - FK that references id field of the office table 

- Create Table SQL

        create table `RPI_OFFICE` (
        `ID` integer not null auto_increment,
        `OFFICE_ID` varchar(255),
        `OFFICE_LOCATION` varchar(255),
        primary key (`ID`)
        ) engine=InnoDB;

**Find office table data [here](./OfficeData.md)**