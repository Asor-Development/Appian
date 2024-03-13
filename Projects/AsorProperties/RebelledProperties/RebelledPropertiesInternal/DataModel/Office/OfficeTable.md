# Office Table

## 3 COLUMNS
- [x] id
    - INT
- [x] officeId
    - TEXT        
- [x] officeLocation
    - TEXT 
    
        create table `RPI_OFFICE` (
        `ID` integer not null auto_increment,
        `OFFICE_ID` varchar(255),
        `OFFICE_LOCATION` varchar(255),
        primary key (`ID`)
        ) engine=InnoDB;

**Find office table data [here](./OfficeData.md)**