# Naming

> The most important consideration in naming is that the name fully and accurately describes the entity/action the variable/function represents.

## JavaScript
---

#### Variable names should be a nouns

_Exception: variables that contain boolean_

###### Bad

```javascript
const getEmptyString = ''
```

###### Good

```javascript
const emptyString = ''
```

</br>

#### All variable names that contain boolean should start from `is/are` or `have/has`

###### Bad

```javascript
const valid = true
```

###### Good

```javascript
const isValid = true
```

</br>

#### Constant variables and dictionaries should be named uppercase with splitting words by underscore(CONSTANT_CASE)

###### Bad

```javascript
const defaultUserRole = ''
const validationMessages = {}

```

###### Good

```javascript
const DEFAULT_USER_ROLE = ''
const VALIDATION_MESSAGES = {}
```

</br>

#### Function names should be a verbs

_Exception: not called computed properties and getters in Vue_

###### Bad

```javascript
const validation = () => {}
```

###### Good

```javascript
const validate = () => {}
```

</br>

#### All Function names that returns boolean should start from `check`

###### Bad

```javascript
const valid = () => true
const isAuthorized = () => true
```

###### Good

```javascript
const checkValidity = () => true
const checkAuthorization = () => true
```

</br>

## Vue
---

#### Computed properties should be named as functions if are called and as variables if are not called

###### Bad

```javascript
computed: {
  checkUserAuthorization() {},
  userById(id) {}
}
```

###### Good

```javascript
computed: {
  isUserAuthorized(),
  getUserById(id) {}
}
```

</br>

#### Methods should be named as functions

###### Bad

```javascript
methods: {
  isUserAuthorized() {},
  user()
}
```

###### Good

```javascript
methods: {
  checkUserAuthorization(),
  getUser() {}
}
```

</br>

## Vuex
---

#### Mutations should be named as functions in CONSTANT_CASE and start with `ADD/SET/UPDATE/DELETE`

###### Bad

```javascript
mutations: {
  createUser() {},
  changeSettings() {}
}
```

###### Good

```javascript
mutations: {
  ADD_USER() {},
  UPDATE_SETTINGS() {}
}
```

</br>

#### Actions should be named as functions

###### Bad

```javascript
actions: {
  googleAuthorization() {}
}
```

###### Good

```javascript
actions: {
  authorizeByGoogle() {}
}
```

</br>

#### Getters should be named as functions if are called and as variables if are not called

###### Bad

```javascript
getters: {
  getUser() {},
  checkUserAuthorization() {},
  userById(id) {}
}
```

###### Good

```javascript
getters: {
  user(),
  isUserAuthorized(),
  getUserById(id) {}
}
```

</br>
