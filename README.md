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

<img width="712" alt="Screenshot 2023-02-27 at 11 57 49 PM" src="https://user-images.githubusercontent.com/43849911/221651342-f25a77d6-0abc-41d7-ac53-447295c89d3a.png">

