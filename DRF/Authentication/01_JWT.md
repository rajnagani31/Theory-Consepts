# JWT (Json Web token)

They gunreat Two key Public(They avaliable and share publicly) and Privet (They not avaliable in public and they not shard)

# state less and state full (they use many place)

-> state less is meaning is they not stord in dataa base
it's mean jwt is not stord in database

-> state full meaning is they stord data in data base

# what is JWT

JWT is like a digital ID card that websites and apps use to prove who you are and to let you stay logged in without asking for your password every time.

JWT is sturcturd in 3 part 

### 1.Header

think like "lable" on box

    {
    "alg": "HS256",
    "typ": "JWT"
    }

### 2.Payload

    {
    "id": 123,
    "name": "Raj",
    "role": "admin"
    }

### Signature

This is like the lock on the box.

It ensures nobody has changed the Header or Payload.

It’s created by combining the header + payload + secret key and running them through a formula (hash).