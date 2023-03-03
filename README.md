# Littlelemon Booking system

## Introduction
This is the final project of Coursera course Meta The Full Stack https://www.coursera.org/learn/the-full-stack/

A booking system of Littlelemon restaurant. The front end javascript code of book page communicates with the api provided by back end.

Tech stack: Django + DRF + JavaScript + MySql

## Misc
There are several typos in the given template of the course. One of the main typo will affect the function that "the current date is automatically selected when opening the booking form". 

In the begining of the script of 'book.html', the original code:
```html
document.getElementById('reservation_date').value = `${date.getFullYear()}-${date.getMonth() + 1}-${date.getDate().toString().padStart(2, "0")}`
```
There are at least two ways to fix this:

1. 
```html
document.getElementById('reservation_date').value = 
  `${date.getFullYear()}-${(date.getMonth()+1).toString().padStart(2, "0")}-${date.getDate().toString().padStart(2, "0")}`
```
2. 
```html
document.getElementById('reservation_date').valueAsDate = date
```