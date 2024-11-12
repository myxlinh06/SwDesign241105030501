# 1. Subsystem context diagrams



# 2. Analysis class to design element map

| Analysis Class	       | Design Element                |
| ---------------------- |:-----------------------------:|
| LoginForm              | LoginForm                     |
| MaintainTimecardForm   | MainEmployeeForm, TimecardForm|
|                        | MainApplicationForm           |
| TimecarrdController    | TimecardController            |
| SystemClockI           | SystemClockI                  |
| PayrollController      | PayrollController             |
| Paycheck               | Paycheck                      |

# 3. Design element to owning package map

| Design Element	                  | Package             |
| --------------------------------- |:-------------------:|
| LoginForm	                        | com.app.controllers |
| MainEmployeeForm, TimecardForm	  | com.app.services    |
| PaymentGateway    | com.app.payment     |
| DocumentStorage   | com.app.storage     |
