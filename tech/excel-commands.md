This comprehensive cheat sheet covers an array of **Excel functions** across various categories, including [**Cube**](#cube-functions), [**Database**](#database-functions), [**Date and Time**](#date-and-time-functions), [**Engineering**](#engineering-functions), [**Financial**](#financial-functions), [**Information**](#information-functions), [**Logical**](#logical-functions), [**Lookup and Reference**](#lookup-and-reference-functions), [**Math and Trigonometry**](#math-and-trigonometry-functions),[ **Statistical**](#statistical-functions), [**Text**](#text-functions), [**User Defined**](#user-defined-functions), and [**Web**](#web-functions) **functions**. Each section introduces functions with simple, clear examples to illustrate their usage, helping users understand how to apply these tools in their data analysis tasks. From performing basic calculations and data analysis to handling complex formulas and extracting web data, this cheat sheet serves as a go-to guide for Excel users seeking to enhance their spreadsheet skills. Whether you're calculating financial forecasts, analyzing statistical data, or manipulating text strings, this cheat sheet provides the essential information to leverage [Excel's powerful functions](https://support.microsoft.com/en-us/office/excel-functions-alphabetical-b3944572-255d-4efb-bb96-c6d90033e188) effectively.

## Cube functions

### CUBEKPIMEMBER

Returns a key performance indicator (KPI) property and displays the KPI name in the cell. A KPI is a quantifiable measurement, such as monthly gross profit or quarterly employee turnover, that is used to monitor an organization's performance.

**Example:** `=CUBEKPIMEMBER("Adventure Works", "[Measures].[Internet Sales Amount]", 2)` returns the goal of the Internet Sales Amount KPI from the Adventure Works cube.

### CUBEMEMBER

Returns a member or tuple from the cube. Use to validate that the member or tuple exists in the cube.

**Example:** `=CUBEMEMBER("Adventure Works", "[Product].[All Products].[Bikes]")` returns the Bikes category from the Product dimension in the Adventure Works cube.

### CUBEMEMBERPROPERTY

Returns the value of a member property from the cube. Use to validate that a member name exists within the cube and to return the specified property for this member.

**Example:** `=CUBEMEMBERPROPERTY("Adventure Works", "[Employee].[Employees].[John Smith]", "Email")` returns the email address of John Smith from the Adventure Works cube.

### CUBERANKEDMEMBER

Returns the nth, or ranked, member in a set. Use to return one or more elements in a set, such as the top sales performer or the top 10 students.

**Example:** `=CUBERANKEDMEMBER("Adventure Works", "[Product].[All Products]", 1)` returns the top product from the All Products set in the Adventure Works cube.

### CUBESET

Defines a calculated set of members or tuples by sending a set expression to the cube on the server, which creates the set, and then returns that set to Microsoft Excel.

**Example:** `=CUBESET("Adventure Works", "{[Product].[Category].[Bikes], [Product].[Category].[Accessories]}", "Bikes and Accessories")` defines a set consisting of Bikes and Accessories categories in the Adventure Works cube.

### CUBESETCOUNT

Returns the number of items in a set.

**Example:** `=CUBESETCOUNT(CUBESET("Adventure Works", "{[Product].[Category].[Bikes], [Product].[Category].[Accessories]}"))` returns the number of items in the set defined by Bikes and Accessories categories.

### CUBEVALUE

Returns an aggregated value from the cube.

**Example:** `=CUBEVALUE("Adventure Works", "[Measures].[Internet Sales Amount]", "[Time].[2008]", "[Product].[Category].[Bikes]")` returns the total internet sales amount for bikes in 2008 from the Adventure Works cube.

## Database functions

### DAVERAGE

Returns the average of selected database entries.

**Example:** `=DAVERAGE(database, field, criteria)` calculates the average salary in a database of employees who meet certain criteria.

### DCOUNT

Counts the cells that contain numbers in a database.

**Example:** `=DCOUNT(database, field, criteria)` counts the number of employees in a database who meet certain criteria.

### DCOUNTA

Counts nonblank cells in a database.

**Example:** `=DCOUNTA(database, field, criteria)` counts the number of nonblank entries for a specified field in a database that meet certain criteria.

### DGET

Extracts from a database a single record that matches the specified criteria.

**Example:** `=DGET(database, field, criteria)` retrieves the salary of a specific employee from a database.

### DMAX

Returns the maximum value from selected database entries.

**Example:** `=DMAX(database, field, criteria)` finds the highest salary in a database of employees who meet certain criteria.

### DMIN

Returns the minimum value from selected database entries.

**Example:** `=DMIN(database, field, criteria)` finds the lowest salary in a database of employees who meet certain criteria.

### DPRODUCT

Multiplies the values in a particular field of records that match the criteria in a database.

**Example:** `=DPRODUCT(database, field, criteria)` multiplies the sales figures of certain products in a database.

### DSTDEV

Estimates the standard deviation based on a sample of selected database entries.

**Example:** `=DSTDEV(database, field, criteria)` estimates the standard deviation of salaries in a database of employees who meet certain criteria.

### DSTDEVP

Calculates the standard deviation based on the entire population of selected database entries.

**Example:** `=DSTDEVP(database, field, criteria)` calculates the standard deviation of salaries for all employees in a database.

### DSUM

Adds the numbers in the field column of records in the database that match the criteria.

**Example:** `=DSUM(database, field, criteria)` sums the salaries of employees in a database who meet certain criteria.

### DVAR

Estimates variance based on a sample from selected database entries.

**Example:** `=DVAR(database, field, criteria)` estimates the variance of sales figures for certain products in a database.

### DVARP

Calculates variance based on the entire population of selected database entries.

**Example:** `=DVARP(database, field, criteria)` calculates the variance of sales figures for all products in a database.


## Date and Time functions

### DATE

Returns the serial number of a particular date.

**Example:** `=DATE(2023, 12, 31)` returns the serial number for December 31, 2023.

### DATEDIF

Calculates the number of days, months, or years between two dates.

**Example:** `=DATEDIF("2023-01-01", "2024-01-01", "Y")` calculates the number of years between January 1, 2023, and January 1, 2024.

### DATEVALUE

Converts a date in the form of text to a serial number.

**Example:** `=DATEVALUE("12/31/2023")` converts the text "12/31/2023" to a serial number.

### DAY

Converts a serial number to a day of the month.

**Example:** `=DAY(43830)` converts the serial number 43830 to the day of the month.

### DAYS

Returns the number of days between two dates.

**Example:** `=DAYS("2024-01-01", "2023-01-01")` returns the number of days between January 1, 2023, and January 1, 2024.

### DAYS360

Calculates the number of days between two dates based on a 360-day year.

**Example:** `=DAYS360("2023-01-01", "2024-01-01")` calculates the number of days between January 1, 2023, and January 1, 2024, based on a 360-day year.

### EDATE

Returns the serial number of the date that is the indicated number of months before or after the start date.

**Example:** `=EDATE("2023-01-01", 1)` returns the serial number for February 1, 2023.

### EOMONTH

Returns the serial number of the last day of the month before or after a specified number of months.

**Example:** `=EOMONTH("2023-01-01", 1)` returns the serial number for the last day of February 2023.

### HOUR

Converts a serial number to an hour.

**Example:** `=HOUR("15:00")` returns 15.

### ISOWEEKNUM

Returns the number of the ISO week number of the year for a given date.

**Example:** `=ISOWEEKNUM("2023-01-01")` returns the ISO week number for January 1, 2023.

### MINUTE

Converts a serial number to a minute.

**Example:** `=MINUTE("15:30")` returns 30.

### MONTH

Converts a serial number to a month.

**Example:** `=MONTH("2023-12-31")` returns 12 for December.

### NETWORKDAYS

Returns the number of whole workdays between two dates.

**Example:** `=NETWORKDAYS("2023-01-01", "2023-01-31")` returns the number of workdays in January 2023.

### NETWORKDAYS.INTL

Returns the number of whole workdays between two dates using parameters to indicate which and how many days are weekend days.

**Example:** `=NETWORKDAYS.INTL("2023-01-01", "2023-01-31", 1)` calculates workdays considering Saturday and Sunday as weekends.

### NOW

Returns the serial number of the current date and time.

**Example:** `=NOW()` returns the current date and time.

### SECOND

Converts a serial number to a second.

**Example:** `=SECOND("15:30:25")` returns 25.

### TIME

Returns the serial number of a particular time.

**Example:** `=TIME(15, 30, 25)` returns the serial number for 3:30:25 PM.

### TIMEVALUE

Converts a time in the form of text to a serial number.

**Example:** `=TIMEVALUE("15:30:25")` converts "15:30:25" to a serial number.

### TODAY

Returns the serial number of today's date.

**Example:** `=TODAY()` returns the current date.

### WEEKDAY

Converts a serial number to a day of the week.

**Example:** `=WEEKDAY("2023-01-01")` returns the day of the week for January 1, 2023.

### WEEKNUM

Converts a serial number to a number representing where the week falls numerically within a year.

**Example:** `=WEEKNUM("2023-01-01")` returns the week number for January 1, 2023.

### WORKDAY

Returns the serial number of the date before or after a specified number of workdays.

**Example:** `=WORKDAY("2023-01-01", 10)` returns the serial number for the date 10 workdays after January 1, 2023.

### WORKDAY.INTL

Returns the serial number of the date before or after a specified number of workdays using parameters to indicate which and how many days are weekend days.

**Example:** `=WORKDAY.INTL("2023-01-01", 10, 1)` calculates the date 10 workdays after January 1, 2023, considering Saturday and Sunday as weekends.

### YEAR

Converts a serial number to a year.

**Example:** `=YEAR("2023-12-31")` returns 2023.

### YEARFRAC

Returns the year fraction representing the number of whole days between start_date and end_date.

**Example:** `=YEARFRAC("2023-01-01", "2024-01-01")` returns the fraction of the year that represents the number of whole days between January 1, 2023, and January 1, 2024.


## Engineering functions

### BESSELI

Returns the modified Bessel function In(x).

**Example:** `=BESSELI(2.5,1)` calculates the modified Bessel function In(x) for x=2.5 and n=1.

### BESSELJ

Returns the Bessel function Jn(x).

**Example:** `=BESSELJ(2.5,1)` calculates the Bessel function Jn(x) for x=2.5 and n=1.

### BESSELK

Returns the modified Bessel function Kn(x).

**Example:** `=BESSELK(2.5,1)` calculates the modified Bessel function Kn(x) for x=2.5 and n=1.

### BESSELY

Returns the Bessel function Yn(x).

**Example:** `=BESSELY(2.5,1)` calculates the Bessel function Yn(x) for x=2.5 and n=1.

### BIN2DEC

Converts a binary number to decimal.

**Example:** `=BIN2DEC(101)` converts the binary number 101 to its decimal equivalent.

### BIN2HEX

Converts a binary number to hexadecimal.

**Example:** `=BIN2HEX(101)` converts the binary number 101 to its hexadecimal equivalent.

### BIN2OCT

Converts a binary number to octal.

**Example:** `=BIN2OCT(101)` converts the binary number 101 to its octal equivalent.

### BITAND

Returns a 'Bitwise And' of two numbers.

**Example:** `=BITAND(5,3)` calculates the bitwise AND of 5 and 3.

### BITLSHIFT

Returns a value number shifted left by shift_amount bits.

**Example:** `=BITLSHIFT(5,2)` shifts the number 5 left by 2 bits.

### BITOR

Returns a bitwise OR of 2 numbers.

**Example:** `=BITOR(5,3)` calculates the bitwise OR of 5 and 3.

### BITRSHIFT

Returns a value number shifted right by shift_amount bits.

**Example:** `=BITRSHIFT(5,2)` shifts the number 5 right by 2 bits.

### BITXOR

Returns a bitwise 'Exclusive Or' of two numbers.

**Example:** `=BITXOR(5,3)` calculates the bitwise XOR of 5 and 3.

### COMPLEX

Converts real and imaginary coefficients into a complex number.

**Example:** `=COMPLEX(3,4)` converts the real coefficient 3 and the imaginary coefficient 4 into a complex number.

### CONVERT

Converts a number from one measurement system to another.

**Example:** `=CONVERT(100,"cm","m")` converts 100 centimeters to meters.

### DEC2BIN

Converts a decimal number to binary.

**Example:** `=DEC2BIN(5)` converts the decimal number 5 to its binary equivalent.

### DEC2HEX

Converts a decimal number to hexadecimal.

**Example:** `=DEC2HEX(255)` converts the decimal number 255 to its hexadecimal equivalent.

### DEC2OCT

Converts a decimal number to octal.

**Example:** `=DEC2OCT(8)` converts the decimal number 8 to its octal equivalent.

### DELTA

Tests whether two values are equal.

**Example:** `=DELTA(5,5)` returns 1 since the two numbers are equal.

### ERF

Returns the error function.

**Example:** `=ERF(1)` calculates the error function for the value 1.

### ERF.PRECISE

Returns the error function.

**Example:** `=ERF.PRECISE(1)` calculates the precise error function for the value 1.

### ERFC

Returns the complementary error function.

**Example:** `=ERFC(1)` calculates the complementary error function for the value 1.

### ERFC.PRECISE

Returns the complementary ERF function integrated between x and infinity.

**Example:** `=ERFC.PRECISE(1)` calculates the precise complementary error function for the value 1.

### GESTEP

Tests whether a number is greater than a threshold value.

**Example:** `=GESTEP(5,4)` returns 1 since 5 is greater than the threshold 4.

### HEX2BIN

Converts a hexadecimal number to binary.

**Example:** `=HEX2BIN("F")` converts the hexadecimal number F to its binary equivalent.

### HEX2DEC

Converts a hexadecimal number to decimal.

**Example:** `=HEX2DEC("F")` converts the hexadecimal number F to its decimal equivalent.

### HEX2OCT

Converts a hexadecimal number to octal.

**Example:** `=HEX2OCT("F")`converts the hexadecimal number F to its octal equivalent.

### IMABS

Returns the absolute value (modulus) of a complex number.

**Example:** `=IMABS("3+4i")` calculates the modulus of the complex number 3+4i, which is 5.

### IMAGINARY

Returns the imaginary coefficient of a complex number.

**Example:** `=IMAGINARY("3+4i")` extracts the imaginary part of 3+4i, which is 4.

### IMARGUMENT

Returns the argument theta, an angle expressed in radians.

**Example:** `=IMARGUMENT("3+4i")` calculates the argument of the complex number 3+4i.

### IMCONJUGATE

Returns the complex conjugate of a complex number.

**Example:** `=IMCONJUGATE("3+4i")` returns the complex conjugate of 3+4i, which is 3-4i.

### IMCOS

Returns the cosine of a complex number.

**Example:** `=IMCOS("3+4i")` calculates the cosine of the complex number 3+4i.

### IMCOSH

Returns the hyperbolic cosine of a complex number.

**Example:** `=IMCOSH("3+4i")` calculates the hyperbolic cosine of the complex number 3+4i.

### IMCOT

Returns the cotangent of a complex number.

**Example:** `=IMCOT("3+4i")` calculates the cotangent of the complex number 3+4i.

### IMCSC

Returns the cosecant of a complex number.

**Example:** `=IMCSC("3+4i")` calculates the cosecant of the complex number 3+4i.

### IMCSCH

Returns the hyperbolic cosecant of a complex number.

**Example:** `=IMCSCH("3+4i")` calculates the hyperbolic cosecant of the complex number 3+4i.

### IMDIV

Returns the quotient of two complex numbers.

**Example:** `=IMDIV("3+4i", "1+2i")` calculates the quotient of the complex numbers 3+4i and 1+2i.

### IMEXP

Returns the exponential of a complex number.

**Example:** `=IMEXP("3+4i")` calculates the exponential of the complex number 3+4i.

### IMLN

Returns the natural logarithm of a complex number.

**Example:** `=IMLN("3+4i")` calculates the natural logarithm of the complex number 3+4i.

### IMLOG10

Returns the base-10 logarithm of a complex number.

**Example:** `=IMLOG10("3+4i")` calculates the base-10 logarithm of the complex number 3+4i.

### IMLOG2

Returns the base-2 logarithm of a complex number.

**Example:** `=IMLOG2("3+4i")` calculates the base-2 logarithm of the complex number 3+4i.

### IMPOWER

Returns a complex number raised to an integer power.

**Example:** `=IMPOWER("3+4i", 2)` calculates the complex number 3+4i raised to the power of 2.

### IMPRODUCT

Returns the product of from 2 to 255 complex numbers.

**Example:** `=IMPRODUCT("3+4i", "1+2i")` calculates the product of the complex numbers 3+4i and 1+2i.

### IMREAL

Returns the real coefficient of a complex number.

**Example:** `=IMREAL("3+4i")` extracts the real part of 3+4i, which is 3.

### IMSEC

Returns the secant of a complex number.

**Example:** `=IMSEC("3+4i")` calculates the secant of the complex number 3+4i.

### IMSECH

Returns the hyperbolic secant of a complex number.

**Example:** `=IMSECH("3+4i")` calculates the hyperbolic secant of the complex number 3+4i.

### IMSIN

Returns the sine of a complex number.

**Example:** `=IMSIN("3+4i")` calculates the sine of the complex number 3+4i.

### IMSINH

Returns the hyperbolic sine of a complex number.

**Example:** `=IMSINH("3+4i")` calculates the hyperbolic sine of the complex number 3+4i.

### IMSQRT

Returns the square root of a complex number.

**Example:** `=IMSQRT("3+4i")` calculates the square root of the complex number 3+4i.

### IMSUB

Returns the difference between two complex numbers.

**Example:** `=IMSUB("5+6i", "3+4i")` calculates the difference between the complex numbers 5+6i and 3+4i, resulting in 2+2i.

### IMSUM

Returns the sum of complex numbers.

**Example:** `=IMSUM("1+2i", "3+4i")` calculates the sum of the complex numbers 1+2i and 3+4i, resulting in 4+6i.

### IMTAN

Returns the tangent of a complex number.

**Example:** `=IMTAN("3+4i")` calculates the tangent of the complex number 3+4i.

### OCT2BIN

Converts an octal number to binary.

**Example:** `=OCT2BIN(7)` converts the octal number 7 to its binary equivalent.

### OCT2DEC

Converts an octal number to decimal.

**Example:** `=OCT2DEC(10)` converts the octal number 10 to its decimal equivalent.

### OCT2HEX

Converts an octal number to hexadecimal.

**Example:** `=OCT2HEX(20)` converts the octal number 20 to its hexadecimal equivalent.


## Financial functions

### ACCRINT

Returns the accrued interest for a security that pays periodic interest.

**Example:** `=ACCRINT(issue_date, first_interest, settlement, rate, par, frequency, [basis], [calc_method])`

### ACCRINTM

Returns the accrued interest for a security that pays interest at maturity.

**Example:** `=ACCRINTM(issue_date, settlement, rate, par, [basis])`

### AMORDEGRC

Returns the depreciation for each accounting period by using a depreciation coefficient.

**Example:** `=AMORDEGRC(cost, date_purchased, first_period, salvage, period, rate, [basis])`

### AMORLINC

Returns the depreciation for each accounting period.

**Example:** `=AMORLINC(cost, date_purchased, first_period, salvage, period, rate, [basis])`

### COUPDAYBS

Returns the number of days from the beginning of the coupon period to the settlement date.

**Example:** `=COUPDAYBS(settlement, maturity, frequency, [basis])`

### COUPDAYS

Returns the number of days in the coupon period that contains the settlement date.

**Example:** `=COUPDAYS(settlement, maturity, frequency, [basis])`

### COUPDAYSNC

Returns the number of days from the settlement date to the next coupon date.

**Example:** `=COUPDAYSNC(settlement, maturity, frequency, [basis])`

### COUPNCD

Returns the next coupon date after the settlement date.

**Example:** `=COUPNCD(settlement, maturity, frequency, [basis])`

### COUPNUM

Returns the number of coupons payable between the settlement date and maturity date.

**Example:** `=COUPNUM(settlement, maturity, frequency, [basis])`

### COUPPCD

Returns the previous coupon date before the settlement date.

**Example:** `=COUPPCD(settlement, maturity, frequency, [basis])`

### CUMIPMT

Returns the cumulative interest paid between two periods.

**Example:** `=CUMIPMT(rate, nper, pv, start_period, end_period, type)`

### CUMPRINC

Returns the cumulative principal paid on a loan between two periods.

**Example:** `=CUMPRINC(rate, nper, pv, start_period, end_period, type)`

### DB

Returns the depreciation of an asset for a specified period by using the fixed-declining balance method.

**Example:** `=DB(cost, salvage, life, period, [month])`

### DDB

Returns the depreciation of an asset for a specified period by using the double-declining balance method or some other method you specify.

**Example:** `=DDB(cost, salvage, life, period, [factor])`

### DISC

Returns the discount rate for a security.

**Example:** `=DISC(settlement, maturity, pr, redemption, [basis])`

### DOLLARDE

Converts a dollar price, expressed as a fraction, into a dollar price, expressed as a decimal number.

**Example:** `=DOLLARDE(fractional_dollar, fraction)`

### DOLLARFR

Converts a dollar price, expressed as a decimal number, into a dollar price, expressed as a fraction.

**Example:** `=DOLLARFR(decimal_dollar, fraction)`

### DURATION

Returns the annual duration of a security with periodic interest payments.

**Example:** `=DURATION(settlement, maturity, coupon, yld, frequency, [basis])`

### EFFECT

Returns the effective annual interest rate.

**Example:** `=EFFECT(nominal_rate, npery)`

### FV

Returns the future value of an investment.

**Example:** `=FV(rate, nper, pmt, [pv], [type])`

### FVSCHEDULE

Returns the future value of an initial principal after applying a series of compound interest rates.

**Example:** `=FVSCHEDULE(principal, schedule)`

### INTRATE

Returns the interest rate for a fully invested security.

**Example:** `=INTRATE(settlement, maturity, investment, redemption, [basis])`

### IPMT

Returns the interest payment for an investment for a given period.

**Example:** `=IPMT(rate, per, nper, pv, [fv], [type])`

### IRR

Returns the internal rate of return for a series of cash flows.

**Example:** `=IRR(values, [guess])`

### ISPMT

Calculates the interest paid during a specific period of an investment.

**Example:** `=ISPMT(rate, per, nper, pv)`

### MDURATION

Returns the Macauley modified duration for a security with an assumed par value of $100.

**Example:** `=MDURATION(settlement, maturity,coupon, yld, frequency, [basis])`

### MIRR

Returns the internal rate of return where positive and negative cash flows are financed at different rates.

**Example:** `=MIRR(values, finance_rate, reinvest_rate)`

### NOMINAL

Returns the annual nominal interest rate.

**Example:** `=NOMINAL(effect_rate, npery)`

### NPER

Returns the number of periods for an investment.

**Example:** `=NPER(rate, pmt, pv, [fv], [type])`

### NPV

Returns the net present value of an investment based on a series of periodic cash flows and a discount rate.

**Example:** `=NPV(rate, value1, [value2], ...)`

### ODDFPRICE

Returns the price per $100 face value of a security with an odd first period.

**Example:** `=ODDFPRICE(settlement, maturity, issue, first_coupon, rate, yld, redemption, frequency, [basis])`

### ODDFYIELD

Returns the yield of a security with an odd first period.

**Example:** `=ODDFYIELD(settlement, maturity, issue, first_coupon, rate, pr, redemption, frequency, [basis])`

### ODDLPRICE

Returns the price per $100 face value of a security with an odd last period.

**Example:** `=ODDLPRICE(settlement, maturity, last_interest, rate, yld, redemption, frequency, [basis])`

### ODDLYIELD

Returns the yield of a security with an odd last period.

**Example:** `=ODDLYIELD(settlement, maturity, last_interest, rate, pr, redemption, frequency, [basis])`

### PDURATION

Returns the number of periods required by an investment to reach a specified value.

**Example:** `=PDURATION(rate, pv, fv)`

### PMT

Returns the periodic payment for an annuity.

**Example:** `=PMT(rate, nper, pv, [fv], [type])`

### PPMT

Returns the payment on the principal for an investment for a given period.

**Example:** `=PPMT(rate, per, nper, pv, [fv], [type])`

### PRICE

Returns the price per $100 face value of a security that pays periodic interest.

**Example:** `=PRICE(settlement, maturity, rate, yld, redemption, frequency, [basis])`

### PRICEDISC

Returns the price per $100 face value of a discounted security.

**Example:** `=PRICEDISC(settlement, maturity, discount, redemption, [basis])`

### PRICEMAT

Returns the price per $100 face value of a security that pays interest at maturity.

**Example:** `=PRICEMAT(settlement, maturity, issue, rate, yld, [basis])`

### PV

Returns the present value of an investment.

**Example:** `=PV(rate, nper, pmt, [fv], [type])`

### RATE

Returns the interest rate per period of an annuity.

**Example:** `=RATE(nper, pmt, pv, [fv], [type], [guess])`

### RECEIVED

Returns the amount received at maturity for a fully invested security.

**Example:** `=RECEIVED(settlement, maturity, investment, discount, [basis])`

### RRI

Returns an equivalent interest rate for the growth of an investment.

**Example:** `=RRI(nper, pv, fv)`

### SLN

Returns the straight-line depreciation of an asset for one period.

**Example:** `=SLN(cost, salvage, life)`

### SYD

Returns the sum-of-years' digits depreciation of an asset for a specified period.

**Example:** `=SYD(cost, salvage, life, per)`

### TBILLEQ

Returns the bond-equivalent yield for a Treasury bill.

**Example:** `=TBILLEQ(settlement, maturity, discount)`

### TBILLPRICE

Returns the price per $100 face value for a Treasury bill.

**Example:** `=TBILLPRICE(settlement, maturity, discount)`

### TBILLYIELD

Returns the yield for a Treasury bill.

**Example:** `=TBILLYIELD(settlement, maturity, pr)`

### VDB

Returns the depreciation of an asset for a specified or partial period by using a declining balance method.

**Example:** `=VDB(cost, salvage, life, start_period, end_period, [factor], [no_switch])`

### XIRR

Returns the internal rate of return for a schedule of cash flows that is not necessarily periodic.

**Example:** `=XIRR(values, dates, [guess])`

### XNPV

Returns the net present value for a schedule of cash flows that is not necessarily periodic.

**Example:** `=XNPV(rate, values, dates)`

### YIELD

Returns the yield on a security that pays periodic interest.

**Example:** `=YIELD(settlement, maturity, rate, pr, redemption, frequency, [basis])`

### YIELDDISC

Returns the annual yield for a discounted security; for example, a Treasury bill.

**Example:** `=YIELDDISC(settlement, maturity, pr, redemption, [basis])`

### YIELDMAT

Returns the annual yield of a security that pays interest at maturity.

**Example:** `=YIELDMAT(settlement, maturity, issue, rate, pr, [basis])`


## Information functions

### CELL

Returns information about the formatting, location, or contents of a cell.

**Example:** `=CELL("type", A1)` returns the type of data in cell A1.

### ERROR.TYPE

Returns a number corresponding to an error type.

**Example:** `=ERROR.TYPE(A1)` returns a number that corresponds to the type of error in cell A1.

### INFO

Returns information about the current operating environment.

**Example:** `=INFO("osversion")` returns the version of the operating system.

### ISBLANK

Returns TRUE if the value is blank.

**Example:** `=ISBLANK(A1)` checks if cell A1 is empty.

### ISERR

Returns TRUE if the value is any error value except #N/A.

**Example:** `=ISERR(A1)` checks if cell A1 contains any error except #N/A.

### ISERROR

Returns TRUE if the value is any error value.

**Example:** `=ISERROR(A1)` checks if cell A1 contains any error.

### ISEVEN

Returns TRUE if the number is even.

**Example:** `=ISEVEN(2)` checks if 2 is an even number.

### ISFORMULA

Returns TRUE if there is a reference to a cell that contains a formula.

**Example:** `=ISFORMULA(A1)` checks if cell A1 contains a formula.

### ISLOGICAL

Returns TRUE if the value is a logical value.

**Example:** `=ISLOGICAL(TRUE)` checks if TRUE is a logical value.

### ISNA

Returns TRUE if the value is the #N/A error value.

**Example:** `=ISNA(A1)` checks if cell A1 contains the #N/A error.

### ISNONTEXT

Returns TRUE if the value is not text.

**Example:** `=ISNONTEXT(A1)` checks if the value in A1 is not text.

### ISNUMBER

Returns TRUE if the value is a number.

**Example:** `=ISNUMBER(A1)` checks if the value in A1 is a number.

### ISODD

Returns TRUE if the number is odd.

**Example:** `=ISODD(3)` checks if 3 is an odd number.

### ISOMITTED

Checks whether the value in a LAMBDA is missing and returns TRUE or FALSE.

**Example:** `=ISOMITTED(A1)` checks if an argument expected by a LAMBDA function is missing in A1.

### ISREF

Returns TRUE if the value is a reference.

**Example:** `=ISREF(A1)` checks if A1 is a reference to a cell.

### ISTEXT

Returns TRUE if the value is text.

**Example:** `=ISTEXT(A1)` checks if the value in A1 is text.

### N

Returns a value converted to a number.

**Example:** `=N("10")` converts the text "10" into the number 10.

### NA

Returns the error value #N/A.

**Example:** `=NA()` returns the #N/A error value.

### SHEET

Returns the sheet number of the referenced sheet.

**Example:** `=SHEET()` returns the sheet number of the sheet containing the formula.

### SHEETS

Returns the number of sheets in a reference.

**Example:** `=SHEETS(A1:C10)` returns the number of sheets that include the range A1:C10.

### TYPE

Returns a number indicating the data type of a value.

**Example:** `=TYPE(A1)` returns a number indicating the data type of the value in cell A1.


## Logical functions

### AND

Returns TRUE if all of its arguments are TRUE.

**Example:** `=AND(TRUE, TRUE)` returns TRUE.

### BYCOL

Applies a LAMBDA to each column and returns an array of the results.

**Example:** `=BYCOL(A1:B2, LAMBDA(a, SUM(a)))` applies a LAMBDA that sums each column in the range A1:B2.

### BYROW

Applies a LAMBDA to each row and returns an array of the results.

**Example:** `=BYROW(A1:B2, LAMBDA(a, SUM(a)))` applies a LAMBDA that sums each row in the range A1:B2.

### FALSE

Returns the logical value FALSE.

**Example:** `=FALSE()` returns FALSE.

### IF

Specifies a logical test to perform.

**Example:** `=IF(A1>10, "High", "Low")` returns "High" if A1 is greater than 10, otherwise returns "Low".

### IFERROR

Returns a value you specify if a formula evaluates to an error; otherwise, returns the result of the formula.

**Example:** `=IFERROR(1/0, "Error in calculation")` returns "Error in calculation" since dividing by zero is an error.

### IFNA

Returns the value you specify if the expression resolves to #N/A, otherwise returns the result of the expression.

**Example:** `=IFNA(VLOOKUP(A1, B:C, 2, FALSE), "Not Found")` returns "Not Found" if the VLOOKUP results in #N/A.

### IFS

Checks whether one or more conditions are met and returns a value that corresponds to the first TRUE condition.

**Example:** `=IFS(A1>10, "High", A1>5, "Medium", TRUE, "Low")` returns "High" if A1 is greater than 10, "Medium" if A1 is greater than 5 but less than or equal to 10, and "Low" otherwise.

### LAMBDA

Create custom, reusable functions and call them by a friendly name.

**Example:** `=LAMBDA(x, x^2)(3)` defines a LAMBDA that squares a number and then applies it to the number 3, resulting in 9.

### LET

Assigns names to calculation results.

**Example:** `=LET(x, 5, x*2)` assigns the name x to the value 5, then calculates x*2, resulting in 10.

### MAKEARRAY

Returns a calculated array of a specified row and column size, by applying a LAMBDA.

**Example:** `=MAKEARRAY(2, 2, LAMBDA(r, c, r+c))` creates a 2x2 array where each value is the sum of its row and column indices.

### MAP

Returns an array formed by mapping each value in the array(s) to a new value by applying a LAMBDA to create a new value.

**Example:** `=MAP({1,2,3}, LAMBDA(a, a^2))` squares each number in the array {1,2,3}.

### NOT

Reverses the logic of its argument.

**Example:** `=NOT(FALSE)` returns TRUE because it reverses the logic of FALSE.

### OR

Returns TRUE if any argument is TRUE.

**Example:** `=OR(FALSE, TRUE)` returns TRUE because at least one argument is TRUE.

### REDUCE

Reduces an array to an accumulated value by applying a LAMBDA to each value and returning the total value in the accumulator.

**Example:** `=REDUCE(0, {1,2,3}, LAMBDA(acc, x, acc + x))` sums the numbers in the array {1,2,3}, starting with an initial accumulator of 0.

### SCAN

Scans an array by applying a LAMBDA to each value and returns an array that has each intermediate value.

**Example:** `=SCAN(0, {1,2,3}, LAMBDA(acc, x, acc + x))` returns an array of the cumulative sums of {1,2,3}.

### SWITCH

Evaluates an expression against a list of values and returns the result corresponding to the first matching value. If there is no match, an optional default value may be returned.

**Example:** `=SWITCH(A1, 1, "One", 2, "Two", "Other")` returns "One" if A1 is 1, "Two" if A1 is 2, and "Other" otherwise.

### TRUE

Returns the logical value TRUE.

**Example:** `=TRUE()` returns TRUE.

### XOR

Returns a logical exclusive OR of all arguments.

**Example:** `=XOR(TRUE, FALSE)` returns TRUE because an odd number ofarguments are TRUE.

### XOR

Returns a logical exclusive OR of all arguments.

**Example:** `=XOR(TRUE, FALSE)` returns TRUE because an odd number of arguments are TRUE. If both arguments were TRUE or both were FALSE, it would return FALSE. This function is useful for checking if an odd number of conditions are met.



## Lookup and reference functions

### ADDRESS

Returns a reference as text to a single cell in a worksheet.

**Example:** `=ADDRESS(1, 1)` returns `$A$1`.

### AREAS

Returns the number of areas in a reference.

**Example:** `=AREAS((A1:B2,C3:D4))` returns `2`.

### CHOOSE

Chooses a value from a list of values.

**Example:** `=CHOOSE(2, "First", "Second", "Third")` returns `"Second"`.

### CHOOSECOLS

Returns the specified columns from an array.

**Example:** Not directly applicable without a dynamic array context.

### CHOOSEROWS

Returns the specified rows from an array.

**Example:** Not directly applicable without a dynamic array context.

### COLUMN

Returns the column number of a reference.

**Example:** `=COLUMN(D4)` returns `4`.

### COLUMNS

Returns the number of columns in a reference.

**Example:** `=COLUMNS(A1:C3)` returns `3`.

### DROP

Excludes a specified number of rows or columns from the start or end of an array.

**Example:** Not directly applicable without a dynamic array context.

### EXPAND

Expands or pads an array to specified row and column dimensions.

**Example:** Not directly applicable without a dynamic array context.

### FILTER

Filters a range of data based on criteria you define.

**Example:** `=FILTER(A1:A10, B1:B10>5)` filters values in `A1:A10` where corresponding `B` values are greater than `5`.

### FORMULATEXT

Returns the formula at the given reference as text.

**Example:** `=FORMULATEXT(A1)` returns the formula in cell A1 as text.

### GETPIVOTDATA

Returns data stored in a PivotTable report.

**Example:** `=GETPIVOTDATA("Sales", A3)`.

### HLOOKUP

Looks in the top row of an array and returns the value of the indicated cell.

**Example:** `=HLOOKUP("Value", A1:D2, 2, FALSE)`.

### HSTACK

Appends arrays horizontally and in sequence to return a larger array.

**Example:** Not directly applicable without a dynamic array context.

### HYPERLINK

Creates a shortcut or jump that opens a document stored on a network server, an intranet, or the Internet.

**Example:** `=HYPERLINK("http://www.example.com", "Click Here")`.

### IMAGE

Returns an image from a given source.

**Example:** `=IMAGE("https://example.com/image.png")`.

### INDEX

Uses an index to choose a value from a reference or array.

**Example:** `=INDEX(A1:C3, 2, 2)` returns the value in the second row and second column of range A1:C3.

### INDIRECT

Returns a reference indicated by a text value.

**Example:** `=INDIRECT("A1")` returns the value in A1.

### LOOKUP

Looks up values in a vector or array.

**Example:** `=LOOKUP(2, {1,2,3}, {"a","b","c"})` returns `"b"`.

### MATCH

Looks up values in a reference or array.

**Example:** `=MATCH(9, A1:A10, 0)` returns the position of the first occurrence of `9` in the range A1:A10.

### OFFSET

Returns a reference offset from a given reference.

**Example:** `=OFFSET(A1, 1, 1)` returns the value one row down and one column right from A1.

### ROW

Returns the row number of a reference.

**Example:** `=ROW(C5)` returns `5`.

### ROWS

Returns the number of rows in a reference.

**Example:** `=ROWS(A1:A10)` returns `10`.

### RTD

Retrieves real-time data from a program that supports COM automation.

**Example:** Not directly applicable without a real-time data source.

### SORT

Sorts the contents of a range or array.

**Example:** `=SORT(A1:A10)` sorts the values in range A1:A10.

### SORTBY

Sorts the contents of a range or array based on the values in a corresponding range or array.

**Example:** `=SORTBY(A1:A10, B1:B10)` sorts values in A1:A10 based on the sorting of values in B1:B10.

### TAKE

Returns a specified number of contiguous rows or columns from the start or end of an array.

**Example:** Not directly applicable without a dynamic array context.

### TOCOL

Returns the array in a single column.

**Example:** Not directly applicable without a dynamic array context.

### TOROW

Returns the array in a single row.

**Example:** Not directly applicable without a dynamic array context.

### TRANSPOSE

Returns the transpose of an array.

**Example:** `=TRANSPOSE(A1:B2)` would switch the rows and columns of the range A1:B2.

### UNIQUE

Returns a list of unique values in a list or range.

**Example:** `=UNIQUE(A1:A10)` returns the unique values from the range A1:A10.

### VLOOKUP

Looks in the first column of an array and moves across the row to return the value of a cell.

**Example:** `=VLOOKUP("SearchKey", A1:B10, 2, FALSE)` finds "SearchKey" in the first column of A1:B10 and returns the value from the second column.

### VSTACK

Appends arrays vertically and in sequence to return a larger array.

**Example:** Not directly applicable without a dynamic array context.

### WRAPCOLS

Wraps the provided row or column of values by columns after a specified number of elements.

**Example:** Not directly applicable without a dynamic array context.

### WRAPROWS

Wraps the provided row or column of values by rows after a specified number of elements.

**Example:** Not directly applicable without a dynamic array context.

### XLOOKUP

Searches a range or an array, and returns an item corresponding to the first match it finds. If a match doesn't exist, then XLOOKUP can return the closest (approximate) match.

**Example:** `=XLOOKUP("SearchKey", A1:A10, B1:B10)` searches for "SearchKey" in A1:A10 and returns the corresponding value from B1:B10.

### XMATCH

Returns the relative position of an item in an array or range of cells.

**Example:** `=XMATCH("SearchKey", A1:A10)` returns the position of "SearchKey" within the range A1:A10.


## Math and trigonometry functions
### ABS

Returns the absolute value of a number.

**Example:** `=ABS(-5)` returns `5`.

### ACOS

Returns the arccosine of a number.

**Example:** `=ACOS(0.5)` returns `1.047197551`.

### ACOSH

Returns the inverse hyperbolic cosine of a number.

**Example:** `=ACOSH(10)` returns `2.993222846`.

### ACOT

Returns the arccotangent of a number.

**Example:** `=ACOT(1)` returns `0.785398163`.

### ACOTH

Returns the hyperbolic arccotangent of a number.

**Example:** `=ACOTH(10)` returns `0.100335347`.

### AGGREGATE

Returns an aggregate in a list or database.

**Example:** `=AGGREGATE(1, 6, A1:A10)` calculates the average of A1:A10, ignoring errors.

### ARABIC

Converts a Roman number to Arabic, as a number.

**Example:** `=ARABIC("IV")` returns `4`.

### ASIN

Returns the arcsine of a number.

**Example:** `=ASIN(0.5)` returns `0.523598776`.

### ASINH

Returns the inverse hyperbolic sine of a number.

**Example:** `=ASINH(10)` returns `2.99822295`.

### ATAN

Returns the arctangent of a number.

**Example:** `=ATAN(1)` returns `0.785398163`.

### ATAN2

Returns the arctangent from x- and y-coordinates.

**Example:** `=ATAN2(1,1)` returns `0.785398163`.

### ATANH

Returns the inverse hyperbolic tangent of a number.

**Example:** `=ATANH(0.1)` returns `0.100335348`.

### BASE

Converts a number into a text representation with the given radix (base).

**Example:** `=BASE(10,2)` converts `10` to binary, resulting in `1010`.

### CEILING

Rounds a number to the nearest integer or to the nearest multiple of significance.

**Example:** `=CEILING(2.5, 1)` returns `3`.

### CEILING.MATH

Rounds a number up, to the nearest integer or to the nearest multiple of significance.

**Example:** `=CEILING.MATH(2.5, 1)` returns `3`.

### CEILING.PRECISE

Rounds a number the nearest integer or to the nearest multiple of significance. Regardless of the sign of the number, the number is rounded up.

**Example:** `=CEILING.PRECISE(-2.5, 2)` returns `-2`.

### COMBIN

Returns the number of combinations for a given number of objects.

**Example:** `=COMBIN(5,2)` calculates the combinations of 5 items taken 2 at a time, resulting in `10`.

### COMBINA

Returns the number of combinations with repetitions for a given number of items.

**Example:** `=COMBINA(5,2)` returns `15`.

### COS

Returns the cosine of a number.

**Example:** `=COS(PI()/3)` returns `0.5`.

### COSH

Returns the hyperbolic cosine of a number.

**Example:** `=COSH(0)` returns `1`.

### COT

Returns the cotangent of an angle.

**Example:** `=COT(PI()/4)` returns `1`.

### COTH

Returns the hyperbolic cotangent of a number.

**Example:** `=COTH(2)` returns `1.0373147207`.

### CSC

Returns the cosecant of an angle.

**Example:** Not directly applicable without a dynamic array context.

### CSCH

Returns the hyperbolic cosecant of an angle.

**Example:** Not directly applicable without a dynamic array context.

### DECIMAL

Converts a text representation of a number in a given base into a decimal number.

**Example:** `=DECIMAL("A", 16)` converts the hexadecimal number `A` to decimal, resulting in `10`.

### DEGREES

Converts radians to degrees.

**Example:** `=DEGREES(PI())` converts π radians to degrees, resulting in `180`.

### EVEN

Rounds a number up to the nearest even integer.

**Example:** `=EVEN(3)` returns `4`.

### EXP

Returns *e* raised to the power of a given number.

**Example:** `=EXP(1)` returns Euler's number *e*.

### FACT

Returns the factorial of a number.

**Example:** `=FACT(5)` returns `120`.

### FACTDOUBLE

Returns the double factorial ofa number.

**Example:** `=FACTDOUBLE(5)` returns `15`.

### FLOOR

Rounds a number down, toward zero.

**Example:** `=FLOOR(2.5, 1)` returns `2`.

### FLOOR.MATH

Rounds a number down, to the nearest integer or to the nearest multiple of significance.

**Example:** `=FLOOR.MATH(2.5, 1)` returns `2`.

### FLOOR.PRECISE

Rounds a number down to the nearest integer or to the nearest multiple of significance. Regardless of the sign of the number, the number is rounded down.

**Example:** `=FLOOR.PRECISE(-2.5, 2)` returns `-4`.

### GCD

Returns the greatest common divisor.

**Example:** `=GCD(8, 12)` returns `4`.

### INT

Rounds a number down to the nearest integer.

**Example:** `=INT(2.9)` returns `2`.

### ISO.CEILING

Returns a number that is rounded up to the nearest integer or to the nearest multiple of significance.

**Example:** `=ISO.CEILING(4.3)` returns `5`.

### LCM

Returns the least common multiple.

**Example:** `=LCM(4, 5)` returns `20`.

### LET

Assigns names to calculation results to allow storing intermediate calculations, values, or defining names inside a formula.

**Example:** `=LET(x, 2, x*x)` defines `x` as `2` and calculates `x*x`, resulting in `4`.

### LN

Returns the natural logarithm of a number.

**Example:** `=LN(E())` returns `1`.

### LOG

Returns the logarithm of a number to a specified base.

**Example:** `=LOG(100, 10)` returns `2`.

### LOG10

Returns the base-10 logarithm of a number.

**Example:** `=LOG10(100)` returns `2`.

### MDETERM

Returns the matrix determinant of an array.

**Example:** Not directly applicable without a matrix context.

### MINVERSE

Returns the matrix inverse of an array.

**Example:** Not directly applicable without a matrix context.

### MMULT

Returns the matrix product of two arrays.

**Example:** Not directly applicable without a matrix context.

### MOD

Returns the remainder from division.

**Example:** `=MOD(10, 3)` returns `1`.

### MROUND

Returns a number rounded to the desired multiple.

**Example:** `=MROUND(10, 3)` returns `9`.

### MULTINOMIAL

Returns the multinomial of a set of numbers.

**Example:** `=MULTINOMIAL(2, 3, 4)` returns `1260`.

### MUNIT

Returns the unit matrix or the specified dimension.

**Example:** Not directly applicable without a matrix context.

### ODD

Rounds a number up to the nearest odd integer.

**Example:** `=ODD(2)` returns `3`.

### PI

Returns the value of pi.

**Example:** `=PI()` returns approximately `3.14159265358979`.

### POWER

Returns the result of a number raised to a power.

**Example:** `=POWER(2, 3)` returns `8`.

### PRODUCT

Multiplies its arguments.

**Example:** `=PRODUCT(2, 3, 4)` returns `24`.

### QUOTIENT

Returns the integer portion of a division.

**Example:** `=QUOTIENT(8, 3)` returns `2`.

### RADIANS

Converts degrees to radians.

**Example:** `=RADIANS(180)` returns π.

### RAND

Returns a random number between 0 and 1.

**Example:** `=RAND()` generates a random number.

### RANDARRAY

Returns an array of random numbers between 0 and 1. 

**Example:** `=RANDARRAY(2,3)` generates a 2x3 array of random numbers.

### RANDBETWEEN

Returns a random number between the numbers you specify.

**Example:** `=RANDBETWEEN(1, 10)` returns a random integer between 1 and 10.

### ROMAN

Converts an Arabic numeral to Roman, as text.

**Example:** `=ROMAN(4)` returns `IV`.

### ROUND

Rounds a number to a specified number of digits.

**Example:** `=ROUND(2.567, 2)` returns `2.57`.

### ROUNDDOWN

Rounds a number down, toward zero.

**Example:** `=ROUNDDOWN(2.567, 2)` returns `2.56`.

### ROUNDUP

Rounds a number up, away from zero.

**Example:** `=ROUNDUP(2.567, 2)` returns `2.57`.

### SEC

Returns the secant of an angle.

**Example:** `=SEC(45)` provides the secant of 45 degrees in radians.

### SECH

Returns the hyperbolic secant of an angle.

**Example:** `=SECH(2)` gives the hyperbolic secant of 2.

### SERIESSUM

Returns the sum of a power series based on the formula.

**Example:** `=SERIESSUM(2,0,1,A1:A4)` calculates the power series sum based on coefficients in A1:A4.

### SEQUENCE

Generates a list of sequential numbers in an array, such as 1, 2, 3, 4.

**Example:** `=SEQUENCE(4)` generates an array of 1, 2, 3, 4.

### SIGN

Returns the sign of a number.

**Example:** `=SIGN(-10)` returns `-1`.

### SIN

Returns the sine of the given angle.

**Example:** `=SIN(PI()/2)` returns `1`.

### SINH

Returns the hyperbolic sine of a number.

**Example:** `=SINH(1)` returns `1.175201194`.

### SQRT

Returns a positive square root.

**Example:** `=SQRT(16)` returns `4`.

### SQRTPI

Returns the square root of (number * pi).

**Example:** `=SQRTPI(9)` returns approximately `5.317`.

### SUBTOTAL

Returns a subtotal in a list or database.

**Example:** `=SUBTOTAL(9, A1:A10)` calculates the sum of A1:A10, ignoring hidden rows.

### SUM

Adds its arguments.

**Example:** `=SUM(1, 2, 3, 4)` returns `10`.

### SUMIF

Adds the cells specified by a given criteria.

**Example:** `=SUMIF(A1:A10, ">5", B1:B10)` sums values in B1:B10 where corresponding A1:A10 are greater than 5.

### SUMIFS

Adds the cells in a range that meet multiple criteria.

**Example:** `=SUMIFS(B1:B10, A1:A10, ">5", C1:C10, "<10")` sums B1:B10 where A1:A10 > 5 and C1:C10 < 10.

### SUMPRODUCT

Returns the sum of the products of corresponding array components.

**Example:** `=SUMPRODUCT(A1:A3, B1:B3)` multiplies each element of A1:A3 with the corresponding element of B1:B3 and sums them up.

### SUMSQ

Returns the sum of the squares of the arguments.

**Example:** `=SUMSQ(1, 2, 3, 4)` returns `30` (1^2 + 2^2 + 3^2 + 4^2).

### SUMX2MY2

Returns the sum of the difference of squares of corresponding values in two arrays.

**Example:** `=SUMX2MY2(A1:A3, B1:B3)` computes the sum of (A^2 - B^2) for each corresponding A and B.

### SUMX2PY2

Returns the sum of the sum of squares of corresponding values in two arrays.

**Example:** `=SUMX2PY2(A1:A3, B1:B3)` computes the sum of (A^2 + B^2) for each corresponding A and B.

### SUMXMY2

Returns the sum of squares of differences of corresponding values in two arrays.

**Example:** `=SUMXMY2(A1:A3, B1:B3)` computes the sum of (A-B)^2 for each corresponding A and B.

### TAN

Returns the tangent of a number.

**Example:** `=TAN(PI()/4)` returns `1`.

### TANH

Returns the hyperbolic tangent of a number.

**Example:** `=TANH(1)` returns `0.761594156`.

### TRUNC

Truncates a number to an integer.

**Example:** `=TRUNC(8.9)` returns `8`.


## Statistical functions

### AVEDEV

Returns the average of the absolute deviations of data points from their mean.

**Example:** `=AVEDEV(1, 2, 3, 4, 5)` calculates the average of the absolute deviations from the mean of the numbers 1 through 5.

### AVERAGE

Returns the average of its arguments.

**Example:** `=AVERAGE(1, 2, 3, 4, 5)` calculates the average of the numbers 1 through 5.

### AVERAGEA

Returns the average of its arguments, including numbers, text, and logical values.

**Example:** `=AVERAGEA(1, "2", TRUE)` calculates the average, treating text as 0 and TRUE as 1.

### AVERAGEIF

Returns the average (arithmetic mean) of all the cells in a range that meet a given criteria.

**Example:** `=AVERAGEIF(A1:A5, ">3")` calculates the average of numbers greater than 3 in the range A1:A5.

### AVERAGEIFS

Returns the average (arithmetic mean) of all cells that meet multiple criteria.

**Example:** `=AVERAGEIFS(A1:A5, A1:A5, ">3", B1:B5, "<5")` calculates the average of numbers greater than 3 and corresponding values in B1:B5 less than 5.

### BETA.DIST

Returns the beta cumulative distribution function.

**Example:** `=BETA.DIST(2, 8, 10, TRUE, 1, 3)` calculates the beta cumulative distribution function.

### BETA.INV

Returns the inverse of the cumulative distribution function for a specified beta distribution.

**Example:** `=BETA.INV(0.5, 8, 10, 1, 3)` calculates the inverse beta cumulative distribution function.

### BINOM.DIST

Returns the individual term binomial distribution probability.

**Example:** `=BINOM.DIST(6, 10, 0.5, FALSE)` calculates the probability of getting exactly 6 successes in 10 trials.

### BINOM.DIST.RANGE

Returns the probability of a trial result using a binomial distribution.

**Example:** `=BINOM.DIST.RANGE(10, 0.5, 5, 7)` calculates the probability of getting between 5 and 7 successes in 10 trials.

### BINOM.INV

Returns the smallest value for which the cumulative binomial distribution is less than or equal to a criterion value.

**Example:** `=BINOM.INV(10, 0.5, 0.75)` finds the smallest number of successes in 10 trials for which the cumulative binomial distribution is less than or equal to 0.75.

### CHISQ.DIST

Returns the cumulative beta probability density function.

**Example:** `=CHISQ.DIST(10, 5, TRUE)` calculates the left-tailed probability of the chi-squared distribution.

### CHISQ.DIST.RT

Returns the one-tailed probability of the chi-squared distribution.

**Example:** `=CHISQ.DIST.RT(10, 5)` calculates the right-tailed probability of the chi-squared distribution.

### CHISQ.INV

Returns the cumulative beta probability density function.

**Example:** `=CHISQ.INV(0.5, 5)` calculates the inverse of the left-tailed probability of the chi-squared distribution.

### CHISQ.INV.RT

Returns the inverse of the one-tailed probability of the chi-squared distribution.

**Example:** `=CHISQ.INV.RT(0.5, 5)` calculates the inverse of the right-tailed probability of the chi-squared distribution.

### CHISQ.TEST

Returns the test for independence.

**Example:** `=CHISQ.TEST(A1:B2, C1:D2)` calculates the chi-squared test for independence between two ranges.

### CONFIDENCE.NORM

Returns the confidence interval for a population mean.

**Example:** `=CONFIDENCE.NORM(0.05, 1, 50)` calculates the confidence interval for a population mean, based on a sample standard deviation of 1, sample size of 50, and a 95% confidence level.

### CONFIDENCE.T

Returns the confidence interval for a population mean, using a Student's t distribution.

**Example:** `=CONFIDENCE.T(0.05, 1, 50)` calculates the confidence interval for a population mean, based on a sample standard deviation of 1, sample size of 50, and a 95% confidence level using the t distribution.

### CORREL

Returns the correlation coefficient between two data sets.

**Example:** `=CORREL(A1:A10, B1:B10)` calculates the correlation coefficient between the datasets in A1:A10 and B1:B10.

### COUNT

Counts how many numbers are in the list of arguments.

**Example:** `=COUNT(1, 2, "apple", TRUE)` counts the number of numeric values in the list, resulting in 2.

### COUNTA

Counts how many values are in the list of arguments.

**Example:** `=COUNTA(1, 2, "apple", TRUE)` counts all values, including numbers, text, and logical values, resulting in 4.

### COUNTBLANK

Counts the number of blank cells within a range.

**Example:** `=COUNTBLANK(A1:A10)` counts the number of blank cells in the range A1:A10.

### COUNTIF

Counts the number of cells within a range that meet the given criteria.

**Example:** `=COUNTIF(A1:A10, ">5")` counts the number of cells in the range A1:A10 that contain numbers greater than 5.

### COUNTIFS

Counts the number of cells within a range that meet multiple criteria.

**Example:** `=COUNTIFS(A1:A10, ">5", B1:B10, "<10")` counts the number of cells in range A1:A10 that are greater than 5 with corresponding cells in range B1:B10 less than 10.

### COVARIANCE.P

Returns covariance, the average of the products of paired deviations.

**Example:** `=COVARIANCE.P(A1:A10, B1:B10)` calculates the population covariance between two data sets.

### COVARIANCE.S

Returns the sample covariance, the average of the products deviations for each data point pair in two data sets.

**Example:** `=COVARIANCE.S(A1:A10, B1:B10)` calculates the sample covariance between two data sets.

### DEVSQ

Returns the sum of squares of deviations.

**Example:** `=DEVSQ(1, 2, 3, 4, 5)` calculates the sum of the squares of deviations from the mean for the numbers 1 through 5.

### EXPON.DIST

Returns the exponential distribution.

**Example:** `=EXPON.DIST(1, 0.5, TRUE)` calculates the cumulative exponential distribution function at x=1 with λ=0.5.

### F.DIST

Returns the F probability distribution.

**Example:** `=F.DIST(15.35, 6, 4, TRUE)` calculates the cumulative F distribution for the value 15.35 with 6 and 4 degrees of freedom.

### F.DIST.RT

Returns the F probability distribution.

**Example:** `=F.DIST.RT(15.35, 6, 4)` calculates the right-tailed F distribution for the value 15.35 with 6 and 4 degrees of freedom.

### F.INV

Returns the inverse of the F probability distribution.

**Example:** `=F.INV(0.95, 6, 4)` calculates the inverse of the F distribution for the 95th percentile with 6 and 4 degrees of freedom.

### F.INV.RT

Returns the inverse of the F probability distribution.

**Example:** `=F.INV.RT(0.05, 6, 4)` calculates the inverse of the right-tailed F distribution for the 5th percentile with 6 and 4 degrees of freedom.

### F.TEST

Returns the result of an F-test.

**Example:** `=F.TEST(A1:A10, B1:B10)` calculates the result of an F-test for two arrays of data, indicating whether their variances are significantly different.

### FISHER

Returns the Fisher transformation.

**Example:** `=FISHER(0.75)` calculates the Fisher transformation at the value 0.75.

### FISHERINV

Returns the inverse of the Fisher transformation.

**Example:** `=FISHERINV(0.972955)` calculates the inverse Fisher transformation for the value 0.972955.

This covers the statistical functions listed in your query up to FISHERINV, providing examples for each to illustrate their usage.

### FORECAST

Returns a value along a linear trend.

**Example:** `=FORECAST(30, A2:A10, B2:B10)` predicts a future point on a linear trend line fitted to the datasets in A2:A10 and B2:B10.

### FORECAST.ETS

Returns a future value based on existing (historical) values using the Exponential Smoothing algorithm.

**Example:** `=FORECAST.ETS(A11, A2:A10, B2:B10)` forecasts a value using the ETS algorithm based on historical data in A2:A10 and time in B2:B10.

### FORECAST.ETS.CONFINT

Returns a confidence interval for the forecast value at the specified target date.

**Example:** `=FORECAST.ETS.CONFINT(A11, A2:A10, B2:B10, 0.95)` returns the 95% confidence interval for the forecasted value at A11.

### FORECAST.ETS.SEASONALITY

Returns the length of the repetitive pattern Excel detects for the specified time series.

**Example:** `=FORECAST.ETS.SEASONALITY(A2:A10, B2:B10)` identifies the seasonal pattern length in the data series.

### FORECAST.ETS.STAT

Returns a statistical value as a result of time series forecasting.

**Example:** `=FORECAST.ETS.STAT(A2:A10, B2:B10, "statistic_type")` retrieves specific statistical values from the ETS forecast, where "statistic_type" specifies the statistic to return.

### FORECAST.LINEAR

Returns a future value based on existing values.

**Example:** `=FORECAST.LINEAR(30, A2:A10, B2:B10)` predicts a future point on a linear trend line fitted to the datasets in A2:A10 and B2:B10.

### FREQUENCY

Returns a frequency distribution as a vertical array.

**Example:** `=FREQUENCY(A2:A10, B2:B5)` returns a frequency distribution of the data in A2:A10 for the bins specified in B2:B5.

### GAMMA

Returns the Gamma function value.

**Example:** `=GAMMA(4)` calculates the value of the Gamma function Γ(4).

### GAMMA.DIST

Returns the gamma distribution.

**Example:** `=GAMMA.DIST(2.5, 3, 2, TRUE)` calculates the cumulative gamma distribution for x=2.5, α=3, and β=2.

### GAMMA.INV

Returns the inverse of the gamma cumulative distribution.

**Example:** `=GAMMA.INV(0.5, 3, 2)` calculates the inverse of the cumulative gamma distribution for a probability of 0.5, α=3, and β=2.

### GAMMALN

Returns the natural logarithm of the gamma function, Γ(x).

**Example:** `=GAMMALN(4)` calculates the natural logarithm of the Gamma function Γ(4).

### GAMMALN.PRECISE

Returns the natural logarithm of the gamma function, Γ(x).

**Example:** `=GAMMALN.PRECISE(4)` calculates the precise natural logarithm of the Gamma function Γ(4).

### GAUSS

Returns 0.5 less than the standard normal cumulative distribution.

**Example:** `=GAUSS(2)` calculates the probability that a random observation from a standard normal distribution will fall between the mean and z standard deviations from the mean.

### GEOMEAN

Returns the geometric mean.

**Example:** `=GEOMEAN(1, 2, 3, 4, 5)` calculates the geometric mean of the numbers 1, 2, 3, 4, and 5.

### GROWTH

Returns values along an exponential trend.

**Example:** `=GROWTH(B2:B10, A2:A10)` predicts values along an exponential trend fitted to the data in B2:B10.

### HARMEAN

Returns the harmonic mean.

**Example:** `=HARMEAN(1, 2, 3)` calculates the harmonic mean of the numbers 1, 2, and 3.

This continues the explanation and examples for the statistical functions in your query, covering from FORECAST to HARMEAN.

### HYPGEOM.DIST

Returns the hypergeometric distribution.

**Example:** `=HYPGEOM.DIST(1, 6, 3, 8, FALSE)` calculates the probability of drawing 1 success in a sample of 6 from a population of 8 with 3 successes.

### INTERCEPT

Returns the intercept of the linear regression line.

**Example:** `=INTERCEPT(B2:B10, A2:A10)` calculates the point where the linear regression line intersects the Y-axis based on data points in B2:B10 and A2:A10.

### KURT

Returns the kurtosis of a data set.

**Example:** `=KURT(A2:A10)` calculates the kurtosis of the data set in A2:A10, indicating how peaked the distribution is.

### LARGE

Returns the k-th largest value in a data set.

**Example:** `=LARGE(A2:A10, 3)` finds the third largest number in the range A2:A10.

### LINEST

Returns the parameters of a linear trend.

**Example:** `=LINEST(B2:B10, A2:A10)` calculates the slope and intercept of the linear regression line for the datasets.

### LOGEST

Returns the parameters of an exponential trend.

**Example:** `=LOGEST(B2:B10, A2:A10)` calculates the parameters of an exponential trend for the data sets.

### LOGNORM.DIST

Returns the cumulative lognormal distribution.

**Example:** `=LOGNORM.DIST(4, 3.5, 1.2, TRUE)` calculates the cumulative lognormal distribution for x=4, with a mean of 3.5 and standard deviation of 1.2.

### LOGNORM.INV

Returns the inverse of the lognormal cumulative distribution.

**Example:** `=LOGNORM.INV(0.75, 3.5, 1.2)` calculates the value x such that the cumulative lognormal distribution with mean 3.5 and standard deviation 1.2 is 0.75.

### MAX

Returns the maximum value in a list of arguments.

**Example:** `=MAX(A2:A10)` finds the highest number in the range A2:A10.

### MAXA

Returns the maximum value in a list of arguments, including numbers, text, and logical values.

**Example:** `=MAXA(A2:A10)` calculates the maximum value in A2:A10, treating TRUE as 1, FALSE as 0, and text as 0.

### MAXIFS

Returns the maximum value among cells specified by a given set of conditions or criteria.

**Example:** `=MAXIFS(A2:A10, B2:B10, ">10")` finds the maximum value in A2:A10 for which the corresponding value in B2:B10 is greater than 10.

### MEDIAN

Returns the median of the given numbers.

**Example:** `=MEDIAN(A2:A10)` calculates the median value in the data set A2:A10.

### MIN

Returns the minimum value in a list of arguments.

**Example:** `=MIN(A2:A10)` finds the smallest number in the range A2:A10.

### MINA

Returns the smallest value in a list of arguments, including numbers, text, and logical values.

**Example:** `=MINA(A2:A10)` calculates the minimum value in A2:A10, treating TRUE as 1, FALSE as 0, and text as 0.

### MINIFS

Returns the minimum value among cells specified by a given set of conditions or criteria.

**Example:** `=MINIFS(A2:A10, B2:B10, ">10")` finds the minimum value in A2:A10 for which the corresponding value in B2:B10 is greater than 10.

### MODE.MULT

Returns a vertical array of the most frequently occurring, or repetitive values in an array or range of data.

**Example:** `=MODE.MULT(A2:A10)` finds all the modes in the range A2:A10 and returns them in a vertical array.

### MODE.SNGL

Returns the most common value in a data set.

**Example:** `=MODE.SNGL(A2:A10)` identifies the most frequently occurring number in the range A2:A10.

### NEGBINOM.DIST

Returns the negative binomial distribution.

**Example:** `=NEGBINOM.DIST(10, 5, 0.5, FALSE)` calculates the probability of 10 failures before the 5th success with a success probability of 0.5.

### NORM.DIST

Returns the normal cumulative distribution.

**Example:** `=NORM.DIST(4, 2, 1, TRUE)` calculates the cumulative distribution function for a normally distributed variable with a mean of 2 and standard deviation of 1 at the value of 4.

### NORM.INV

Returns the inverse of the normal cumulative distribution.

**Example:** `=NORM.INV(0.8, 2, 1)` finds the value x such that the cumulative normal distribution with a mean of 2 and standard deviation of 1 is 0.8.

### NORM.S.DIST

Returns the standard normal cumulative distribution.

**Example:** `=NORM.S.DIST(1.5, TRUE)` calculates the cumulative distribution function for a standard normal variable (mean = 0, standard deviation = 1) at the value of 1.5.

### NORM.S.INV

Returns the inverse of the standard normal cumulative distribution.

**Example:** `=NORM.S.INV(0.9)` finds the value x such that the cumulative standard normal distribution is 0.9.

### PEARSON

Returns the Pearson product moment correlation coefficient.

**Example:** `=PEARSON(A2:A10, B2:B10)` calculates the Pearson correlation coefficient between two data sets A2:A10 and B2:B10.

### PERCENTILE.EXC

Returns the k-th percentile of values in a range, where k is in the range 0..1, exclusive.

**Example:** `=PERCENTILE.EXC(A2:A10, 0.3)` finds the 30th percentile of the data set A2:A10, excluding 0 and 1.

### PERCENTILE.INC

Returns the k-th percentile of values in a range.

**Example:** `=PERCENTILE.INC(A2:A10, 0.5)` calculates the median (50th percentile) of the data set A2:A10.

### PERCENTRANK.EXC

Returns the rank of a value in a data set as a percentage (0..1, exclusive) of the data set.

**Example:** `=PERCENTRANK.EXC(A2:A10, 5)` finds the percentile rank of the value 5 in the data set A2:A10, excluding 0 and 1.

### PERCENTRANK.INC

Returns the percentage rank of a value in a data set.

**Example:** `=PERCENTRANK.INC(A2:A10, 5)` calculates the percentile rank of the value 5 in the data set A2:A10.

### PERMUT

Returns the number of permutations for a given number of objects.

**Example:** `=PERMUT(10, 3)` calculates the number of ways to arrange 3 items out of 10.

### PERMUTATIONA

Returns the number of permutations for a given number of objects (with repetitions) that can be selected from the total objects.

**Example:** `=PERMUTATIONA(10, 3)` calculates the number of ways to arrange 3 items out of 10 with repetition.

### PHI

Returns the value of the density function for a standard normal distribution.

**Example:** `=PHI(1)` calculates the probability density function of the standard normal distribution for the value 1.

### POISSON.DIST

Returns the Poisson distribution.

**Example:** `=POISSON.DIST(5, 3, FALSE)` calculates the probability of exactly 5 occurrences when the average number of occurrences is 3.

### PROB

Returns the probability that values in a range are between two limits.

**Example:** `=PROB(A2:A10, B2:B10, 3, 5)` calculates the probability that values in A2:A10 are between 3 and 5, given their probabilities in B2:B10.

### QUARTILE.EXC

Returns the quartile of the data set, based on percentile values from 0..1, exclusive.

**Example:** `=QUARTILE.EXC(A2:A10, 2)` finds the median (50th percentile) of the data set A2:A10, excluding 0 and 1.

### QUARTILE.INC

Returns the quartile of a data set.

**Example:** `=QUARTILE.INC(A2:A10, 3)` calculates the third quartile (75th percentile) of the data set A2:A10.

### RANK.AVG

Returns the rank of a number in a list of numbers. If there are multiple occurrences of the same number, the average rank is returned.

**Example:** `=RANK.AVG(4, A1:A10)` calculates the rank of the number 4 within the range A1:A10, averaging if there are ties.

### RANK.EQ

Returns the rank of a number in a list of numbers. If there are multiple occurrences of the same number, the position of the first occurrence is returned.

**Example:** `=RANK.EQ(4, A1:A10)` calculates the rank of the number 4 within the range A1:A10, without averaging for ties.

### RSQ

Returns the square of the Pearson product moment correlation coefficient.

**Example:** `=RSQ(A1:A10, B1:B10)` calculates the R-squared value, a measure of how well the regression line approximates the real data points, for two sets of data.

### SKEW

Returns the skewness of a distribution.

**Example:** `=SKEW(A1:A10)` calculates the skewness of the distribution within the range A1:A10, indicating its asymmetry.

### SKEW.P

Returns the skewness of a distribution based on a population: a characterization of the degree of asymmetry of a distribution around its mean.

**Example:** `=SKEW.P(A1:A10)` calculates the population skewness of the distribution within the range A1:A10.

### SLOPE

Returns the slope of the linear regression line.

**Example:** `=SLOPE(B1:B10, A1:A10)` calculates the slope of the line resulting from linear regression of the data sets in A1:A10 and B1:B10.

### SMALL

Returns the k-th smallest value in a data set.

**Example:** `=SMALL(A1:A10, 2)` finds the second smallest number in the range A1:A10.

### STANDARDIZE

Returns a normalized value.

**Example:** `=STANDARDIZE(4, 2, 0.5)` normalizes the value 4 based on a mean of 2 and a standard deviation of 0.5.

### STDEV.P

Calculates standard deviation based on the entire population.

**Example:** `=STDEV.P(A1:A10)` calculates the standard deviation of the values in the range A1:A10 as if they represent an entire population.

### STDEV.S

Estimates standard deviation based on a sample.

**Example:** `=STDEV.S(A1:A10)` calculates the standard deviation of the values in the range A1:A10 as if they are a sample of a larger population.

### STDEVA

Estimates standard deviation based on a sample, including numbers, text, and logical values.

**Example:** `=STDEVA(A1:A10)` calculates the standard deviation of the values in A1:A10, treating text and logicals as well.

### STDEVPA

Calculates standard deviation based on the entire population, including numbers, text, and logical values.

**Example:** `=STDEVPA(A1:A10)` calculates the standard deviation of A1:A10, treating all data types.

### STEYX

Returns the standard error of the predicted y-value for each x in the regression.

**Example:** `=STEYX(B1:B10, A1:A10)` calculates the standard error of the estimate for a predicted y-value from each x in A1:A10 based on the regression line calculated from A1:A10 and B1:B10.

### T.DIST

Returns the Percentage Points (probability) for the Student t-distribution.

**Example:** `=T.DIST(2, 10, TRUE)` calculates the left-tailed probability of the t-distribution with a t-value of 2 and 10 degrees of freedom.

### T.DIST.2T

Returns the Percentage Points (probability) for the Student t-distribution.

**Example:** `=T.DIST.2T(2, 10)` calculates the two-tailed probability of the t-distribution with a t-value of 2 and 10 degrees of freedom.

### T.DIST.RT

Returns the Student's t-distribution.

**Example:** `=T.DIST.RT(2, 10)` calculates the right-tailed probability of the t-distribution with a t-value of 2 and 10 degrees of freedom.

### T.INV

Returns the t-value of the Student's t-distribution as a function of the probability and the degrees of freedom.

**Example:** `=T.INV(0.05, 10)` finds the t-value for the left-tailed inverse of the t-distribution with a significance level of 0.05 and 10 degrees of freedom.

### T.INV.2T

Returns the inverse of the Student's t-distribution for a given two-tailed probability and degrees of freedom.

**Example:** `=T.INV.2T(0.05, 10)` finds the t-value for the two-tailed inverse of the t-distribution with a significance level of 0.05 and 10 degrees of freedom.

### T.TEST

Returns the probability associated with a Student's t-test.

**Example:** `=T.TEST(A1:A10, B1:B10, 2, 1)` conducts a two-tailed t-test for the datasets in A1:A10 and B1:B10, assuming equal variances.

### TREND

Returns values along a linear trend.

**Example:** `=TREND(B1:B10, A1:A10, C1:C10)` predicts y-values based on a linear trend derived from the x-values in A1:A10 and known y-values in B1:B10, for new x-values in C1:C10.

### TRIMMEAN

Returns the mean of the interior of a data set.

**Example:** `=TRIMMEAN(A1:A10, 0.1)` calculates the mean of the range A1:A10, trimming 10% of the data points from both ends of the dataset.

### VAR.P

Calculates variance based on the entire population.

**Example:** `=VAR.P(A1:A10)` calculates the variance of the population represented by the data in A1:A10.

### VAR.S

Estimates variance based on a sample.

**Example:** `=VAR.S(A1:A10)` estimates the variance of a sample represented by the data in A1:A10.

### VARA

Estimates variance based on a sample, including numbers, text, and logical values.

**Example:** `=VARA(A1:A10)` calculates the variance of a sample represented by the data in A1:A10, including text and logical values.

### VARPA

Calculates variance based on the entire population, including numbers, text, and logical values.

**Example:** `=VARPA(A1:A10)` calculates the variance of the entire population represented by the data in A1:A10, including text and logical values.

### WEIBULL.DIST

Returns the Weibull distribution.

**Example:** `=WEIBULL.DIST(1.5, 1, 2, TRUE)` calculates the cumulative Weibull distribution function with shape parameter 1, scale parameter 2, and evaluates it at 1.5.

### Z.TEST

Returns the one-tailed probability-value of a z-test.

**Example:** `=Z.TEST(A1:A10, 0, 1)` calculates the one-tailed probability of the z-test for the dataset A1:A10, assuming a mean of 0 and a standard deviation of 1.


## Text functions

### ASC

Changes full-width (double-byte) English letters or katakana within a character string to half-width (single-byte) characters.

**Example:** `=ASC("ｈｅｌｌｏ")` returns "hello".

### ARRAYTOTEXT

Returns an array of text values from any specified range.

**Example:** `=ARRAYTOTEXT(A1:B2)` converts the range A1:B2 into a single text string.

### BAHTTEXT

Converts a number to text, using the ß (baht) currency format.

**Example:** `=BAHTTEXT(123)` returns the text representation of 123 in the Thai Baht currency format.

### CHAR

Returns the character specified by the code number.

**Example:** `=CHAR(65)` returns "A".

### CLEAN

Removes all nonprintable characters from text.

**Example:** `=CLEAN(CHAR(7)&"Hello")` returns "Hello".

### CODE

Returns a numeric code for the first character in a text string.

**Example:** `=CODE("A")` returns 65.

### CONCAT

Combines the text from multiple ranges and/or strings, but it doesn't provide the delimiter or IgnoreEmpty arguments.

**Example:** `=CONCAT("Hello ", "world!")` returns "Hello world!".

### CONCATENATE

Joins several text items into one text item.

**Example:** `=CONCATENATE("Hello", " ", "world!")` returns "Hello world!".

### DBCS

Changes half-width (single-byte) English letters or katakana within a character string to full-width (double-byte) characters.

**Example:** `=DBCS("hello")` might return a full-width representation of "hello".

### DOLLAR

Converts a number to text, using the $ (dollar) currency format.

**Example:** `=DOLLAR(1234.567)` returns "$1,234.57".

### EXACT

Checks to see if two text values are identical.

**Example:** `=EXACT("hello", "Hello")` returns FALSE.

### FIND, FINDB

Finds one text value within another (case-sensitive).

**Example:** `=FIND("M", "Miriam McGovern")` returns 6.

### FIXED

Formats a number as text with a fixed number of decimals.

**Example:** `=FIXED(123.456, 2)` returns "123.46".

### LEFT, LEFTB

Returns the leftmost characters from a text value.

**Example:** `=LEFT("Hello World", 5)` returns "Hello".

### LEN, LENB

Returns the number of characters in a text string.

**Example:** `=LEN("Hello")` returns 5.

### LOWER

Converts text to lowercase.

**Example:** `=LOWER("HELLO WORLD")` returns "hello world".

### MID, MIDB

Returns a specific number of characters from a text string starting at the position you specify.

**Example:** `=MID("Hello World", 7, 5)` returns "World".

### NUMBERVALUE

Converts text to number in a locale-independent manner.

**Example:** `=NUMBERVALUE("1,234.56", ".", ",")` returns 1234.56.

### PHONETIC

Extracts the phonetic (furigana) characters from a text string.

**Example:** Assuming A1 contains Japanese text with furigana, `=PHONETIC(A1)` extracts the furigana.

### PROPER

Capitalizes the first letter in each word of a text value.

**Example:** `=PROPER("hello world")` returns "Hello World".

### REPLACE, REPLACEB

Replaces characters within text.

**Example:** `=REPLACE("XYZ123", 4, 3, "456")` returns "XYZ456".

### REPT

Repeats text a given number of times.

**Example:** `=REPT("Hello", 3)` returns "HelloHelloHello".

### RIGHT, RIGHTB

Returns the rightmost characters from a text value.

**Example:** `=RIGHT("Hello World", 5)` returns "World".

### SEARCH, SEARCHB

Finds one text value within another (not case-sensitive).

**Example:** `=SEARCH("m", "Miriam McGovern")` returns 6.

### SUBSTITUTE

Substitutes new text for old text in a text string.

**Example:** `=SUBSTITUTE("Hello World", "World", "There")` returns "Hello There".

### T

Converts its arguments to text.

**Example:** `=T(123)` returns "123".

### TEXT

Formats a number and converts it to text.

**Example:** `=TEXT(1234.567, "$#,##0.00")` returns "$1,234.57".

### TEXTAFTER

Returns text that occurs after a given character or string.

**Example:** `=TEXTAFTER("John Doe - CEO", " - ")` returns "CEO".

### TEXTBEFORE

Returns text that occurs before a given character or string.

**Example:** `=TEXTBEFORE("John Doe - CEO", " - ")` returns "John Doe".

### TEXTJOIN

Combines the text from multiple ranges and/or strings.

**Example:** `=TEXTJOIN(", ", TRUE, "John", "Paul", "George", "Ringo")` returns "John, Paul, George, Ringo".

### TEXTSPLIT

Splits text strings by using column and row delimiters.

**Example:** `=TEXTSPLIT("John,Paul,George,Ringo", ",", TRUE)` might return an array of the four Beatles' names.

### TRIM

Removes spaces from text.

**Example:** `=TRIM(" Hello  World ")` returns "Hello World".

### UNICHAR

Returns the Unicode character that is referenced by the given numeric value.

**Example:** `=UNICHAR(9731)` returns the snowflake symbol (❄).

### UNICODE

Returns the number (code point) corresponding to the first character of the text.

**Example:** `=UNICODE("A")` returns 65.

### UPPER

Converts text to uppercase.

**Example:** `=UPPER("hello world")` returns "HELLO WORLD".

### VALUE

Converts a text argument to a number.

**Example:** `=VALUE("$1,234.56")` returns 1234.56.

### VALUETOTEXT

Returns text from any specified value.

**Example:** `=VALUETOTEXT(123)` returns "123".


## User defined functions
### CALL

Calls a procedure in a dynamic link library or code resource.

**Example:** `=CALL("User32", "MessageBeep", "J", 16)` might be used to call a Windows function that causes the system to make a warning sound.

### EUROCONVERT

Converts a number to euros, converts a number from euros to a euro member currency, or converts a number from one euro member currency to another by using the euro as an intermediary (triangulation).

**Example:** `=EUROCONVERT(100, "USD", "EUR")` converts 100 US dollars to euros.

### REGISTER.ID

Returns the register ID of the specified dynamic link library (DLL) or code resource that has been previously registered.

**Example:** `=REGISTER.ID("mydll.dll", "MyFunction")` returns the register ID for "MyFunction" in "mydll.dll".


## Web functions

Web functions are not available in Excel for the web.

### ENCODEURL

Returns a URL-encoded string.

**Example:** `=ENCODEURL("http://www.example.com?name=John Doe")` encodes the URL to make it valid for web requests.

### FILTERXML

Returns specific data from the XML content by using the specified XPath.

**Example:** `=FILTERXML("<items><item>1</item><item>2</item></items>", "//item")` returns 1 and 2 from the XML string.

### WEBSERVICE

Returns data from a web service.

**Example:** `=WEBSERVICE("http://api.example.com/data")` retrieves data from the specified web service URL.
