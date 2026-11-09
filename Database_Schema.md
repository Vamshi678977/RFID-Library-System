# Database Schema and Data Dictionary

## 1. Members Table
* **MemberID** (Primary Key): Unique ID for each user.
* **Name**: Full name of the library member.
* **Role**: Determines if they are a 'Patron' or 'Staff'.
* **FinesBalance**: Current amount owed.
* **Status**: Active or Blocked.

## 2. Books (Bibliographic) Table
* **BookID** (Primary Key): Unique ID for the book.
* **Title**: Title of the book.
* **ISBN**: Standard book number.
* **IsReference**: Boolean (True/False) - if True, the book cannot be checked out.

## 3. RFID_Tags Table
* **TagID** (Primary Key): The unique code on the physical RFID sticker.
* **BookID** (Foreign Key): Links the tag to a specific book.
* **Status**: Checked-in, Checked-out, Missing, or Misplaced.

## 4. Circulation (Transactions) Table
* **TransactionID** (Primary Key): Unique record of the event.
* **BookID**: Which book was scanned.
* **MemberID**: Who checked it out.
* **CheckoutDate**: When it left the library.
* **DueDate**: When it must be returned.
* **ReturnDate**: When it was actually returned.
