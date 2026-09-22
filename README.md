# 💻 freeCodeCamp Python Workshops & Exercises

This repository contains practical workshops, algorithm challenges, and beginner-level projects completed as part of the **freeCodeCamp** Python curriculum.

---

## 📚 Table of Contents
* [Overview](#-overview)
* [Workshop 1: Ticket Pricing & Conditional Logic](#-workshop-1-ticket-pricing--conditional-logic)
* [Workshop 2: Employee Data Processing & String Manipulation](#-workshop-2-employee-data-processing--string-manipulation)
* [Technologies Used](#-technologies-used)

---

## 🎯 Overview

The goal of this repository is to document my Python learning journey, track progress through freeCodeCamp exercises, and showcase foundational programming concepts such as conditional logic, data types, string manipulation, and string slicing.

---

## 🎟️ Workshop 1: Ticket Pricing & Conditional Logic

### 📝 Overview
Demonstrates control flow, multi-condition logic (`if-elif-else`), logical operators (`and`, `or`, `not`), and dynamic variable updates in a movie ticket booking system.

```python
base_price = 15
age = 21
seat_type = 'Gold'
show_time = 'Evening'

if age > 17:
    print('User is eligible to book a ticket')

if age >= 21:
    print('User is eligible for Evening shows')
else:
    print('User is not eligible for Evening shows')

is_member = False
is_weekend = False

discount = 0
if is_member and age >= 21:
    discount = 3
    print('User qualifies for membership discount')
else:
    print('User does not qualify for membership discount')
print('Discount:', discount)

extra_charges = 0
if is_weekend or show_time == 'Evening':
    extra_charges = 2
    print('Extra charges will be applied')
else:
    print('No extra charges will be applied')
print('Extra charges:', extra_charges)

if age >= 21 or age >= 18 and (show_time != 'Evening' or is_member):
    print('Ticket booking condition satisfied')

    service_charges = 0
    if seat_type == 'Premium':
        service_charges = 5
    elif seat_type == 'Gold':
        service_charges = 3
    else:
        service_charges = 1
    print('Service charges:', service_charges)

    final_price = base_price - discount + extra_charges + service_charges
    print('Final price of ticket:', final_price)
else:
    print('Ticket booking failed due to restriction')
