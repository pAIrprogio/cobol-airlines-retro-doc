# CICS Interfaces Documentation

This document provides an overview of the different interfaces used in the COBOL project, focusing on their fields and details.

## AS-400 Interface: Login Display File (LOGIN-DSPF)

| COBOL Name | Intelligible Name | Description         | Data Type          | Constraints                         |
| ---------- | ----------------- | ------------------- | ------------------ | ----------------------------------- |
| USERID     | User ID           | User identifier     | Alphanumeric (8A)  | Required, Uppercase Only            |
| PASSWORD   | Password          | User password       | Alphanumeric (16A) | Required, Encrypted, Display Masked |
| MSG1       | Message 1         | First message line  | Alphanumeric (68A) | Optional, Display Only              |
| MSG2       | Message 2         | Second message line | Alphanumeric (68A) | Optional, Display Only              |
| DATE       | Date              | Current date        | Date (YY/MM/DD)    | Read-only                           |
| TIME       | Time              | Current time        | Time (HH:MM:SS)    | Read-only                           |

[View file](../AS-400/DSPF/LOGIN-DSPF)

## CICS Interface: Login Map (LOGINMAP)

| COBOL Name | Intelligible Name | Description         | Data Type         | Constraints                         |
| ---------- | ----------------- | ------------------- | ----------------- | ----------------------------------- |
| USERID     | User ID           | User identifier     | Alphanumeric (8)  | Required, Uppercase Only            |
| PASSW      | Password          | User password       | Alphanumeric (8)  | Required, Encrypted, Display Masked |
| LDATE      | Login Date        | Current date        | Date (YY/MM/DD)   | Read-only                           |
| LHOUR      | Login Time        | Current time        | Time (HH:MM:SS)   | Read-only                           |
| MSG1       | Message 1         | First message line  | Alphanumeric (70) | Optional, Display Only              |
| MSG2       | Message 2         | Second message line | Alphanumeric (70) | Optional, Display Only              |

[View file](../CICS/LOGIN/LOGINMAP)

## CICS Interface: Sales Mapping (SELL1-MAP)

| COBOL Name | Intelligible Name | Description          | Data Type         | Constraints                     |
| ---------- | ----------------- | -------------------- | ----------------- | ------------------------------- |
| USERID     | User ID           | User identifier      | Alphanumeric (8)  | Required, Uppercase Only        |
| CLIID      | Client ID         | Client identifier    | Alphanumeric (6)  | Required                        |
| FNUM       | Flight Number     | Flight identifier    | Numeric (6)       | Required                        |
| FDATE      | Flight Date       | Date of flight       | Date (YYYY-MM-DD) | Required, Valid Date            |
| PASSN      | Passenger Number  | Number of passengers | Numeric (1)       | Required, 1-9                   |
| SPRICE     | Single Price      | Price per ticket     | Numeric (22)      | Required, Decimal, Non-negative |
| STPRICE    | Total Price       | Total price          | Numeric (22)      | Required, Decimal, Non-negative |

[View file](../CICS/SALES-MAP/SELL1-MAP)

## CICS Interface: Search Flight Map (SRCHFLI-MAP)

| COBOL Name | Intelligible Name | Description            | Data Type         | Constraints                   |
| ---------- | ----------------- | ---------------------- | ----------------- | ----------------------------- |
| USERID     | User ID           | User identifier        | Alphanumeric (8)  | Required, Uppercase Only      |
| FNUM       | Flight Number     | Flight identifier      | Numeric (6)       | Required                      |
| FDATE      | Flight Date       | Date of flight         | Date (YYYY-MM-DD) | Required, Valid Date          |
| DAIR       | Departure Airport | Departure airport code | Alphanumeric (3)  | Required, Valid Airport Codes |

[View file](../CICS/SALES-MAP/SRCHFLI-MAP)

## CICS Interface: Search Ticket Map (SRCHTKT-MAP)

| COBOL Name | Intelligible Name | Description            | Data Type         | Constraints                   |
| ---------- | ----------------- | ---------------------- | ----------------- | ----------------------------- |
| USERID     | User ID           | User identifier        | Alphanumeric (8)  | Required, Uppercase Only      |
| TKTID      | Ticket ID         | Ticket identifier      | Alphanumeric (10) | Required                      |
| CLIID      | Client ID         | Client identifier      | Alphanumeric (10) | Required                      |
| FNAME      | First Name        | Passenger's first name | Alphanumeric (15) | Required, Valid Name          |
| LNAME      | Last Name         | Passenger's last name  | Alphanumeric (15) | Required, Valid Name          |
| FDATE      | Flight Date       | Date of flight         | Date (YYYY-MM-DD) | Required, Valid Date          |
| FLIID      | Flight ID         | Flight identifier      | Alphanumeric (10) | Required                      |
| STDEP      | Departure Time    | Time of departure      | Time (HH:MM)      | Required, Valid Time          |
| STLAN      | Landing Time      | Time of landing        | Time (HH:MM)      | Required, Valid Time          |
| SDAIR      | Departure Airport | Departure airport code | Alphanumeric (3)  | Required, Valid Airport Codes |
| SLAIR      | Landing Airport   | Landing airport code   | Alphanumeric (3)  | Required, Valid Airport Codes |
| SSEAT      | Seat Number       | Seat number            | Numeric (3)       | Required                      |

[View file](../CICS/SALES-MAP/SRCHTKT-MAP)
