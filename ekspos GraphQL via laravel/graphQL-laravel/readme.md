<p align="center"><img src="https://laravel.com/assets/img/components/logo-laravel.svg"></p>

<p align="center">
<a href="https://travis-ci.org/laravel/framework"><img src="https://travis-ci.org/laravel/framework.svg" alt="Build Status"></a>
<a href="https://packagist.org/packages/laravel/framework"><img src="https://poser.pugx.org/laravel/framework/d/total.svg" alt="Total Downloads"></a>
<a href="https://packagist.org/packages/laravel/framework"><img src="https://poser.pugx.org/laravel/framework/v/stable.svg" alt="Latest Stable Version"></a>
<a href="https://packagist.org/packages/laravel/framework"><img src="https://poser.pugx.org/laravel/framework/license.svg" alt="License"></a>
</p>

in folder project graphQL laravel.. review the folder _config_ and open file _graphql.php_.. make sure you configuration on 
**schema** , **query**, and **mutation**
..
for testing graphQl...
.
you can testing graphQl with postman and graphiql.. 
in here i use postman.. 

.http://localhost:8000/graphql?query=query+FetchUsers{users{id : "1" ,email}} => for showing user with id 1 and email..

* {
 *   "data": {
  *      "users": [
   *         {
    *            "id": "1",
     *           "email": "bimo@gmail.com"
            },
            

http://localhost:8000/graphql?query=query+FetchUsers{users{id ,email,name,jabatan,jobdesk}} => for showing all user with catagories **id**, **email**, **name** , **jabatan** and **jobdesk**

* {
  *              "id": "2",
   *             "email": "imel@gmail.com",
    *            "name": "angga",
     *           "jabatan": "backend",
      *          "jobdesk": "koding"
            }
        ]
    }
}

you can add other catagories adjust on your database table ....
.
testing mutation 
http://localhost:8000/graphql?query=mutation+users{updateusers(id: "1", email: "bimoanugrah@gmail.com"){id,name,email,jabatan,jobdesk}} => for update data user with id 1

* {
    + "data": {
      +  "updateusers": {
       +     "id": "1",
        +    "name": "kibo",
         +   "email": "bimoanugrah@gmail.com",
          +  "jabatan": "backend develloper",
           + "jobdesk": "building system and maintenance "
+        }
+    }
+ }
