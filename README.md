# Python Programming Assignments - Data Structures & Algorithms

This repository contains Python solutions and experimental investigations for practical programming problems focusing on core data structures, slicing, dictionaries, sets, list comprehensions, nested data structures, and algorithmic design.

---

## Table of Contents
1. [Q1: Lists and Slicing - Daily Rainfall Records](#q1-lists-and-slicing---daily-rainfall-records)
2. [Q3: Dictionaries - Farmer Helpline Complaint Analysis](#q3-dictionaries---farmer-helpline-complaint-analysis)
3. [Q4: Sets - Elective Registration Clash Detection](#q4-sets---elective-registration-clash-detection)
4. [Q5: List Comprehension - Cleaning Sensor Readings](#q5-list-comprehension---cleaning-sensor-readings)
5. [Q6: Nested Data - A Railway Timetable](#q6-nested-data---a-railway-timetable)
6. [Q7: Contact-Merging Program from First Principles](#q7-contact-merging-program-from-first-principles)

---

## Q1: Lists and Slicing: Daily Rainfall Records
* **Context:** Village Rain-Gauge Station recording daily rainfall values.
* **Key Implementation Tasks:**
  * Computes weekly totals using list slicing.
  * Finds maximum and minimum weekly totals with their positions (wettest and driest weeks).
  * Computes a 7-day moving average using both naive and optimized running-sum approaches.
  * Identifies the list of dry days ($0$ mm).
* **Experimental Analysis:** Benchmarks performance across $365$, $36,500$, and $365,000$ readings.

---

## Q3: Dictionaries: Farmer Helpline Complaint Analysis
* **Context:** Kisan Call Centre recording text of farmer complaints.
* **Key Implementation Tasks:**
  * Counts word frequencies using dictionaries with `.get()` and `.setdefault()`, excluding common stop words.
  * Groups complaints by district into a dictionary of lists.
  * Retrieves top-$k$ most frequent words sorted by frequency (descending) and alphabetically (ascending) for ties.
* **Experimental Analysis:** Benchmarks custom dictionary counting against `collections.Counter` and list `.count()` methods across large text corpora.

---

## Q4: Sets: Elective Registration Clash Detection
* **Context:** Academic office managing elective course registrations and timetable clashes.
* **Key Implementation Tasks:**
  * Stores each elective's registration numbers in a set.
  * Uses set operations (`&`, `^`, `-`, `|`) and set methods (`intersection`, `symmetric_difference`, `difference`, `union`).
  * Finds students in both electives (clash), students in exactly one, and students who have not registered at all.
* **Experimental Analysis:** Compares membership testing and intersection performance between lists and sets for large datasets.

---

## Q5: List Comprehension: Cleaning Sensor Readings
* **Context:** Cold-storage unit temperature monitoring for vaccines.
* **Key Implementation Tasks:**
  * Cleans and validates sensor readings (filtering out-of-range error values).
  * Converts Celsius temperatures to Fahrenheit.
  * Generates alarm minutes outside acceptable temperature ranges using `enumerate()`.
* **Experimental Analysis:** Compares execution time and memory footprint (`sys.getsizeof()`) across traditional loops, list comprehensions, `map`/`filter`, and generator expressions.

---

## Q6: Nested Data: A Railway Timetable
* **Context:** Station enquiry counter tracking train timetables.
* **Key Implementation Tasks:**
  * Builds a nested data structure containing dictionaries, lists, tuples, and sets mapping train numbers to names, stops, and running days.
  * Queries trains stopping at a given station on a specific day, sorted by departure time using `sorted()` with `key=lambda`.
* **Experimental Analysis:** Investigates the trade-offs of building secondary indices (`station -> list of trains`) to speed up search queries.

---

## Q7: Contact-Merging Program from First Principles
* **Context:** Consolidating phone contacts from multiple sources with varied naming and phone number formats.
* **Key Implementation Tasks:**
  * Normalizes phone numbers (stripping non-digit characters and standardizing formats).
  * Merges records using a dictionary keyed by the normalized primary number, utilizing sets for alternate numbers and email addresses.
* **Experimental Analysis:** Evaluates algorithmic complexity ($O(n^2)$ pairwise comparison vs $O(n)$ dictionary lookup) across thousands of contact records.

---

## Running the Code
Ensure you have Python 3.7+ installed. Run any script using your terminal:
```bash
python script_name.py
