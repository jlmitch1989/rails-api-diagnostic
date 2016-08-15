# Rails API Diagnostic

Place your responses inside the fenced code-blocks where indicated by comments.


What is the purpose of a backend?

```bash
To store data for which to communicate to the front end and ultimately with the client.
```

Which layer in the MVC pattern is used by the controller to fetch data?

```bash
The model.
```

In which part of the MVC pattern can we find C.R.U.D actions?

```bash
The controller
```
List at least 5 standard actions that C.R.U.D corresponds to?

```bash
Create, Index, Show, Update, and Destroy
```

A user action fires a `PATCH` request for `pets/1`. Explain in detail each step
required for data to be returned to the client. (bullet points or ordered list,
please include information on dynamic segments, the params hash and seralizers).

```bash
+ The PATCH request goes to the router.
+ The router takes the PATCH request and goes to the appropriate PATCH action controller.
+ The action controller goes to the appropriate model where the business logic resides.
+ The model then goes to the database to update the data.
+ The data gets sent back to the model, and to then to the controller.
+ The controller works with the serializer in figuring out what gets sent back to the client.
+ What ever is in the params hash is what is sent back to the client in the form of JSON.
```

What is the command to scaffold a `medicalRecords` join table which holds
refrences to a `pets` and a `vets` table?

```bash
rails g scaffold medicalRecords pets:references vets:references
```

What is the point of having a join table?

```bash
To be able to combine data from two different tables and also be able to access the information.
```

Give an example of a one-to-many relationship and a many-to-many relationship:

```bash
A one-to-many relationship can be demonstrated as Users and addresses; a user can have many addresses, but an address can only belong to one user.  A many-to-many relationship can be demonstrated as doctors to patients; doctors can have many patients, and patients can have many doctors.
```
