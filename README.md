# dvdrental


### Code to select a category 'name' by using 'film_id'
```
select name from category where category_id in (select category_id from film_category where film_id =133);
```
