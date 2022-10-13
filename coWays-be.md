> `1. Register`

# REGISTER API

## A. Requirements

**url** = {your_host}/api/v1/register

**mehtod** = POST

**request body** =

```json
{
  "email": "dinda@gmail.com",
  "password": "myCustomPassword",
  "name": "Dinda Adinda Putri"
}
```

**response body** =

```json
{
  "status": "success",
  "data": {
    "user": {
      "name": "Dinda Adinda Putri",
      "email": "dindaputri@mail.com",
      "token": "0sdnOJIoinsdo9878IJNBIniiuinINiuYIUY"
    }
  }
}
```

## B. Instructions

- When you finish this task, move it to "test" list. Then don't forget to push your job on https://github.com/[your_name]_coWays_be

- Create branch `1.Register`.

```
   git checkout -b 1.Register
```

- Push to branch `1.Register`.

```
   git add .
   git commit -m "add Register"
   git push origin 1.Register
```

==========================================================================

> `2. Login`

# LOGIN API

## A. Requirements

**url** = {your_host}/api/v1/login
**mehtod** = POST
**request body** =

```json
{
  "email": " samsul@gmail.com ",
  "password": "myPasswordCom"
}
```

**response body** =

```json
{
  "status": "success",
  "data": {
    "user": {
      "name": "samsul rijal",
      "email": "samsul@gmail.com",
      "status": "customer",
      "token": "0sdnOJIoinsdo9878IJNBIniiuinINiuYIUY"
    }
  }
}
```

## B. Instructions

- When you finish this task, move it to "test" list. Then don't forget to push your job on https://github.com/[your_name]_coWays_be

- Create branch `2.Login`.

```
   git checkout -b 2.Login
```

- Push to branch `2.Login`.

```
   git add .
   git commit -m "add Login"
   git push origin 2.Login
```

==========================================================================

> `3. Music`

# MUSIC API

## A. Requirements

# 1. Add Profuct

**url** = {your*host}/api/v1/product
**recruitments** = \_For image/video file upload, when user add new music, userId automatically insert and associate with product*

**method** = POST

**request header** =

```json
{
  "Authorization": "Bearer {token}"
}
```

**request body** =

```json
{
  "thumbnail": "balon-ku-ada-lima.png",
  "title": "Balon ku ada 5",
  "year": 2004,
  "singer_id": 4,
  "music_file": "balon-ku-ada-lima.mp3"
}
```

**response body** =

```json
{
  "status": "success",
  "data": {
    "product": {
      "id": 1,
      "thumbnail": "<domain>/balon-ku-ada-lima.png",
      "title": "Balon ku ada 5",
      "year": 2004,
      "singer": {
        "id": 4,
        "thumbnail": "<domain>/ariel-noah.png",
        "old": 40,
        "category": "solo",
        "start_career": 2008
      },
      "music_file": "<domain>/balon-ku-ada-lima.mp3",
      "user": {
        "id": 1,
        "name": "Admin",
        "email": "admin@mail.com",
        "Image": "admin.jpg"
      }
    }
  }
}
```

# 2. Get All products

**url** = {your_host}/api/v1/products
**method** = GET
**response body** =

```json
{
  "status": "success",
  "data": {
    "products": [
      {
        "id": 1,
        "image": "mouse-pad.png",
        "title": "Mouse Pad",
        "desc": "The best Mouse Pad ...",
        "price": 500000,
        "qty": 300
      },
      {
        "id": 2,
        "image": "keyboard.png",
        "title": "Keyboard",
        "desc": "The best keyboard ...",
        "price": 3500000,
        "qty": 200
      },
      {
        "id": 3,
        "image": "monitor.png",
        "title": "Monitor",
        "desc": "The best Monitor ...",
        "price": 7200000,
        "qty": 120
      },
      {
        "id": 4,
        "image": "mouse.png",
        "title": "Mouse",
        "desc": "The best Mouse ...",
        "price": 5500000,
        "qty": 230
      }
    ]
  }
}
```

# 3. Get Product Detail

**url** = {your_host}/api/v1/product/:id
**mehtod** = GET

**request header** =

```json
{
  "Authorization": "Bearer {token}"
}
```

**response body** =

```json
{
  "status": "success",
  "data": {
    "product": {
      "id": 1,
      "image": "mouse-pad.png",
      "title": "Mouse Pad",
      "desc": "The best Mouse Pad ...",
      "price": 500000,
      "qty": 300
    }
  }
}
```

# 4. Update Product

**url** = {your_host}/api/v1/product/:id
**mehtod** = PATCH

**request header** =

```json
{
  "Authorization": "Bearer {token}"
}
```

**request body** =

```json
{
  "desc": "Best Quality Mouse Pad"
}
```

**response body** =

```json
{
  "status": "success",
  "data": {
    "product": {
      "id": 1,
      "image": "mouse-pad.png",
      "title": "Mouse Pad",
      "desc": "Best Quality Mouse Pad",
      "price": 500000,
      "qty": 300
    }
  }
}
```

# 5. Delete Product

**url** = {your_host}/api/v1/product/:id
**mehtod** = DELETE

**request header** =

```json
{
  "Authorization": "Bearer {token}"
}
```

**response body** =

```json
{
  "status": "success",
  "data": {
    "id": 1
  }
}
```

## B. Instructions

- When you finish this task, move it to "test" list. Then don't forget to push your job on https://github.com/[your_name]_be_dumbgram

- Create branch `3.Product`.

  ```bash
  git checkout -b 3. Product
  ```

- Push to branch `3. Product `.

  ```bash
    git add .
    git commit -m "add Product "
    git push origin 3. Product
  ```

> `4. Artist`

> `5. Transaction`
