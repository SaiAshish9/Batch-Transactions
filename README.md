```
Spring Batch => Process millions of records faster


spring batch is one of the core module of spring framework and using this we can create robust batch processing system.

Batch processing is a technique which processes data in a large group instead of a single element of data, where we can process a high volume of data with minimal human interaction.

when we need to transfer huge amount of data from source to destination then we must use spring batch.


1. Lets say we want to design a billing analysis system, we've the billing information in the csv format, we want to dump that csv(src) to db (dest). Inserting row by row to the db will be painful , hence we can use batch processing here to speed up process.


2. Report Generation System:

Let's say everyday we need to generate a csv report(destination) by fetching data from the db (source). We can speed up this via spring batch.

Key components of spring batch architecture : 

Job Launcher is an interface used to launch spring batch jobs and its an entrypoint to initiate any job in spring batch.

It has a run method to trigger job object immediately it calls Job repo which is used to maintain state of job whether its succeed or failed.

State management is crucial when processing large amount of data this is done using spring batch job repository.

Then job component will communicate with another component of spring batch called Step.

Step is combination of ItemReader, ItemProcessor and ItemWriter.

ItemReader reads the data from source (csv), ItemProcessor can be used to perform any operation in between reading and writing data and ItemWriter helps to write data to dest. (db).

A job can have multiple steps.

```

```
brew install mysql

$ brew services stop mysql
$ pkill mysqld
$ rm -rf /usr/local/var/mysql/ # NOTE: this will delete your existing database!!!
$ brew postinstall mysql
$ brew services restart mysql
$ mysql -uroot

We've installed your MySQL database without a root password. To secure it run:
    mysql_secure_installation
    
saiashish

MySQL is configured to only allow connections from localhost by default

To connect run:
    mysql -u root

To start mysql now and restart at login:
  brew services start mysql
```

<img width="712" alt="Screenshot 2023-02-27 at 11 57 49 PM" src="https://user-images.githubusercontent.com/43849911/221651342-f25a77d6-0abc-41d7-ac53-447295c89d3a.png">

<img width="1032" alt="Screenshot 2023-02-28 at 12 04 50 AM" src="https://user-images.githubusercontent.com/43849911/221652661-9283baeb-0b71-4531-a5f9-afce1b8c467c.png">

<img width="1010" alt="Screenshot 2023-02-28 at 1 27 29 AM" src="https://user-images.githubusercontent.com/43849911/221669516-0133e0d7-21f3-4975-b994-0c73c57266cd.png">

<img width="880" alt="Screenshot 2023-02-28 at 1 28 38 AM" src="https://user-images.githubusercontent.com/43849911/221669807-3140855c-58f7-4496-99f5-bc11a4bc61df.png">

<img width="978" alt="Screenshot 2023-02-28 at 1 30 58 AM" src="https://user-images.githubusercontent.com/43849911/221670452-1c5761c6-a91f-4001-9721-bb9973dfb76a.png">

