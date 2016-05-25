# _.includes

## Problem 1

We have an array of roles and we need to know if the user is an admin.

(In lodash v3 this was also aliases as `_.contains`)


```javascript

const user = {
  firstName: 'Jay',
  roles: [ 'Support', 'Customer Services', 'Sales', 'Admin' ],
}

const isAdmin = _.includes(user.roles, 'Admin');

console.log('Is Jay an admin?', isAdmin);

```

[Fiddle](https://jsfiddle.net/ge7snspf/)


## Problem 2

We want to check if there is a partial match on a longer string. For instance if there is a duplicate entry in Postgres, it will say something like `error: insert into "your_table" ("first_name", "city") values ($1, $2) - duplicate key value violates unique constraint "your_table_first_name_city_pkey"`


```javascript

const dbError = `error: insert into "your_table" ("first_name", "city") values ($1, $2) - duplicate key value violates unique constraint "your_table_first_name_city_pkey"`;


const isDuplicateError = _.includes(dbError, 'duplicate');

if (isDuplicateError) {
  console.log(`Returning 409 Conflict`);
} else {
  console.log(`Returning 500 Internal Server Error`);
}


```

[Fiddle](https://jsfiddle.net/xqpy0008/1/)
