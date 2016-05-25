# _.map

## Problem 1 - JSX / HTML

I have an array of objects (users) and I want to return a ProfileCard for each of them, which would display their first name and have a link to their ProfileDetail page

```javascript

import ProfileCard from 'src/components/profile-card';

const users = [
  { firstName: 'Jason', id: 1 },
  { firstName: 'Bob', id: 2 },
  { firstName: 'Tom', id: 3 },
  { firstName: 'Lily', id: 4 },
];

const profileCards = _.map(users, user => {
  return <ProfileCard user={user}>;
});

```

## Problem 2 - Transform objects into new objects

I have an array of objects (users) that each have a first name and a last name but an email function we are using expects just an array of objects with a `name` key, so we should concatenate first + last name.

```javascript

function sendEmails(users) {
  _.each(users, user => {
    console.log(`Sending email to ${user.name}`);

    // emailLib.sendEmail(user.name, user.email);
  });
}


const users = [
  { firstName: 'Jason', lastName: 'Riley', email: 'jason@blah.com' },
  { firstName: 'Bob', lastName: 'Timmons', email: 'bob@blah.com' },
  { firstName: 'Tom', lastName: 'Bart', email: 'tom@blah.com' },
  { firstName: 'Lily', lastName: 'Flower', email: 'lily@blah.com' },
];

const transformedUsers = _.map(users, user => {
  return {
    name: `${user.firstName} ${user.lastName}`,
    email: user.email,
  };
});

sendEmails(transformedUsers);

```

[Fiddle](https://jsfiddle.net/dug0modm/1/)


## Problem 3 - Getting one key from objects

I have an array of objects (users) and I want to display their first names on the winners.html page I built.

(This used to be _.pluck in lodash v3)

```javascript

const users = [
  { firstName: 'Jason', lastName: 'Riley', email: 'jason@blah.com' },
  { firstName: 'Bob', lastName: 'Timmons', email: 'bob@blah.com' },
  { firstName: 'Lily', lastName: 'Flower', email: 'lily@blah.com' },
];

const firstNames = _.map(users, 'firstName');

console.log('The winners are: ', firstNames);

```

[Fiddle](https://jsfiddle.net/e2s2kc1g/1/)

