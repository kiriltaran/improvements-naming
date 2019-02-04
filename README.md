# Naming

> The most important consideration in naming is that the name fully and accurately describes the entity/action the variable/function represents.

## JavaScript
---

#### Use nouns for variable names

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

#### Use `is/are` or `have/has` prefixes for boolean variable

###### Bad

```javascript
const valid = true
```

###### Good

```javascript
const isValid = true
```

</br>

#### Use uppercase with splitting words by underscore(CONSTANT_CASE) for constant variables and dictionaries 

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

#### Use verbs for functions names

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

#### Use `check` for functions names that returns boolean

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

#### Use variable naming for computed properties without parameter and function naming for computed properties with parameter
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
  isUserAuthorized() {},
  getUserById(id) {}
}
```

</br>

#### Use function naming for methods section

###### Bad

```javascript
methods: {
  isUserAuthorized() {},
  user() {}
}
```

###### Good

```javascript
methods: {
  checkUserAuthorization() {},
  getUser() {}
}
```

</br>

#### Use `on` prefix for event handlers names. Also prefer to use event name in method name

###### Bad

```javascript
<CustomComponent @event-name="action" />
```

###### Good

```javascript
<CustomComponent @event-name="onAction" />
```

###### Better

```javascript
<CustomComponent @event-name="onEventName" />
```

</br>

## Vuex
---

#### Use CONSTANT_CASE and `ADD/SET/UPDATE/DELETE` prefixes for mutations

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

Better use modules for every entity with constant set of consistent mutations

###### Better

```javascript
// modules/moduleA

mutations: {
  ADD() {},
  SET() {},
  UPDATE() {},
  DELETE() {},
}

// modules/moduleB

mutations: {
  ADD() {},
  SET() {},
  UPDATE() {},
  DELETE() {},
}
```

</br>

#### Use function naming for actions

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

#### Use variable naming for getters without parameter and function naming for getters with parameter

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
  user() {},
  isUserAuthorized() {},
  getUserById(id) {}
}
```

</br>
