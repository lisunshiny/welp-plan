# Schema Information

## Restaurants
column name | data type | details
------------|-----------|-----------------------
id          | integer   | not null, primary key
address     | integer   | not null
city        | string    | not null
state       | string    | not null
zip         | integer   | not null
phone       | integer   | not null
price       | integer   | not null
user-id     | integer   | not null, foreign key (references users)

## Reviews

column name   | data type | details
--------------|-----------|-----------------------
id            | integer   | not null, primary key
author_id     | integer   | not null, foreign key (references users)
restaurant_id | integer   | not null, foreign key (references users)
rating        | integer   | not null
body          | string    | not null

## users
column name     | data type | details
----------------|-----------|-----------------------
id              | integer   | not null, primary key
email           | string    | not null, unique
password_digest | string    | not null
session_token   | string    | not null, unique
