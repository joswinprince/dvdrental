# dvdrental


### ER Diagram
![dvdrental_ER](dvdrental_ER.jpg)


### Code to select a category 'name' by using 'film_id'
```
select name from category where category_id in (select category_id from film_category where film_id =133);
```

### Code to select name from  category and last_update from film_category table 
```
select category.name as Category_Name,film_category.last_update as Film_LastUpdate from category INNER JOIN film_category ON category.category_id = film_category.category_id;
```
### code to select lastupdate from category table and lastupdate from film_category
```
select category.name ,category.last_update as cat_last_update,
film_category.last_update as film_cate_lastupdate from category inner join film_category on
category.category_id =film_category.category_id
```
### query category_id using the category "Action"
```
select category_id from category where name ='Action'
```
### select action films in film_category table
```
select film_id from film_category where category_id in (select category_id from category where name ='Action')
```
### select all the films  which are action films
```
select * from film where film_id in (select film_id from film_category where category_id in (select category_id from category where name ='Action'))
```
### select category id of Animation Movies
```
select category_id from category where name ='Animation'
```
### select film_id of Animation Movies
```
select film_id from film_category where category_id in (select category_id from category where name ='Animation')
```
