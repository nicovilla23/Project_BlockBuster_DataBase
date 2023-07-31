<p align="center" width="300">
   <h3 align="center"> Blockbuster Database</h3>
</p>
<img width="478" alt="Principal" src=https://github.com/nicovilla23/Proyect_BlockBuster_DataBase/blob/main/images/Captura%20de%20Pantalla%202023-07-31%20a%20las%2019.05.09.png?raw=true>
<p align="center" width="300">
   <h3 align="center"> Nicolás Villanova</h3>

</p>

## Proyect

In this proyect we operate based on a hypothetical case in which a client wants to reopen blockbuster and asks us to create a database using old records from when it was open.

## Analysing old record

1. Import the old records.
2. Analyse them to figure out which data is usefull.
3. Identify data I need to clean.
4. Make a general diagram for the database's relations.

## Data cleaning
### Actor:
- Replace the first_name and last_name columns with a column that includes both.


### Film:

- Erase the original_language column since it has no records.
- Erase the release_year given that all values are duplicated.
- Updating the last_update column to the current date.
### Inventory:
- Given the client wont reopen with multiple stores I won't create a table for stores in the database and therefore erase the store_id column.


-  Create a new column 'Disponibility' to enable the option to check if it has already been rented.

- Updating the last_update column to the current date.

### Language:
- Updating the last_update column to the current date.

### Old_HDD:
- Replace the first_name and last_name columns with a column that includes both.
- Updating the last_update column to the current date.

### Rental:
- Erase the staff_id column since there is no current staff.
- Updating the last_update column to the current date.
### Staff:
- Creating an empty table 'staff' for future employees.
- Creating columns: staff_id and Name.
### Customer:
- Creating an empty table 'costumer' 
- creating columns: customer_id, Name, Email and Phone
### Category:
- Updating the last_update column to the current date.
## Enabling the database

### Customer:
- Extract customer_id's from the rental table.
- Using the explode fuction to create a row for each costumer.
### Old_HDD:
- Since this is the only table in which we can associate actor with film we will use it as an intermediary table between actor and film
- Identifying actor's actor_id in Old_HDD by comparing with actor table
- Identifying film's film_id in Old_HDD by comparing with film table
- Erase the category_id column after extracting it for further use.

### Film_category:
- Due to the relationship between categories and film in which both can have many of the other I create an intermediary table between both.
- Create a new column using the previously extracted column 'category_id' where it matches with it's correspondant film_id wich was also in the old_HDD table.

## Creating the database

Given the data I have I create a database built around the business plan of the company with its given relation.

I use MySQL to import the data that has been previously cleaned and insert it into the database I created.

<img width="478" alt="Principal" src="https://github.com/nicovilla23/Proyect_BlockBuster_DataBase/blob/main/images/Captura%20de%20Pantalla%202023-07-31%20a%20las%2016.07.16.png?raw=true">







