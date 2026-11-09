# Architecture Design

## 1. Layered Architecture
* **User layer:** Staff web interface, search interface, dashboard, and administration.
* **Application layer:** Cataloguing, circulation, member management, and fines.
* **RFID middleware:** Device-neutral commands for the staff reader, handheld reader, and security gate.
* **Interoperability:** Mock NCIP 2.0 and SIP2 adapters since vendor endpoints are unavailable.
* **Data layer:** Transactional database, search index, and migration staging area.
* **Integration layer:** Mock connectors for Email, SMS, print, and CCTV photos.
* **Operations layer:** Configuration, logs, and offline installer.

## 2. Mock Contracts
Since physical hardware is excluded, we will use mock software interfaces to simulate the following:
* **Staff Reader Mock:** Simulates scanning a book's RFID tag at the desk.
* **Security Gate Mock:** Simulates detecting an unauthorized book leaving the library.
* **Smart Card Mock:** Simulates a staff member logging in with an ID card.

## 3. Database Schema Overview
* (To be designed: Tables for Books, Members, Transactions, and RFID Tags)
