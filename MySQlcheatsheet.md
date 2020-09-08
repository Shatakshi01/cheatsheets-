# MySQL CHEAT SHEET 
## 
```Mysql
mysql -u root -p
```
###  SELECT USER
```
 SELECT User, Host FROM mysql.user;
 ```
###  GET LIST OF DATABASES 
 ```
 SHOW DATABASES;
 ```
### SELECT DB TO WORK IN 
 ```
USE dbmslab1;
 ```
### LIST OF TABLES IN IT 
 ```
  SHOW TABLES;
  ```
  ```
  DROP TABLE client_master;
  ```

  ```
   CREATE TABLE CLIENT_MASTER(
    client_no VARCHAR(6),
    name VARCHAR(20),
    adress1 VARCHAR(30),
     adress2 VARCHAR(30),
     city VARCHAR(15),
     pincode  INT,
     state VARCHAR(15)
     );
```

```
CREATE TABLE PRODUCT_MASTER(
    product_no  VARCHAR(15),
    description VARCHAR(20),
    quntity_on_hand INT(8),
    reorder_level INT(8),
    cost_price DECIMAL(8,2),
    selling_price DECIMAL(8,2)
    );
```

```
CREATE TABLE SALESMAN_MASTER(
    salesman_no  VARCHAR(6),
     name VARCHAR(20),
     address1 VARCHAR(30),
     address2 VARCHAR(30),
     city VARCHAR(15),
    pincode  INT,
    state VARCHAR(15),
     date_od_joining DATE,
     salary DECIMAL(8,2)
     );
```
```
INSERT INTO CLIENT_MASTER(client_no,name,adress1,adress2,city,pincode,state) values
('101','Fred','AVENUE ','ABC','DELHI',2410003,'UP'),
('102','JOSH ','park ','def','MUMBAI',2410004,'MP'),
('103','MARY','BIG BAZAR ','MNOP','Banglore ',2410009,'J&K');
```


```
INSERT INTO PRODUCT_MASTER(product_no ,description, quntity_on_hand,reorder_level,cost_price,selling_price) values
('101','BAG',34,6,12.45, 20.6),
('102','Bottle',54,16,99.56, 120.6),
('103','pen',104,26,10.5, 15.6);
```

```
INSERT INTO SALESMAN_MASTER(salesman_no,name,address1,address2,city,pincode,state,date_od_joining,salary) values
('101','SHATS','AVENUE ','ABC','DELHI',2410003,'UP',now(), 18500.00),
('102','Scott','PARK','DEF','MUMBAI',2410004,'MP',now(), 19500.00),
('103','MARY','BIG BAZAR ','MNOP','Banglore ',2410009,'J&K',now(), 20000.00);
```

```
 DELETE FROM CLIENT_MASTER WHERE client_no='101';
 DELETE FROM PRODUCT_MASTER WHERE  salesman_no='101';
  DELETE FROM  SALESMAN_MASTER WHERE  salesman_no='101';
```

```
 CREATE TABLE NEW_TABLE AS (SELECT * FROM CLIENT_MASTER);
 ```

```
INSERT INTO NEW_TABLE values('104','Jarred','karol ','bagh','DELHI',157003,'NEW DELHI'),
('104','Jin','SEOUL ','KOREA','international',008765,'Interantional'),
('105','GINNI','new Market ','INDIA','GUJRAT',157098,'Gandhi Nagar');
```

```
ALTER TABLE  CLIENT_MASTER ADD COLUMN Brand VARCHAR(30);
ALTER TABLE PRODUCT_MASTER  ADD COLUMN production_site VARCHAR(30);
```
```
ALTER TABLE SALESMAN_MASTER RENAME TO NEWSALESMAN_TABLE;
```