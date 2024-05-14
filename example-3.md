# Title
Tijd voor promises

# Description
Tijd om onze eigen promises te schrijven! In de aangeleverde code heb je een aantal functies die nu nog als normale callbacks geschreven zijn. Aan jou de taak om ze om te schrijven naar promises.

Je krijgt de `wait` functie cadeau:

```js
function wait(ms) {
	return new Promise((resolve) => {
		setTimeout(() => resolve(), ms);
	})
}
```

```steps
1. Herschrijf de code in het aangeleverde bestand zo dat er gebruikt gemaakt wordt van promises
```

# LearningObjectives
Het herschrijven van Javascript code naar promises

# Example
```javascript
function randomlyAccept() {
    return new Promise((resolve, reject) => {
        const toResolveOrNot = Math.random() > 0.5;
        if (toResolveOrNot) {
            resolve();
        } else {
            reject();
        }
    });
}

randomlyAccept()
    .then(() => {
        console.log('I resolved');
    })
    .catch(() => {
        console.log('I rejected');
    });

let debounceTimeout;

function debounceFunction(debounceTimer = 1000) {
    return new Promise((resolve) => {
        if (debounceTimeout) {
            clearTimeout(debounceTimeout);
        }
        debounceTimeout = setTimeout(() => resolve(), debounceTimer);
    });
}

debounceFunction(5000).then(() => {
    console.log('one');
});

debounceFunction().then(() => {
    console.log('two');
});

const userData = {
    name: "Thomas",
    userType: "train",
};

function wait(ms) {
    return new Promise((resolve) => {
        setTimeout(() => resolve(), ms);
    });
}

function hasUserData() {
    return new Promise((resolve, reject) => {
        if (userData) {
            resolve();
        } else {
            reject();
        }
    });
}

wait(5 * 1000)
    .then(hasUserData)
    .then(() => {
        console.log('There is a user');
    })
    .catch(() => {
        console.log('No user');
    });
```