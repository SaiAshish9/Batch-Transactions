```
Spring Batch => Process millions of records faster


spring batch is one of the core module of spring framework and using this we can create robust batch processing system.

Batch processing is a technique which processes data in a large group instead of a single element of data, where we can process a high volume of data with minimal human interaction.

when we need to transfer huge amount of data from source to destination then we must use spring batch.


1. Lets say we want to design a billing analysis system, we've the billing information in the csv format, we want to dump that csv(src) to db (dest). Inserting row by row to the db will be painful , hence we can use batch processing here to speed up process.


2. Report Generation System:

Let's say everyday we need to generate a csv report(destination) by fetching data from the db (source). We can speed up this via spring batch.


Job Launcher is an interface used to launch spring batch jobs.

```
