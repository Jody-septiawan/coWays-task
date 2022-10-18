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

# 1. Add Music

**url** = {your*host}/api/v1/music
**recruitments** = \_For image/video file upload, when user add new music, userId automatically insert and associate with music*

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
        "name": "Ariel Noah",
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
        "Image": "<domain>/admin.jpg"
      }
    }
  }
}
```

# 2. Get All Music

**url** = {your_host}/api/v1/musics
**method** = GET
**response body** =

```json
{
  "status": "success",
  "data": {
    "products": [
      {
        "id": 1,
        "thumbnail": "<domain>/balon-ku-ada-lima.png",
        "title": "Balon ku ada 5",
        "year": 2004,
        "singer": {
          "id": 4,
          "name": "Ariel Noah",
          "thumbnail": "<domain>/ariel-noah.png",
          "old": 40,
          "category": "solo",
          "start_career": 2008
        },
        "music_file": "<domain>/balon-ku-ada-lima.mp3"
      },
      {
        "id": 2,
        "thumbnail": "<domain>/balon-ku-ada-enam.png",
        "title": "Balon ku ada 6",
        "year": 2001,
        "singer": {
          "id": 4,
          "name": "Tulus",
          "thumbnail": "<domain>/tulus.png",
          "old": 40,
          "category": "solo",
          "start_career": 2005
        },
        "music_file": "<domain>/balon-ku-ada-enam.mp3"
      },
      {
        "id": 3,
        "thumbnail": "<domain>/balon-ku-ada-tujuh.png",
        "title": "Balon ku ada 7",
        "year": 2010,
        "singer": {
          "id": 4,
          "name": "Rich Brian",
          "thumbnail": "<domain>/rich-brian.png",
          "old": 40,
          "category": "solo",
          "start_career": 2008
        },
        "music_file": "<domain>/balon-ku-ada-tujuh.mp3"
      }
    ]
  }
}
```

# 3. Get music Detail

**url** = {your_host}/api/v1/music/:id
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
      "id": 3,
      "thumbnail": "<domain>/balon-ku-ada-tujuh.png",
      "title": "Balon ku ada 7",
      "year": 2010,
      "singer": {
        "id": 4,
        "name": "Rich Brian",
        "thumbnail": "<domain>/rich-brian.png",
        "old": 40,
        "category": "solo",
        "start_career": 2008
      },
      "music_file": "<domain>/balon-ku-ada-tujuh.mp3"
    }
  }
}
```

# 4. Update music

**url** = {your_host}/api/v1/music/:id
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
  "desc": "Balon ku ada tujuh"
}
```

**response body** =

```json
{
  "status": "success",
  "data": {
    "product": {
      "id": 3,
      "thumbnail": "<domain>/balon-ku-ada-tujuh.png",
      "title": "Balon ku ada tujuh",
      "year": 2010,
      "singer": ,
      "music_file": "<domain>/balon-ku-ada-tujuh.mp3"
    }
  }
}
```

# 5. Delete Music

**url** = {your_host}/api/v1/music/:id
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
    "id": 3
  }
}
```

## B. Instructions

- When you finish this task, move it to "test" list. Then don't forget to push your job on https://github.com/[your_name]_coWays_be

- Create branch `3.Music`.

  ```bash
  git checkout -b 3. Music
  ```

- Push to branch `3. Music `.

  ```bash
    git add .
    git commit -m "add Music "
    git push origin 3. Music
  ```

> `4. Artis`

# ARTIS API

## A. Requirements

# 1. Add Artis

**url** = {your\*host}/api/v1/artis

**recruitments** =

- Handle file For image/video file upload, when user add new artis
- category is `solo` or `group`

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
  "name": "Judika",
  "old": 40,
  "category": "Solo",
  "start_a_career": "2002",
  "thumbnail": "judika-img.jpeg"
}
```

**response body** =

```json
{
  "status": "success",
  "data": {
    "artis": {
      "id": 1,
      "name": "Judika",
      "old": 40,
      "category": "Solo",
      "start_a_career": "2002",
      "thumbnail": "<domain>/judika-img.jpeg"
    }
  }
}
```

# 2. Get all Artis

**url** = {your\*host}/api/v1/artis

**method** = GET

**response body** =

```json
{
  "status": "success",
  "data": {
    "artis": [
        {
          "id": 1,
          "name": "Judika",
          "old": 40,
          "category": "Solo",
          "start_a_career": "2002",
          "thumbnail": "<domain>/judika-img.jpeg"
        },
        {
        "id": 2,
        "name": "Abel Dustin",
        "old": 19,
        "category": "Solo",
        "start_a_career": "2020",
        "thumbnail": "<domain>/abel-img.jpeg"
      }
      {
        "id": 3,
        "name": "Andre Taulany",
        "old": 45,
        "category": "Solo",
        "start_a_career": "1997",
        "thumbnail": "<domain>/andre-img.jpeg"
      }
    ]
  }
}
```

> `5. Transaction`

# 1. Add Transaction

**url** = {your\*host}/api/v1/transaction

**recruitments** =

- Handle file For image/video file upload, when user add new artis
- category is `solo` or `group`

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
  "account_number": "6872364732894234",
  "proof_of_transfer": "68794234-transfer.jpeg"
}
```

**response body** =

```json
{
  "status": "success",
  "data": {
    "transaction": {
      "id": 63,
      "account_number": "6872364732894234",
      "proof_of_transfer": "<domain>/68794234-transfer.jpeg",
      "status": "pending",
      "user": {
        "id": 4,
        "name": "samsul rijal",
        "email": "samsul@gmail.com",
        "status": "customer"
      }
    }
  }
}
```

# 2. Get all transaction

**url** = {your\*host}/api/v1/transactions

**method** = GET

**response body** =

```json
{
  "status": "success",
  "data": {
    "transactions": [
      {
        "id": 10,
        "account_number": "987132123232333",
        "proof_of_transfer": "<domain>/987132123-transfer.jpeg",
        "status": "success",
        "remaining_active": 20,
        "user": {
          "id": 4,
          "name": "Jody Septiawan",
          "email": "jody@gmail.com",
          "status": "customer"
        }
      },
      {
        "id": 17,
        "account_number": "6872364732894234",
        "proof_of_transfer": "<domain>/68794234-transfer.jpeg",
        "status": "pending",
        "remaining_active": 0,
        "user": {
          "id": 4,
          "name": "samsul rijal",
          "email": "samsul@gmail.com",
          "status": "customer"
        }
      },
      {
        "id": 31,
        "account_number": "293489234894234",
        "proof_of_transfer": "<domain>/29348923-transfer.jpeg",
        "status": "success",
        "remaining_active": 27,
        "user": {
          "id": 4,
          "name": "Radifan",
          "email": "radif@gmail.com",
          "status": "customer"
        }
      },
      {
        "id": 63,
        "account_number": "6872364732894234",
        "proof_of_transfer": "<domain>/68794234-transfer.jpeg",
        "status": "pending",
        "remaining_active": 0,
        "user": {
          "id": 4,
          "name": "samsul rijal",
          "email": "samsul@gmail.com",
          "status": "customer"
        }
      }
    ]
  }
}
```
