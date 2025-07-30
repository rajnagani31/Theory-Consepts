# ACID Property (Atomicity ,Consistency ,Isolation ,Durability)

## Atomicity("All or Nothing(NONE)")
#### first ensures it's transection ,start transection and at the time all stapp succesfully commplete so no problum and they commit all data but during transection not pass any step they are use rollback and start again to first stap(it's mean transection is not successfull they use rollback no any data commit they restart) 


## Consistencey:Maintaining valid data sates

#### befor transection sum of all balance of Account "A" and same "b" ,after transection the sum of money like A=1000 -200 ,b =1000 +200 after transection A=800 and b=1200 and data commite

#### EX 2. you buy any product in 1000 rs  but your account avalible balance is 800 so payment method not allow complete the transection so you go in rollback , this process is go rollback all data reading time so any data not commit (mean buyer and seller data as it's as)


## Isolation(no(mix-up) interferencr Between transection)

#### EX 1 :you buy movie ticket and other person buy same movie ticket in same time with isolation only one you can book ,without isolation give errors

#### EX 2 : you creat voting poll in online and pepole are voting same time it's vote calculate in accurate not count double clicked vote and no lost any vote

#### it means it complete onee transection in one time 

## Durability -Saved means saved (even after cresh)

#### you changes any data(voting,pyment,account holder , gaming data) in database this data saved lifetime until it is changed back(after durability then agin any data change ,update ,insert,delete this all data commit and saved life time(durability))

#### EX 1. you payment to shop using upi id and payment success fully execution but after your mobile is crashes so money is save,safe and recorded.


# BASE

##### Basy is an alternative ACID

### BA (Bascically Avaliable)

#### Bascically database system  should  always be available to respond to user request after faile any system becuse BA use replicated data (mean it's data store in another database)

### soft state

#### soft state may change data over time without any new inputs


### Evantully update

#### any data change in database they not change immidate they tech few time (hight trafic ,active users)