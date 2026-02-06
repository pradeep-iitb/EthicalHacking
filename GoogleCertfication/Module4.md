# Operating System Fundamentals & Linux Architecture

This guide covers the basic concepts of computer architecture, the history of Linux, and why it is the primary tool for security professionals.

### Logical Operators

#### AND operator
- Requires every condition in the `WHERE` clause to be true.

```sql
SELECT *
FROM machines
WHERE operating_system = 'OS 1'
    AND email_client = 'Email Client 1';
```

Result: Only machines that meet both conditions.

#### OR operator
- Requires at least one condition to be true; records that meet either (or both) conditions are returned.

```sql
SELECT *
FROM machines
WHERE operating_system = 'OS 1'
     OR operating_system = 'OS 3';
```

Result: Machines with OS 1, OS 3, or both.

#### NOT operator
- Excludes records that match the condition, returning everything else.

```sql
SELECT *
FROM machines
WHERE NOT operating_system = 'OS 3';
```

Result: All machines except those running OS 3.

#### Logical operator summary

| Operator | Meaning                          |
| --- | --- |
| AND | All conditions must be true |
| OR  | At least one condition must be true |
| NOT | Excludes matching records |

### Joining Tables in SQL

- Security questions often need data from multiple tables (for example, employee details from `employees` and device details from `machines`). Joins combine that information in a single query.
- Use fully qualified column names when the same column name appears in multiple tables: `table_name.column_name`.

#### Primary key vs foreign key
- Primary key: unique, not `NULL` (example: `employees.employee_id`).
- Foreign key: references a primary key in another table; can contain duplicates or `NULL` (example: `machines.employee_id`).

#### INNER JOIN
- Returns rows where the join column matches in both tables; unmatched rows are excluded, and `NULL` join values are ignored.

```sql
SELECT e.username,
             e.office,
             m.operating_system
FROM employees AS e
INNER JOIN machines AS m
                ON e.employee_id = m.employee_id;
```

FROM clause picks the left table (`employees`), `INNER JOIN` adds the right table (`machines`), and `ON` defines the matching columns. Result: only employees who have an assigned machine appear in the output.

2.  See what is there: `ls`
3.  Enter a folder: `cd reports`
4.  Preview a file: `head update.txt`

# Linux File & Directory Management

This guide covers the essential commands for creating, deleting, moving, and editing files and directories directly from the command line.

---

## 1. Managing Directories

### Create a Directory: `mkdir`
* **Command:** `mkdir [directory_name]`
* **Function:** Creates a new folder.
* **Example:** `mkdir network` (Creates a folder named "network" in your current location).
* **Absolute Path Example:** `mkdir /home/analyst/logs/network`

### Remove a Directory: `rmdir`
* **Command:** `rmdir [directory_name]`
* **Function:** Deletes a directory.
* **Constraint:** The directory **must be empty**. If it contains files, this command will fail.
* **Example:** `rmdir network`

---

## 2. Managing Files

### Create a File: `touch`
* **Command:** `touch [file_name]`
* **Function:** Creates a new, empty file.
* **Example:** `touch permissions.txt`

### Remove a File: `rm`
* **Command:** `rm [file_name]`
* **Function:** Deletes a file permanently.
* **Warning:** Deleted files are hard to recover. Use with caution.
* **Example:** `rm permissions.txt`

### Move or Rename: `mv`
The `mv` command has two distinct functions depending on the arguments used.
1.  **Move:** Moves a file from one location to another.
    * `mv permissions.txt /home/analyst/logs`
2.  **Rename:** Renames a file if the destination is a new filename.
    * `mv permissions.txt perm.txt` (Renames the file to `perm.txt`).

### Copy: `cp`
* **Command:** `cp [source] [destination]`
* **Function:** Duplicates the file or directory. The original remains in place.
* **Example:** `cp permissions.txt /home/analyst/logs`



---

## 3. Editing Files with `nano`

**Nano** is a beginner-friendly command-line text editor standard on most Linux distributions.

* **Open/Create:** `nano filename.txt`
    * If the file exists, it opens it.
    * If the file does *not* exist, it creates it.
* **Save:** Press `Ctrl + O` (Write Out), then `Enter` to confirm the name.
* **Exit:** Press `Ctrl + X`.

---

## 4. Standard Output Redirection

In addition to using a text editor, you can send the output of a command (like `echo`) directly into a file using redirection operators.

| Operator | Name | Function | Example |
| :--- | :--- | :--- | :--- |
| **`>`** | **Overwrite** | Replaces **all** content in the file with the new output. **(Use Caution!)** | `echo "End" > file.txt` |
| **`>>`** | **Append** | Adds the new output to the **end** of the file, keeping existing content. | `echo "Next" >> file.txt` |



> **Note:** Both operators will create the file if it does not already exist.

# Linux User Management & The Sudo Command

This guide covers how to safely manage users (add, delete, modify) and why using `sudo` is the industry standard for system administration.

---

## 1. Authentication vs. Authorization

* **Authentication:** The process of proving *who* you are (e.g., logging in with a password).
* **Authorization:** The process of determining *what* you are allowed to do (e.g., can this user access the "Sales" folder?).

---

## 2. The Root User vs. Sudo

### The Root User (Superuser)
The **Root** user has unlimited power. They can modify, delete, or run *any* file on the system.
* **The Risk:** Logging in directly as Root is **bad practice**.
    1.  **Security:** If a hacker breaches the root account, they have total control.
    2.  **Irreversible Mistakes:** One wrong command can permanently delete critical system directories.
    3.  **No Accountability:** If everyone logs in as Root, you cannot track *who* ran a specific command.

### The Solution: `sudo` (SuperUser DO)
`sudo` is a command that temporarily grants elevated privileges to a specific user to run a single command.
* **How it works:** It acts like a "Master Key" for a janitor. The janitor uses their own ID badge (their account) but borrows the master key (`sudo`) only when needed to open a locked room.
* **Requirement:** Users must be listed in the **sudoers file** to use this command.



---

## 3. User Management Commands

**Note:** All these commands require elevated privileges, so they must start with `sudo`.

### A. Adding Users: `useradd`
Adds a new user to the system.

* **Basic Syntax:** `sudo useradd [username]`
* **Advanced Options:**
    * `-g`: Sets the user's **Primary** group.
    * `-G`: Adds the user to **Supplemental** (secondary) groups.

> **Example:** Add user `fgarcia` to the primary group `security` and supplemental groups `finance` and `admin`.
> ```bash
> sudo useradd -g security -G finance,admin fgarcia
> ```

### B. Modifying Users: `usermod`
Changes the settings for an existing user.

* **Change Primary Group:** `sudo usermod -g [groupname] [username]`
* **Add Supplemental Group:** `sudo usermod -a -G [groupname] [username]`
    * *Important:* You must use `-a` (append) with `-G`. If you forget `-a`, it will **overwrite** all their existing groups with the new one.
* **Lock Account:** `sudo usermod -L [username]`
    * Prevents login without deleting the user's files.
* **Change Home Directory:** `sudo usermod -d [new_directory] [username]`

### C. Deleting Users: `userdel`
Removes a user from the system.

* **Basic Delete:** `sudo userdel [username]`
* **Delete with Files:** `sudo userdel -r [username]`
    * The `-r` flag removes the user **and** their home directory/files. Always backup data before using this!

---

## 4. Changing Ownership: `chown`

The `chown` (Change Owner) command updates who owns a file or directory.

* **Change User Owner:** `sudo chown [new_owner] [filename]`
* **Change Group Owner:** `sudo chown :[new_group] [filename]` (Note the colon `:`)

> **Example:** Change the user owner of `access.txt` to `fgarcia` and the group to `security`.
> ```bash
> sudo chown fgarcia:security access.txt
> ```

# Linux Resources & Support Tools

This guide covers how to find help when working with Linux, both through external community resources and built-in command-line tools.

---

## 1. The Linux Community (External Support)

Because Linux is **open-source**, it has a massive global community of developers and users who constantly contribute knowledge.

* **Online Search:** The fastest way to troubleshoot is often a simple search describing your task (e.g., "how to add a group in Linux").
* **Unix & Linux Stack Exchange:** A highly reputable Q&A website where answers are ranked by points. High-quality solutions float to the top.

---

## 2. Integrated Command-Line Support

Linux includes built-in tools to help you learn about commands without leaving the terminal.

### A. The Manual: `man`
* **Command:** `man [command_name]`
* **Function:** Displays the full **manual page** (man page) for a command.
* **Details:** Includes a general description, syntax, and a list of all possible options/flags (like `-r` or `-g`).
* **Example:** `man chown` (Shows detailed info on how to change file ownership).



### B. Quick Description: `whatis`
* **Command:** `whatis [command_name]`
* **Function:** Displays a one-line description of what a command does.
* **Use Case:** Perfect for when you need a quick reminder of a command's function but don't need the full manual.
* **Example:**
    * Input: `whatis tail`
    * Output: `tail (1) - output the last part of files`

### C. Search by Keyword: `apropos`
* **Command:** `apropos [keyword]`
* **Function:** Searches the *descriptions* of all man pages for a specific string of text.
* **Use Case:** When you know *what* you want to do (e.g., "change password") but don't know the specific command name.
* **Advanced Option:** `apropos -a [keyword1] [keyword2]`
    * The `-a` flag stands for "AND". It filters results to show only commands that contain **both** keywords.
* **Example:** `apropos -a change password` (Finds commands related to changing passwords).

---

## 3. Summary Table

| Command | Mnemonic | Function | When to use it |
| :--- | :--- | :--- | :--- |
| **`man`** | **Man**ual | Shows the full guide. | When you need to know specific flags or syntax. |
| **`whatis`** | **What is** this? | Shows a 1-line summary. | When you just need to identify a command. |
| **`apropos`** | **Apropos** (Relevant) | Searches descriptions. | When you don't know the command name yet. |

# Databases and SQL Fundamentals for Security Analysts

---

## Introduction to Databases

Our modern world is filled with data, and this data often guides important decisions. When working with large amounts of data, it’s essential to store it in a way that is organized, efficient, and easy to access. This is where **databases** come in.

A **database** is an organized collection of information or data.

Databases are often compared to spreadsheets, such as Google Sheets. While spreadsheets are useful, they are generally designed for:
- A single user or small team
- Smaller amounts of data
- Simpler operations

In contrast, databases:
- Can be accessed by multiple users simultaneously
- Can store massive amounts of data
- Can perform complex operations efficiently

---

## Why Databases Matter to Security Analysts

As a security analyst, you will often interact with databases that store:
- Login attempts
- Software and patch updates
- Machines and device ownership
- User activity logs

Databases allow analysts to store, access, and analyze large datasets quickly and efficiently.

---

## Relational Databases

In this course, the focus is on **relational databases**.

A **relational database** is a structured database that contains tables that are related to one another.

---

## Tables, Columns, and Rows

### Tables
A table stores information about a specific subject, such as employees or machines.

### Columns (Fields)
Columns define the type of data stored in the table.
Examples:
- `employee_id`
- `device_id`
- `username`

### Rows (Records)
Rows contain actual data entries related to each column.

Example:
- A row representing an employee with ID `1000` working in the marketing department

---

## Relationships Between Tables

Relational databases often contain multiple tables.

Tables can be connected using a **common column**.  
This connection is called a **relationship**.

Example:
- An `employees` table
- A `machines` table
- Both share the `employee_id` column

---

## Keys in Relational Databases

### Primary Key
- A column where every value is unique
- Cannot contain duplicate or empty (NULL) values
- Used to uniquely identify each row

Example:
- `employee_id` in the employees table

Rules:
- Each table can have only **one primary key**

---

### Foreign Key
- A column that is a primary key in another table
- Can contain duplicate or empty values
- Used to connect tables together

Example:
- `employee_id` in the machines table referencing the employees table

Rules:
- A table can have **multiple foreign keys**

---

## Introduction to SQL

To work with databases, analysts use **SQL**.

**SQL (Structured Query Language)** is a programming language used to:
- Create databases
- Interact with databases
- Request and manipulate data

---

## What is a Query?

A **query** is a request for data from:
- A single database table
- Multiple tables combined

Nearly all relational databases rely on SQL for querying data.

---

## Why SQL Is Important for Security Analysts

SQL is essential for:
- Reviewing large security logs
- Analyzing login attempts
- Identifying misconfigured machines
- Detecting unusual or malicious activity

Security logs often contain millions of records.  
SQL can extract relevant data in **seconds** using a single query.

---

## SQL and Data Analytics

SQL is also widely used for **basic data analytics**.

Security analysts use SQL to:
- Filter data for decision-making
- Identify unpatched systems
- Determine optimal times for system updates
- Detect anomalies and trends

---

## Accessing SQL from Linux

One way to access SQL is through the Linux command line.

Example: Accessing SQLite
```bash
sqlite3
```

# SQL Queries, Filtering, and Ordering — Security Analyst Notes

---

## Running Your First SQL Query

As a security analyst, querying databases is a common task. In this lesson, we start by running a **basic SQL query** to determine which computer is assigned to a specific employee.

### Example Scenario
We have an `employees` table with multiple columns. Two important ones are:
- `employee_id`
- `device_id`

---

## Basic SQL Keywords

### SELECT
- Specifies **which columns** to return

### FROM
- Specifies **which table** to query

---

## Example: Selecting Specific Columns

```sql
SELECT employee_id, device_id
FROM employees;
```

# SQL Filtering with Numeric, Date, and Time Data

---

## Introduction

In this section, we expand SQL filtering beyond strings and apply it to **numeric**, **date**, and **time** data types. As a security analyst, this is extremely important because investigations often depend on **counts, timestamps, and date ranges**.

---

## Common Database Data Types

### 1. String Data
- An ordered sequence of characters
- Can include letters, numbers, and symbols
- Examples:
  - usernames (`analyst10`)
  - country names (`USA`)
  - office names (`East-120`)

➡️ **Strings use quotation marks** in SQL filters.

---

### 2. Numeric Data
- Consists only of numbers
- Can be used in mathematical operations
- Examples:
  - number of login attempts
  - login_id
  - employee_id

➡️ **Numbers do NOT use quotation marks**.

---

### 3. Date and Time Data
- Represents dates and/or times
- Common formats:
  - Date: `YYYY-MM-DD`
  - Time: `HH:MM:SS`

Examples:
- `2023-02-01`
- `18:00:00`

➡️ **Dates and times use quotation marks**.

---

## SQL Operators for Numbers and Dates

Common operators used with numeric and date/time data:

| Operator | Meaning |
|--------|--------|
| `=` | Equal to |
| `>` | Greater than |
| `<` | Less than |
| `!=` or `<>` | Not equal to |
| `>=` | Greater than or equal to |
| `<=` | Less than or equal to |
| `BETWEEN` | Within a range |

---

## Filtering by Time (After Business Hours)
### Example: Login attempts after 6 PM

```sql
SELECT *
FROM log_in_attempts
WHERE login_time > '18:00:00';
```

_Note:_ `18:00:00` represents 6:00 PM. This filter is useful for detecting suspicious after-hours activity.

### Filtering by Date Range Using BETWEEN

**Example:** Machines patched between March 1 and September 1, 2021

```sql
SELECT *
FROM machines
WHERE OS_patch_date BETWEEN '2021-03-01' AND '2021-09-01';
```

_Note:_ `BETWEEN` includes both the start and end dates.
BETWEEN includes both start and end dates

Ideal for patch compliance checks

employee details → employees table

### Important Syntax Rules

| Data Type | Use Quotes? |
|-----------|-------------:|
| String    | ✅ Yes |
| Date      | ✅ Yes |
| Time      | ✅ Yes |
| Numeric   | ❌ No |

## Lab: Apply More Filters in SQL

### Activity Overview
This lab focuses on advanced filtering using:

- Dates
- Time
- Ranges
- Unique identifiers

These skills help analysts narrow down logs during investigations.

### Scenario
You are working with the organization database and analyzing the `log_in_attempts` table to investigate suspicious activity.

### Task 1 — Login Attempts After a Certain Date
- Goal: Find login attempts after January 15, 2023.

```sql
SELECT *
FROM log_in_attempts
WHERE login_date > '2023-01-15';
```

Answer: There were 112 login attempts after January 15, 2023.

### Task 2 — Login Attempts Within a Date Range
- Goal: Find login attempts between February 1 and February 7, 2023.

```sql
SELECT *
FROM log_in_attempts
WHERE login_date BETWEEN '2023-02-01' AND '2023-02-07';
```

Answer: There were 88 login attempts in this date range.

### Task 3 — Login Attempts at a Specific Time
- Goal: Find login attempts at exactly 09:30 AM.

```sql
SELECT *
FROM log_in_attempts
WHERE login_time = '09:30:00';
```

Answer: There were 5 login attempts at 09:30:00.

### Task 4 — Login Attempt by ID
- Goal: Find details for login attempt with `login_id = 503`.

```sql
SELECT *
FROM log_in_attempts
WHERE login_id = 503;
```

Answer: The login date for login ID 503 was 2023-02-10.

### Key Takeaways

- SQL supports powerful filtering using numeric, date, and time data.
- Use comparison operators (`>`, `<`, `=`, `BETWEEN`) for precise analysis.
- Dates and times must be enclosed in quotes; numeric values should not be quoted.
- These filters are critical for threat detection and incident investigation.

---

# SQL: Multiple Conditions and Joining Tables

## Filtering with Multiple Conditions in SQL

In real-world security analysis, filtering data often requires **more than one condition**. For example, identifying vulnerabilities may depend on:

- a specific **operating system**
- a specific **email client**

To handle this, SQL provides **logical operators** that allow multiple conditions in a single query.

## AND Operator

### What it does
- The `AND` operator requires **all conditions** to be true.
- Only records that satisfy **every condition** are returned.

### Analogy
Selecting apples that are **large AND fresh**  
→ small fresh apples ❌  
→ large rotten apples ❌  
→ only large fresh apples ✅

### SQL Example
Find machines running **OS 1** *and* using **Email Client 1**:

```sql
SELECT *
FROM machines
WHERE operating_system = 'OS 1'
    AND email_client = 'Email Client 1';
```

## OR Operator

### What it does
- The `OR` operator requires at least one condition to be true.
- Records that meet either condition (or both) are returned.

### Analogy
Selecting fruit that is an apple OR an orange.

### SQL Example
Find machines running OS 1 OR OS 3:

```sql
SELECT *
FROM machines
WHERE operating_system = 'OS 1'
     OR operating_system = 'OS 3';
```

## NOT Operator

### What it does
- The `NOT` operator excludes records that match a condition.
- It returns everything except what is specified.

### Analogy
Selecting any fruit that is NOT an apple.

### SQL Example
Find machines that are not running OS 3:

```sql
SELECT *
FROM machines
WHERE NOT operating_system = 'OS 3';
```

## Summary of Logical Operators

| Operator | Meaning |
|---------:|:--------|
| `AND`    | All conditions must be true |
| `OR`     | At least one condition must be true |
| `NOT`    | Excludes matching records |

## Joining Tables in SQL

### Why Join Tables?
Security questions often require data from multiple tables. For example:

- employee details → `employees` table
- device and OS details → `machines` table

Joining tables allows analysts to combine related information in a single query.

### Table and Column Referencing
When multiple tables have the same column name, qualify columns with the table name using `table_name.column_name` (for example, `employees.employee_id` or `machines.employee_id`).

### Primary Key vs Foreign Key

- **Primary Key**: Unique, no NULL values (e.g., `employee_id` in `employees`).
- **Foreign Key**: References a primary key in another table; can have duplicates or NULL values (e.g., `employee_id` in `machines`).

## INNER JOIN

### What it does
- Returns rows where there is a matching value in both tables.
- Rows without a match are excluded. Rows with `NULL` in the join column are not included.

### INNER JOIN Example

Goal: Get employee username, office location, and operating system of their machine.

```sql
SELECT employees.username,
             employees.office,
             machines.operating_system
FROM employees
INNER JOIN machines
    ON employees.employee_id = machines.employee_id;
```

Explanation:

- `FROM employees` → left table
- `INNER JOIN machines` → right table
- `ON` defines how the tables are connected; join occurs where `employee_id` matches in both tables.

Result: Only employees who have an assigned machine appear in the output.


