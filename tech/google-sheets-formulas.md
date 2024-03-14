This comprehensive cheat sheet encompasses a wide range of functions available in [Google Sheets](https://support.google.com/docs/table/25273?hl=en), categorized into [**Array**](#array), [**Database**](#database), [**Date**](#date), [**Engineering**](#engineering), [**Filter**](#filter), [**Financial**](#financial), [**Google**](#google), [**Info**](#info), [**Logical**](#logical), [**Lookup**](#lookup), [**Math**](#math), [**Operator**](#operator), [**Parser**](#parser), [**Statistical**](#statistical), [**Text**](#text), and [**Web**](#web). It provides concise descriptions and syntax for each function, making it an invaluable resource for users looking to perform various operations from simple calculations to complex data manipulation and web-based imports. Whether you're formatting data, analyzing statistics, or importing information from external sources, this cheat sheet is designed to enhance productivity and streamline your spreadsheet tasks.


## Array

### ARRAY_CONSTRAIN
```
ARRAY_CONSTRAIN(input_range, num_rows, num_cols)
```
Constrains an array result to a specified size.

### BYCOL
```
BYCOL(array_or_range, LAMBDA)
```
Groups an array by columns by application of a LAMBDA function to each column.

### BYROW
```
BYROW(array_or_range, LAMBDA)
```
Groups an array by rows by application of a LAMBDA function to each row.

### CHOOSECOLS
```
CHOOSECOLS(array, col_num1, [col_num2]) 
```
Creates a new array from the selected columns in the existing range.

### CHOOSEROWS
```
CHOOSEROWS(array, row_num1, [row_num2])
```
Creates a new array from the selected rows in the existing range.

### FLATTEN
```
FLATTEN(range1,[range2,...])
```
Flattens all the values from one or more ranges into a single column.

### FREQUENCY
```
FREQUENCY(data, classes)
```
Calculates the frequency distribution of a one-column array into specified classes.

### GROWTH
```
GROWTH(known_data_y, [known_data_x], [new_data_x], [b])
```
Given partial data about an exponential growth trend, fits an ideal exponential growth trend and/or predicts further values.

### HSTACK
```
HSTACK(range1; [range2, …])
```
Appends ranges horizontally and in sequence to return a larger array.

### LINEST
```
LINEST(known_data_y, [known_data_x], [calculate_b], [verbose])
```
Given partial data about a linear trend, calculates various parameters about the ideal linear trend using the least-squares method.

### LOGEST
```
LOGEST(known_data_y, [known_data_x], [b], [verbose])
```
Given partial data about an exponential growth curve, calculates various parameters about the best fit ideal exponential growth curve.

### MAKEARRAY
```
MAKEARRAY(rows, columns, LAMBDA)
```
Returns an array of specified dimensions with values calculated by application of a LAMBDA function.

### MAP
```
MAP(array1, [array2, ...], LAMBDA)
```
Maps each value in the given arrays to a new value by application of a LAMBDA function to each value.

### MDETERM
```
MDETERM(square_matrix)
```
Returns the matrix determinant of a square matrix specified as an array or range.

### MINVERSE
```
MINVERSE(square_matrix)
```
Returns the multiplicative inverse of a square matrix specified as an array or range.

### MMULT
```
MMULT(matrix1, matrix2)
```
Calculates the matrix product of two matrices specified as arrays or ranges.

### REDUCE
```
REDUCE(initial_value, array_or_range, LAMBDA)
```
Reduces an array to an accumulated result by application of a LAMBDA function to each value.

### SCAN
```
SCAN(initial_value, array_or_range, LAMBDA)
```
Scans an array and produces intermediate values by application of a LAMBDA function to each value. Returns an array of the intermediate values obtained at each step.

### SUMPRODUCT
```
SUMPRODUCT(array1, [array2, ...])
```
Calculates the sum of the products of corresponding entries in two equal-sized arrays or ranges.

### SUMX2MY2
```
SUMX2MY2(array_x, array_y)
```
Calculates the sum of the differences of the squares of values in two arrays.

### SUMX2PY2
```
SUMX2PY2(array_x, array_y)
```
Calculates the sum of the sums of the squares of values in two arrays.

### SUMXMY2
```
SUMXMY2(array_x, array_y)
```
Calculates the sum of the squares of differences of values in two arrays.

### TOCOL
```
TOCOL(array_or_range, [ignore], [scan_by_column])
```
Transforms an array or range of cells into a single column.

### TOROW
```
TOROW(array_or_range, [ignore], [scan_by_column])
```
Transforms an array or range of cells into a single row.

### TRANSPOSE
```
TRANSPOSE(array_or_range)
```
Transposes the rows and columns of an array or range of cells.

### TREND
```
TREND(known_data_y, [known_data_x], [new_data_x], [b])
```
Given partial data about a linear trend, fits an ideal linear trend using the least squares method and/or predicts further values.

### VSTACK
```
VSTACK(range1; [range2, …])
```


Appends ranges vertically and in sequence to return a larger array.

### WRAPCOLS
```
WRAPCOLS(range, wrap_count, [pad_with])
```
Wraps the provided row or column of cells by columns after a specified number of elements to form a new array.

### WRAPROWS
```
WRAPROWS(range, wrap_count, [pad_with])
```
Wraps the provided row or column of cells by rows after a specified number of elements to form a new array.


Here's how the provided table part would be formatted in markdown:

## Database

### DAVERAGE
```
DAVERAGE(database, field, criteria)
```
Returns the average of a set of values selected from a database table-like array or range using a SQL-like query.

### DCOUNT
```
DCOUNT(database, field, criteria)
```
Counts numeric values selected from a database table-like array or range using a SQL-like query.

### DCOUNTA
```
DCOUNTA(database, field, criteria)
```
Counts values, including text, selected from a database table-like array or range using a SQL-like query.

### DGET
```
DGET(database, field, criteria)
```
Returns a single value from a database table-like array or range using a SQL-like query.

### DMAX
```
DMAX(database, field, criteria)
```
Returns the maximum value selected from a database table-like array or range using a SQL-like query.

### DMIN
```
DMIN(database, field, criteria)
```
Returns the minimum value selected from a database table-like array or range using a SQL-like query.

### DPRODUCT
```
DPRODUCT(database, field, criteria)
```
Returns the product of values selected from a database table-like array or range using a SQL-like query.

### DSTDEV
```
DSTDEV(database, field, criteria)
```
Returns the standard deviation of a population sample selected from a database table-like array or range using a SQL-like query.

### DSTDEVP
```
DSTDEVP(database, field, criteria)
```
Returns the standard deviation of an entire population selected from a database table-like array or range using a SQL-like query.

### DSUM
```
DSUM(database, field, criteria)
```
Returns the sum of values selected from a database table-like array or range using a SQL-like query.

### DVAR
```
DVAR(database, field, criteria)
```
Returns the variance of a population sample selected from a database table-like array or range using a SQL-like query.

### DVARP
```
DVARP(database, field, criteria)
```
Returns the variance of an entire population selected from a database table-like array or range using a SQL-like query.



For this part of the table related to date functions, here's how it would be translated into markdown format:

## Date

### DATE
```
DATE(year, month, day)
```
Converts a provided year, month, and day into a date.

### DATEDIF
```
DATEDIF(start_date, end_date, unit)
```
Calculates the number of days, months, or years between two dates.

### DATEVALUE
```
DATEVALUE(date_string)
```
Converts a provided date string in a known format to a date value.

### DAY
```
DAY(date)
```
Returns the day of the month that a specific date falls on, in numeric format.

### DAYS
```
DAYS(end_date, start_date)
```
Returns the number of days between two dates.

### DAYS360
```
DAYS360(start_date, end_date, [method])
```
Returns the difference between two days based on the 360 day year used in some financial interest calculations.

### EDATE
```
EDATE(start_date, months)
```
Returns a date a specified number of months before or after another date.

### EOMONTH
```
EOMONTH(start_date, months)
```
Returns a date representing the last day of a month which falls a specified number of months before or after another date.

### EPOCHTODATE
```
EPOCHTODATE(timestamp, [unit])
```
Converts a Unix epoch timestamp in seconds, milliseconds, or microseconds to a datetime in UTC.

### HOUR
```
HOUR(time)
```
Returns the hour component of a specific time, in numeric format.

### ISOWEEKNUM
```
ISOWEEKNUM(date)
```
Returns the number of the ISO week of the year where the provided date falls.

### MINUTE
```
MINUTE(time)
```
Returns the minute component of a specific time, in numeric format.

### MONTH
```
MONTH(date)
```
Returns the month of the year a specific date falls in, in numeric format.

### NETWORKDAYS
```
NETWORKDAYS(start_date, end_date, [holidays])
```
Returns the number of net working days between two provided days.

### NETWORKDAYS.INTL
```
NETWORKDAYS.INTL(start_date, end_date, [weekend], [holidays])
```
Returns the number of net working days between two provided days excluding specified weekend days and holidays.

### NOW
```
NOW()
```
Returns the current date and time as a date value.

### SECOND
```
SECOND(time)
```
Returns the second component of a specific time, in numeric format.

### TIME
```
TIME(hour, minute, second)
```
Converts a provided hour, minute, and second into a time.

### TIMEVALUE
```
TIMEVALUE(time_string)
```
Returns the fraction of a 24-hour day the time represents.

### TODAY
```
TODAY()
```
Returns the current date as a date value.

### WEEKDAY
```
WEEKDAY(date, [type])
```
Returns a number representing the day of the week of the date provided.

### WEEKNUM
```
WEEKNUM(date, [type])
```
Returns a number representing the week of the year where the provided date falls.

### WORKDAY
```
WORKDAY(start_date, num_days, [holidays])
```
Calculates the end date after a specified number of working days.

### WORKDAY.INTL
```
WORKDAY.INTL(start_date, num_days, [weekend], [holidays])
```
Calculates the date after a specified number of workdays excluding specified weekend days and holidays.

### YEAR
```
YEAR(date)
```
Returns the year specified by a given date.

### YEARFRAC
```
YEARFRAC(start_date, end_date, [day_count_convention])
```
Returns the number of years, including fractional years, between two dates using a specified day count convention.


Here's how the provided table part related to engineering functions would be translated into markdown format:

## Engineering

### BIN2DEC
```
BIN2DEC(signed_binary_number)
```
Converts a signed binary number to decimal format.

### BIN2HEX
```
BIN2HEX(signed_binary_number, [significant_digits])
```
Converts a signed binary number to signed hexadecimal format.

### BIN2OCT
```
BIN2OCT(signed_binary_number, [significant_digits])
```
Converts a signed binary number to signed octal format.

### BITAND
```
BITAND(value1, value2)
```
Bitwise boolean AND of two numbers.

### BITLSHIFT
```
BITLSHIFT(value, shift_amount)
```
Shifts the bits of the input a certain number of places to the left.

### BITOR
```
BITOR(value1, value2)
```
Bitwise boolean OR of 2 numbers.

### BITRSHIFT
```
BITRSHIFT(value, shift_amount)
```
Shifts the bits of the input a certain number of places to the right.

### BITXOR
```
BITXOR(value1, value2)
```
Bitwise XOR (exclusive OR) of 2 numbers.

### COMPLEX
```
COMPLEX(real_part, imaginary_part, [suffix])
```
Creates a complex number given real and imaginary coefficients.

### DEC2BIN
```
DEC2BIN(decimal_number, [significant_digits])
```
Converts a decimal number to signed binary format.

### DEC2HEX
```
DEC2HEX(decimal_number, [significant_digits])
```
Converts a decimal number to signed hexadecimal format.

### DEC2OCT
```
DEC2OCT(decimal_number, [significant_digits])
```
Converts a decimal number to signed octal format.

### DELTA
```
DELTA(number1, [number2])
```
Compare two numeric values, returning 1 if they're equal.

### ERF
```
ERF(lower_bound, [upper_bound])
```
The ERF function returns the integral of the Gauss error function over an interval of values.

### ERF.PRECISE
```
ERF.PRECISE(lower_bound, [upper_bound])
```
See ERF for more details.

### GESTEP
```
GESTEP(value, [step])
```
Returns 1 if the rate is strictly greater than or equal to the provided step value or 0 otherwise.

### HEX2BIN
```
HEX2BIN(signed_hexadecimal_number, [significant_digits])
```
Converts a signed hexadecimal number to signed binary format.

### HEX2DEC
```
HEX2DEC(signed_hexadecimal_number)
```
Converts a signed hexadecimal number to decimal format.

### HEX2OCT
```
HEX2OCT(signed_hexadecimal_number, significant_digits)
```
Converts a signed hexadecimal number to signed octal format.

### IMABS
```
IMABS(number)
```
Returns absolute value of a complex number.

### IMAGINARY
```
IMAGINARY(complex_number)
```
Returns the imaginary coefficient of a complex number.

### IMARGUMENT
```
IMARGUMENT(number)
```
Returns the angle of the given complex number in radians.

### IMCONJUGATE
```
IMCONJUGATE(number)
```
Returns the complex conjugate of a number.

### IMCOS
```
IMCOS(number)
```
Returns the cosine of the given complex number.

### IMCOSH
```
IMCOSH(number)
```
Returns the hyperbolic cosine of the given complex number.

### IMCOT
```
IMCOT(number)
```
Returns the cotangent of the given complex number.

### IMCOTH
```
IMCOTH(number)
```
Returns the hyperbolic cotangent of the given complex number.

### IMCSC
```
IMCSC(number)
```
Returns the cosecant of the given complex number.

### IMCSCH
```
IMCSCH(number)
```
Returns the hyperbolic cosecant of the given complex number.

### IMDIV
```
IMDIV(dividend, divisor)
```
Returns one complex number divided by another.

### IMEXP
```
IMEXP(exponent)
```
Returns Euler's number, e, raised to a complex power.

### IMLOG
```
IMLOG(value, base)
```
Returns the logarithm of a complex number for a specified base.

### IMLOG10
```
IMLOG10(value)
```
Returns the logarithm of a complex number with base 10.

### IMLOG2
```
IMLOG2(value)
```
Returns the logarithm of a complex number with base 2.

### IMPRODUCT
```
IMPRODUCT(factor1, [factor2, ...])
```
Returns the result of multiplying a series of

 complex numbers together.

### IMREAL
```
IMREAL(complex_number)
```
Returns the real coefficient of a complex number.

### IMSEC
```
IMSEC(number)
```
Returns the secant of the given complex number.

### IMSECH
```
IMSECH(number)
```
Returns the hyperbolic secant of the given complex number.

### IMSIN
```
IMSIN(number)
```
Returns the sine of the given complex number.

### IMSINH
```
IMSINH(number)
```
Returns the hyperbolic sine of the given complex number.

### IMSUB
```
IMSUB(first_number, second_number)
```
Returns the difference between two complex numbers.

### IMSUM
```
IMSUM(value1, [value2, ...])
```
Returns the sum of a series of complex numbers.

### IMTAN
```
IMTAN(number)
```
Returns the tangent of the given complex number.

### IMTANH
```
IMTANH(number)
```
Returns the hyperbolic tangent of the given complex number.

### OCT2BIN
```
OCT2BIN(signed_octal_number, [significant_digits])
```
Converts a signed octal number to signed binary format.

### OCT2DEC
```
OCT2DEC(signed_octal_number)
```
Converts a signed octal number to decimal format.

### OCT2HEX
```
OCT2HEX(signed_octal_number, [significant_digits])
```
Converts a signed octal number to signed hexadecimal format.


Here's the markdown format for the provided table section related to filter functions:

## Filter

### FILTER
```
FILTER(range, condition1, [condition2])
```
Returns a filtered version of the source range, returning only rows or columns which meet the specified conditions.

### SORT
```
SORT(range, sort_column, is_ascending, [sort_column2], [is_ascending2])
```
Sorts the rows of a given array or range by the values in one or more columns.

### SORTN
```
SORTN(range, [n], [display_ties_mode], [sort_column1, is_ascending1], ...)
```
Returns the first n items in a data set after performing a sort.

### UNIQUE
```
UNIQUE(range)
```
Returns unique rows in the provided source range, discarding duplicates. Rows are returned in the order in which they first appear in the source range.


Here's the markdown format for the provided table section related to financial functions:

## Financial

### ACCRINT
```
ACCRINT(issue, first_payment, settlement, rate, redemption, frequency, [day_count_convention])
```
Calculates the accrued interest of a security that has periodic payments.

### ACCRINTM
```
ACCRINTM(issue, maturity, rate, [redemption], [day_count_convention])
```
Calculates the accrued interest of a security that pays interest at maturity.

### AMORLINC
```
AMORLINC(cost, purchase_date, first_period_end, salvage, period, rate, [basis])
```
Returns the depreciation for an accounting period, or the prorated depreciation if the asset was purchased in the middle of a period.

### COUPDAYBS
```
COUPDAYBS(settlement, maturity, frequency, [day_count_convention])
```
Calculates the number of days from the first coupon, or interest payment, until settlement.

### COUPDAYS
```
COUPDAYS(settlement, maturity, frequency, [day_count_convention])
```
Calculates the number of days in the coupon, or interest payment, period that contains the specified settlement date.

### COUPDAYSNC
```
COUPDAYSNC(settlement, maturity, frequency, [day_count_convention])
```
Calculates the number of days from the settlement date until the next coupon, or interest payment.

### COUPNCD
```
COUPNCD(settlement, maturity, frequency, [day_count_convention])
```
Calculates next coupon, or interest payment, date after the settlement date.

### COUPNUM
```
COUPNUM(settlement, maturity, frequency, [day_count_convention])
```
Calculates the number of coupons, or interest payments, between the settlement date and the maturity date of the investment.

### COUPPCD
```
COUPPCD(settlement, maturity, frequency, [day_count_convention])
```
Calculates last coupon, or interest payment, date before the settlement date.

### CUMIPMT
```
CUMIPMT(rate, number_of_periods, present_value, first_period, last_period, end_or_beginning)
```
Calculates the cumulative interest over a range of payment periods for an investment.

### CUMPRINC
```
CUMPRINC(rate, number_of_periods, present_value, first_period, last_period, end_or_beginning)
```
Calculates the cumulative principal paid over a range of payment periods for an investment.

### DB
```
DB(cost, salvage, life, period, [month])
```
Calculates the depreciation of an asset for a specified period using the arithmetic declining balance method.

### DDB
```
DDB(cost, salvage, life, period, [factor])
```
Calculates the depreciation of an asset for a specified period using the double-declining balance method.

### DISC
```
DISC(settlement, maturity, price, redemption, [day_count_convention])
```
Calculates the discount rate of a security based on price.

### DOLLARDE
```
DOLLARDE(fractional_price, unit)
```
Converts a price quotation given as a decimal fraction into a decimal value.

### DOLLARFR
```
DOLLARFR(decimal_price, unit)
```
Converts a price quotation given as a decimal value into a decimal fraction.

### DURATION
```
DURATION(settlement, maturity, rate, yield, frequency, [day_count_convention])
```
Calculates the number of compounding periods required for an investment to reach a target value.

### EFFECT
```
EFFECT(nominal_rate, periods_per_year)
```
Calculates the annual effective interest rate.

### FV
```
FV(rate, number_of_periods, payment_amount, [present_value], [end_or_beginning])
```
Calculates the future value of an annuity investment.

### FVSCHEDULE
```
FVSCHEDULE(principal, rate_schedule)
```
Calculates the future value of some principal based on a specified series of interest rates.

### INTRATE
```
INTRATE(buy_date, sell_date, buy_price, sell_price, [day_count_convention])
```
Calculates the effective interest rate generated by an investment.

### IPMT
```
IPMT(rate, period, number_of_periods, present_value, [future_value], [end_or_beginning])
```
Calculates the payment on interest for an investment.

### IRR
```
IRR(cashflow_amounts, [rate_guess])
```
Calculates the internal rate of return on an investment.

### ISPMT
```
ISPMT(rate, period, number_of_periods, present_value)
```
Calculates the interest paid during a particular period of an investment.

### MDURATION
```
MDURATION(set

tlement, maturity, rate, yield, frequency, [day_count_convention])
```
Calculates the modified Macaulay duration of a security.

### MIRR
```
MIRR(cashflow_amounts, financing_rate, reinvestment_return_rate)
```
Calculates the modified internal rate of return on an investment.

### NOMINAL
```
NOMINAL(effective_rate, periods_per_year)
```
Calculates the annual nominal interest rate.

### NPER
```
NPER(rate, payment_amount, present_value, [future_value], [end_or_beginning])
```
Calculates the number of payment periods for an investment.

### NPV
```
NPV(discount, cashflow1, [cashflow2, ...])
```
Calculates the net present value of an investment.

### PDURATION
```
PDURATION(rate, present_value, future_value)
```
Returns the number of periods for an investment to reach a specific value.

### PMT
```
PMT(rate, number_of_periods, present_value, [future_value], [end_or_beginning])
```
Calculates the periodic payment for an annuity investment.

### PPMT
```
PPMT(rate, period, number_of_periods, present_value, [future_value], [end_or_beginning])
```
Calculates the payment on the principal of an investment.

### PRICE
```
PRICE(settlement, maturity, rate, yield, redemption, frequency, [day_count_convention])
```
Calculates the price of a security paying periodic interest.

### PRICEDISC
```
PRICEDISC(settlement, maturity, discount, redemption, [day_count_convention])
```
Calculates the price of a discount security based on expected yield.

### PRICEMAT
```
PRICEMAT(settlement, maturity, issue, rate, yield, [day_count_convention])
```
Calculates the price of a security paying interest at maturity.

### PV
```
PV(rate, number_of_periods, payment_amount, [future_value], [end_or_beginning])
```
Calculates the present value of an annuity investment.

### RATE
```
RATE(number_of_periods, payment_per_period, present_value, [future_value], [end_or_beginning], [rate_guess])
```
Calculates the interest rate of an annuity investment.

### RECEIVED
```
RECEIVED(settlement, maturity, investment, discount, [day_count_convention])
```
Calculates the amount received at maturity for a fixed-income security.

### RRI
```
RRI(number_of_periods, present_value, future_value)
```
Returns the interest rate needed for an investment to reach a specific value.

### SLN
```
SLN(cost, salvage, life)
```
Calculates the straight-line depreciation of an asset.

### SYD
```
SYD(cost, salvage, life, period)
```
Calculates the sum of years digits depreciation of an asset.

### TBILLEQ
```
TBILLEQ(settlement, maturity, discount)
```
Calculates the equivalent annualized rate of return of a US Treasury Bill.

### TBILLPRICE
```
TBILLPRICE(settlement, maturity, discount)
```
Calculates the price of a US Treasury Bill based on discount rate.

### TBILLYIELD
```
TBILLYIELD(settlement, maturity, price)
```
Calculates the yield of a US Treasury Bill based on price.

### VDB
```
VDB(cost, salvage, life, start_period, end_period, [factor], [no_switch])
```
Returns the depreciation of an asset for a specified period.

### XIRR
```
XIRR(cashflow_amounts, cashflow_dates, [rate_guess])
```
Calculates the internal rate of return for a series of cash flows occurring at irregular intervals.

### XNPV
```
XNPV(discount, cashflow_amounts, cashflow_dates)
```
Calculates the net present value for a series of cash flows occurring at irregular intervals.

### YIELD
```
YIELD(settlement, maturity, rate, price, redemption, frequency, [day_count_convention])
```
Calculates the annual yield of a security paying periodic interest.

### YIELDDISC
```
YIELDDISC(settlement, maturity, price, redemption, [day_count_convention])
```
Calculates the annual yield of a discount security based on price.

### YIELDMAT
```
YIELDMAT(settlement, maturity, issue, rate, price, [day_count_convention])
```
Calculates the annual yield of a security paying interest at maturity.


Here's the markdown format for the provided table section related to Google functions:

## Google

### ARRAYFORMULA
```
ARRAYFORMULA(array_formula)
```
Enables the display of values returned from an array formula into multiple rows and/or columns and the use of non-array functions with arrays.

### DETECTLANGUAGE
```
DETECTLANGUAGE(text_or_range)
```
Identifies the language used in text within the specified range.

### GOOGLEFINANCE
```
GOOGLEFINANCE(ticker, [attribute], [start_date], [end_date|num_days], [interval])
```
Fetches current or historical securities information from Google Finance.

### GOOGLETRANSLATE
```
GOOGLETRANSLATE(text, [source_language], [target_language])
```
Translates text from one language into another.

### IMAGE
```
IMAGE(url, [mode], [height], [width])
```
Inserts an image into a cell.

### QUERY
```
QUERY(data, query, [headers])
```
Runs a Google Visualization API Query Language query across data.

### SPARKLINE
```
SPARKLINE(data, [options])
```
Creates a miniature chart contained within a single cell.

Here's the markdown format for the provided table section related to Info functions:

## Info

### ERROR.TYPE
```
ERROR.TYPE(reference)
```
Returns a number corresponding to the error value in a different cell.

### ISBLANK
```
ISBLANK(value)
```
Checks whether the referenced cell is empty.

### ISDATE
```
ISDATE(value)
```
Returns whether a value is a date.

### ISEMAIL
```
ISEMAIL(value)
```
Checks whether a value is a valid email address.

### ISERR
```
ISERR(value)
```
Checks whether a value is an error other than `#N/A`.

### ISERROR
```
ISERROR(value)
```
Checks whether a value is an error.

### ISFORMULA
```
ISFORMULA(cell)
```
Checks whether a formula is in the referenced cell.

### ISLOGICAL
```
ISLOGICAL(value)
```
Checks whether a value is `TRUE` or `FALSE`.

### ISNA
```
ISNA(value)
```
Checks whether a value is the error `#N/A`.

### ISNONTEXT
```
ISNONTEXT(value)
```
Checks whether a value is non-textual.

### ISNUMBER
```
ISNUMBER(value)
```
Checks whether a value is a number.

### ISREF
```
ISREF(value)
```
Checks whether a value is a valid cell reference.

### ISTEXT
```
ISTEXT(value)
```
Checks whether a value is text.

### N
```
N(value)
```
Returns the argument provided as a number.

### NA
```
NA()
```
Returns the "value not available" error, `#N/A`.

### TYPE
```
TYPE(value)
```
Returns a number associated with the type of data passed into the function.

### CELL
```
CELL(info_type, reference)
```
Returns the requested information about the specified cell.



Here's the markdown format for the provided table section related to Logical functions:

## Logical

### AND
```
AND(logical_expression1, [logical_expression2, ...])
```
Returns true if all of the provided arguments are logically true, and false if any of the provided arguments are logically false.

### FALSE
```
FALSE()
```
Returns the logical value `FALSE`.

### IF
```
IF(logical_expression, value_if_true, value_if_false)
```
Returns one value if a logical expression is `TRUE` and another if it is `FALSE`.

### IFERROR
```
IFERROR(value, [value_if_error])
```
Returns the first argument if it is not an error value, otherwise returns the second argument if present, or a blank if the second argument is absent.

### IFNA
```
IFNA(value, value_if_na)
```
Evaluates a value. If the value is an #N/A error, returns the specified value.

### IFS
```
IFS(condition1, value1, [condition2, value2], …)
```
Evaluates multiple conditions and returns a value that corresponds to the first true condition.

### LAMBDA
```
LAMBDA(name, formula_expression)
```
Creates and returns a custom function with a set of names and a formula_expression that uses them.

### LET
```
LET(name1, value_expression1, [name2, …], [value_expression2, …], formula_expression)
```
Assigns name with the value_expression results and returns the result of the formula_expression.

### NOT
```
NOT(logical_expression)
```
Returns the opposite of a logical value - `NOT(TRUE)` returns `FALSE`; `NOT(FALSE)` returns `TRUE`.

### OR
```
OR(logical_expression1, [logical_expression2, ...])
```
Returns true if any of the provided arguments are logically true, and false if all of the provided arguments are logically false.

### SWITCH
```
SWITCH(expression, case1, value1, [default or case2, value2], …)
```
Tests an expression against a list of cases and returns the corresponding value of the first matching case, with an optional default value if nothing else is met.

### TRUE
```
TRUE()
```
Returns the logical value `TRUE`.

### XOR
```
XOR(logical_expression1, [logical_expression2, ...])
```
Performs an exclusive or of 2 numbers that returns a 1 if the numbers are different, and a 0 otherwise.


Here's the markdown format for the provided table section related to Lookup functions:

## Lookup

### ADDRESS
```
ADDRESS(row, column, [absolute_relative_mode], [use_a1_notation], [sheet])
```
Returns a cell reference as a string.

### CHOOSE
```
CHOOSE(index, choice1, [choice2, ...])
```
Returns an element from a list of choices based on index.

### COLUMN
```
COLUMN([cell_reference])
```
Returns the column number of a specified cell, with `A=1`.

### COLUMNS
```
COLUMNS(range)
```
Returns the number of columns in a specified array or range.

### FORMULATEXT
```
FORMULATEXT(cell)
```
Returns the formula as a string.

### GETPIVOTDATA
```
GETPIVOTDATA(value_name, any_pivot_table_cell, [original_column, ...], [pivot_item, ...])
```
Extracts an aggregated value from a pivot table that corresponds to the specified row and column headings.

### HLOOKUP
```
HLOOKUP(search_key, range, index, [is_sorted])
```
Horizontal lookup. Searches across the first row of a range for a key and returns the value of a specified cell in the column found.

### INDEX
```
INDEX(reference, [row], [column])
```
Returns the content of a cell, specified by row and column offset.

### INDIRECT
```
INDIRECT(cell_reference_as_string, [is_A1_notation])
```
Returns a cell reference specified by a string.

### LOOKUP
```
LOOKUP(search_key, search_range|search_result_array, [result_range])
```
Looks through a row or column for a key and returns the value of the cell in a result range located in the same position as the search row or column.

### MATCH
```
MATCH(search_key, range, [search_type])
```
Returns the relative position of an item in a range that matches a specified value.

### OFFSET
```
OFFSET(cell_reference, offset_rows, offset_columns, [height], [width])
```
Returns a range reference shifted a specified number of rows and columns from a starting cell reference.

### ROW
```
ROW([cell_reference])
```
Returns the row number of a specified cell.

### ROWS
```
ROWS(range)
```
Returns the number of rows in a specified array or range.

### VLOOKUP
```
VLOOKUP(search_key, range, index, [is_sorted])
```
Vertical lookup. Searches down the first column of a range for a key and returns the value of a specified cell in the row found.

### XLOOKUP
```
XLOOKUP(search_key, lookup_range, result_range, missing_value, [match_mode], [search_mode])
```
Returns the values in the result range based on the position where a match was found in the lookup range. If no match is found, it returns the closest match.


Here's the markdown format for the provided table section related to Math functions:

## Math

### ABS
```
ABS(value)
```
Returns the absolute value of a number.

### ACOS
```
ACOS(value)
```
Returns the inverse cosine of a value, in radians.

### ACOSH
```
ACOSH(value)
```
Returns the inverse hyperbolic cosine of a number.

### ACOT
```
ACOT(value)
```
Returns the inverse cotangent of a value, in radians.

### ACOTH
```
ACOTH(value)
```
Returns the inverse hyperbolic cotangent of a value, in radians. Must not be between -1 and 1, inclusive.

### ASIN
```
ASIN(value)
```
Returns the inverse sine of a value, in radians.

### ASINH
```
ASINH(value)
```
Returns the inverse hyperbolic sine of a number.

### ATAN
```
ATAN(value)
```
Returns the inverse tangent of a value, in radians.

### ATAN2
```
ATAN2(x, y)
```
Returns the angle between the x-axis and a line segment from the origin (0,0) to specified coordinate pair (`x`,`y`), in radians.

### ATANH
```
ATANH(value)
```
Returns the inverse hyperbolic tangent of a number.

### BASE
```
BASE(value, base, [min_length])
```
Converts a number into a text representation in another base, for example, base 2 for binary.

### CEILING
```
CEILING(value, [factor])
```
Rounds a number up to the nearest integer multiple of specified significance.

### CEILING.MATH
```
CEILING.MATH(number, [significance], [mode])
```
Rounds a number up to the nearest integer multiple of specified significance, with negative numbers rounding toward or away from 0 depending on the mode.

### CEILING.PRECISE
```
CEILING.PRECISE(number, [significance])
```
Rounds a number up to the nearest integer multiple of specified significance. If the number is positive or negative, it is rounded up.

### COMBIN
```
COMBIN(n, k)
```
Returns the number of ways to choose some number of objects from a pool of a given size of objects.

### COMBINA
```
COMBINA(n, k)
```
Returns the number of ways to choose some number of objects from a pool of a given size of objects, including ways that choose the same object multiple times.

### COS
```
COS(angle)
```
Returns the cosine of an angle provided in radians.

### COSH
```
COSH(value)
```
Returns the hyperbolic cosine of any real number.

### COT
```
COT(angle)
```
Cotangent of an angle provided in radians.

### COTH
```
COTH(value)
```
Returns the hyperbolic cotangent of any real number.

### COUNTBLANK
```
COUNTBLANK(range)
```
Returns the number of empty cells in a given range.

### COUNTIF
```
COUNTIF(range, criterion)
```
Returns a conditional count across a range.

### COUNTIFS
```
COUNTIFS(criteria_range1, criterion1, [criteria_range2, criterion2, ...])
```
Returns the count of a range depending on multiple criteria.

### COUNTUNIQUE
```
COUNTUNIQUE(value1, [value2, ...])
```
Counts the number of unique values in a list of specified values and ranges.

### CSC
```
CSC(angle)
```
Returns the cosecant of an angle provided in radians.

### CSCH
```
CSCH(value)
```
The CSCH function returns the hyperbolic cosecant of any real number.

### DECIMAL
```
DECIMAL(value, base)
```
The DECIMAL function converts the text representation of a number in another base, to base 10 (decimal).

### DEGREES
```
DEGREES(angle)
```
Converts an angle value in radians to degrees.

### ERFC
```
ERFC(z)
```
Returns the complementary Gauss error function of a value.

### ERFC.PRECISE
```
ERFC.PRECISE(z)
```
See ERFC.

### EVEN
```
EVEN(value)
```
Rounds a number up to the nearest even integer.

### EXP
```
EXP(exponent)
```
Returns Euler's number, e (~2.718) raised to a power.

### FACT
```
FACT(value)
```
Returns the factorial of a number.

### FACTDOUBLE
```
FACTDOUBLE(value)
```
Returns the "double factorial" of a number.

### FLOOR
```
FLOOR(value, [factor])
```
Rounds a number down to the nearest integer multiple of specified significance.

### FLOOR

.MATH
```
FLOOR.MATH(number, [significance], [mode])
```
Rounds a number down to the nearest integer multiple of specified significance, with negative numbers rounding toward or away from 0 depending on the mode.

### FLOOR.PRECISE
```
FLOOR.PRECISE(number, [significance])
```
The FLOOR.PRECISE function rounds a number down to the nearest integer or multiple of specified significance.

### GAMMALN
```
GAMMALN(value)
```
Returns the the logarithm of a specified Gamma function, base e (Euler's number).

### GAMMALN.PRECISE
```
GAMMALN.PRECISE(value)
```
See GAMMALN.

### GCD
```
GCD(value1, value2)
```
Returns the greatest common divisor of one or more integers.

### IMLN
```
IMLN(complex_value)
```
Returns the logarithm of a complex number, base e (Euler's number).

### IMPOWER
```
IMPOWER(complex_base, exponent)
```
Returns a complex number raised to a power.

### IMSQRT
```
IMSQRT(complex_number)
```
Computes the square root of a complex number.

### INT
```
INT(value)
```
Rounds a number down to the nearest integer that is less than or equal to it.

### ISEVEN
```
ISEVEN(value)
```
Checks whether the provided value is even.

### ISO.CEILING
```
ISO.CEILING(number, [significance])
```
See CEILING.PRECISE.

### ISODD
```
ISODD(value)
```
Checks whether the provided value is odd.

### LCM
```
LCM(value1, value2)
```
Returns the least common multiple of one or more integers.

### LN
```
LN(value)
```
Returns the the logarithm of a number, base e (Euler's number).

### LOG
```
LOG(value, base)
```
Returns the the logarithm of a number given a base.

### LOG10
```
LOG10(value)
```
Returns the the logarithm of a number, base 10.

### MOD
```
MOD(dividend, divisor)
```
Returns the result of the modulo operator, the remainder after a division operation.

### MROUND
```
MROUND(value, factor)
```
Rounds one number to the nearest integer multiple of another.

### MULTINOMIAL
```
MULTINOMIAL(value1, value2)
```
Returns the factorial of the sum of values divided by the product of the values' factorials.

### MUNIT
```
MUNIT(dimension)
```
Returns a unit matrix of size dimension x dimension.

### ODD
```
ODD(value)
```
Rounds a number up to the nearest odd integer.

### PI
```
PI()
```
Returns the value of Pi to 14 decimal places.

### POWER
```
POWER(base, exponent)
```
Returns a number raised to a power.

### PRODUCT
```
PRODUCT(factor1, [factor2, ...])
```
Returns the result of multiplying a series of numbers together.

### QUOTIENT
```
QUOTIENT(dividend, divisor)
```
Returns one number divided by another.

### RADIANS
```
RADIANS(angle)
```
Converts an angle value in degrees to radians.

### RAND
```
RAND()
```
Returns a random number between 0 inclusive and 1 exclusive.

### RANDARRAY
```
RANDARRAY(rows, columns)
```
Generates an array of random numbers between 0 and 1.

### RANDBETWEEN
```
RANDBETWEEN(low, high)
```
Returns a uniformly random integer between two values, inclusive.

### ROUND
```
ROUND(value, [places])
```
Rounds a number to a certain number of decimal places according to standard rules.

### ROUNDDOWN
```
ROUNDDOWN(value, [places])
```
Rounds a number to a certain number of decimal places, always rounding down to the next valid increment.

### ROUNDUP
```
ROUNDUP(value, [places])
```
Rounds a number to a certain number of decimal places, always rounding up to the next valid increment.

### SEC
```
SEC(angle)
```
The SEC function returns the secant of an angle, measured in radians.

### SECH
```
SECH(value)
```
The SECH function returns the hyperbolic secant of an angle.

### SEQUENCE
```
SEQUENCE(rows, columns, start, step)
```
Returns an array of sequential numbers, such as 1, 2, 3, 4.

### SERIESSUM
```
SERIESSUM(x, n, m, a)
```
Given parameters `x`, `n

`, `m`, and `a`, returns the power series sum `a1x^n + a2x^(n+m) + ... + aix^(n+(i-1)m)`, where `i` is the number of entries in range `a`.

### SIGN
```
SIGN(value)
```
Given an input number, returns `-1` if it is negative, `1` if positive, and `0` if it is zero.

### SIN
```
SIN(angle)
```
Returns the sine of an angle provided in radians.

### SINH
```
SINH(value)
```
Returns the hyperbolic sine of any real number.

### SQRT
```
SQRT(value)
```
Returns the positive square root of a positive number.

### SQRTPI
```
SQRTPI(value)
```
Returns the positive square root of the product of Pi and the given positive number.

### SUBTOTAL
```
SUBTOTAL(function_code, range1, [range2, ...])
```
Returns a subtotal for a vertical range of cells using a specified aggregation function.

### SUM
```
SUM(value1, [value2, ...])
```
Returns the sum of a series of numbers and/or cells.

### SUMIF
```
SUMIF(range, criterion, [sum_range])
```
Returns a conditional sum across a range.

### SUMIFS
```
SUMIFS(sum_range, criteria_range1, criterion1, [criteria_range2, criterion2, ...])
```
Returns the sum of a range depending on multiple criteria.

### SUMSQ
```
SUMSQ(value1, [value2, ...])
```
Returns the sum of the squares of a series of numbers and/or cells.

### TAN
```
TAN(angle)
```
Returns the tangent of an angle provided in radians.

### TANH
```
TANH(value)
```
Returns the hyperbolic tangent of any real number.

### TRUNC
```
TRUNC(value, [places])
```
Truncates a number to a certain number of significant digits by omitting less significant digits.

## Operator
### ADD
```
ADD(value1, value2)
```
Returns the sum of two numbers. Equivalent to the `+` operator.

### CONCAT
```
CONCAT(value1, value2)
```
Returns the concatenation of two values. Equivalent to the `&` operator.

### DIVIDE
```
DIVIDE(dividend, divisor)
```
Returns one number divided by another. Equivalent to the `/` operator.

### EQ
```
EQ(value1, value2)
```
Returns `TRUE` if two specified values are equal and `FALSE` otherwise. Equivalent to the `=` operator.

### GT
```
GT(value1, value2)
```
Returns `TRUE` if the first argument is strictly greater than the second, and `FALSE` otherwise. Equivalent to the `>` operator.

### GTE
```
GTE(value1, value2)
```
Returns `TRUE` if the first argument is greater than or equal to the second, and `FALSE` otherwise. Equivalent to the `>=` operator.

### ISBETWEEN
```
ISBETWEEN(value_to_compare, lower_value, upper_value, lower_value_is_inclusive, upper_value_is_inclusive)
```
Checks whether a provided number is between two other numbers either inclusively or exclusively.

### LT
```
LT(value1, value2)
```
Returns `TRUE` if the first argument is strictly less than the second, and `FALSE` otherwise. Equivalent to the `<` operator.

### LTE
```
LTE(value1, value2)
```
Returns `TRUE` if the first argument is less than or equal to the second, and `FALSE` otherwise. Equivalent to the `<=` operator.

### MINUS
```
MINUS(value1, value2)
```
Returns the difference of two numbers. Equivalent to the `-` operator.

### MULTIPLY
```
MULTIPLY(factor1, factor2)
```
Returns the product of two numbers. Equivalent to the `*` operator.

### NE
```
NE(value1, value2)
```
Returns `TRUE` if two specified values are not equal and `FALSE` otherwise. Equivalent to the `<>` operator.

### POW
```
POW(base, exponent)
```
Returns a number raised to a power.

### UMINUS
```
UMINUS(value)
```
Returns a number with the sign reversed.

### UNARY_PERCENT
```
UNARY_PERCENT(percentage)
```
Returns a value interpreted as a percentage; that is, `UNARY_PERCENT(100)` equals `1`.

### UNIQUE
```
UNIQUE(range, by_column, exactly_once)
```
Returns unique rows in the provided source range, discarding duplicates. Rows are returned in the order in which they first appear in the source range.

### UPLUS
```
UPLUS(value)
```
Returns a specified number, unchanged.


## PARSER
### CONVERT
```
CONVERT(value, start_unit, end_unit)
```
Converts a numeric value to a different unit of measure.

### TO_DATE
```
TO_DATE(value)
```
Converts a provided number to a date.

### TO_DOLLARS
```
TO_DOLLARS(value)
```
Converts a provided number to a dollar value.

### TO_PERCENT
```
TO_PERCENT(value)
```
Converts a provided number to a percentage.

### TO_PURE_NUMBER
```
TO_PURE_NUMBER(value)
```
Converts a provided date/time, percentage, currency or other formatted numeric value to a pure number without formatting.

### TO_TEXT
```
TO_TEXT(value)
```
Converts a provided numeric value to a text value.

## STATISTICAL
### AVEDEV
```
AVEDEV(value1, [value2, ...])
```
Calculates the average of the magnitudes of deviations of data from a dataset's mean.

### AVERAGE
```
AVERAGE(value1, [value2, ...])
```
Returns the numerical average value in a dataset, ignoring text.

### AVERAGE.WEIGHTED
```
AVERAGE.WEIGHTED(values, weights, [additional values], [additional weights])
```
Finds the weighted average of a set of values, given the values and the corresponding weights.

### AVERAGEA
```
AVERAGEA(value1, [value2, ...])
```
Returns the numerical average value in a dataset.

### AVERAGEIF
```
AVERAGEIF(criteria_range, criterion, [average_range])
```
Returns the average of a range depending on criteria.

### AVERAGEIFS
```
AVERAGEIFS(average_range, criteria_range1, criterion1, [criteria_range2, criterion2, ...])
```
Returns the average of a range depending on multiple criteria.

### BETA.DIST
```
BETA.DIST(value, alpha, beta, cumulative, lower_bound, upper_bound)
```
Returns the probability of a given value as defined by the beta distribution function.

### BETA.INV
```
BETA.INV(probability, alpha, beta, lower_bound, upper_bound)
```
Returns the value of the inverse beta distribution function for a given probability.

### BETADIST
```
BETADIST(value, alpha, beta, lower_bound, upper_bound)
```
See BETA.DIST.

### BETAINV
```
BETAINV(probability, alpha, beta, lower_bound, upper_bound)
```
See BETA.INV.

### BINOM.DIST
```
BINOM.DIST(num_successes, num_trials, prob_success, cumulative)
```
See BINOMDIST.

### BINOM.INV
```
BINOM.INV(num_trials, prob_success, target_prob)
```
See CRITBINOM.

### BINOMDIST
```
BINOMDIST(num_successes, num_trials, prob_success, cumulative)
```
Calculates the probability of drawing a certain number of successes (or a maximum number of successes) in a certain number of tries given a population of a certain size containing a certain number of successes, with replacement of draws.

### CHIDIST
```
CHIDIST(x, degrees_freedom)
```
Calculates the right-tailed chi-squared distribution, often used in hypothesis testing.

### CHIINV
```
CHIINV(probability, degrees_freedom)
```
Calculates the inverse of the right-tailed chi-squared distribution.

### CHISQ.DIST
```
CHISQ.DIST(x, degrees_freedom, cumulative)
```
Calculates the left-tailed chi-squared distribution, often used in hypothesis testing.

### CHISQ.DIST.RT
```
CHISQ.DIST.RT(x, degrees_freedom)
```
Calculates the right-tailed chi-squared distribution, which is commonly used in hypothesis testing.

### CHISQ.INV
```
CHISQ.INV(probability, degrees_freedom)
```
Calculates the inverse of the left-tailed chi-squared distribution.

### CHISQ.INV.RT
```
CHISQ.INV.RT(probability, degrees_freedom)
```
Calculates the inverse of the right-tailed chi-squared distribution.

### CHISQ.TEST
```
CHISQ.TEST(observed_range, expected_range)
```
See CHITEST.

### CHITEST
```
CHITEST(observed_range, expected_range)
```
Returns the probability associated with a Pearson’s chi-squared test on the two ranges of data. Determines the likelihood that the observed categorical data is drawn from an expected distribution.

### CONFIDENCE
```
CONFIDENCE(alpha, standard_deviation, pop_size)
```
See CONFIDENCE.NORM.

### CONFIDENCE.NORM
```
CONFIDENCE.NORM(alpha, standard_deviation, pop_size)
```
Calculates the width of half the confidence interval for a normal distribution.

### CONFIDENCE.T
```
CONFIDENCE.T(alpha, standard_deviation, size)
```
Calculates the width of half the confidence interval for a Student’s t-distribution.

### CORREL
```
CORREL(data_y, data_x)
```
Calculates r, the Pearson product-moment correlation coefficient of a dataset.

### COUNT
```
COUNT(value1, [value2, ...])
```
Returns a count of the number of numeric values in a dataset.

### COUNTA
```
COUNTA(value1, [value2, ...])
```
Returns a count of the number of values in a dataset.

### COVAR
```
COVAR(data_y, data_x

)
```
Calculates the covariance of a dataset.

### COVARIANCE.P
```
COVARIANCE.P(data_y, data_x)
```
See COVAR.

### COVARIANCE.S
```
COVARIANCE.S(data_y, data_x)
```
Calculates the covariance of a dataset, where the dataset is a sample of the total population.

### CRITBINOM
```
CRITBINOM(num_trials, prob_success, target_prob)
```
Calculates the smallest value for which the cumulative binomial distribution is greater than or equal to a specified criteria.

### DEVSQ
```
DEVSQ(value1, value2)
```
Calculates the sum of squares of deviations based on a sample.

### EXPON.DIST
```
EXPON.DIST(x, LAMBDA, cumulative)
```
Returns the value of the exponential distribution function with a specified LAMBDA at a specified value.

### EXPONDIST
```
EXPONDIST(x, LAMBDA, cumulative)
```
See EXPON.DIST.

### F.DIST
```
F.DIST(x, degrees_freedom1, degrees_freedom2, cumulative)
```
Calculates the left-tailed F probability distribution (degree of diversity) for two data sets with given input x. Alternately called Fisher-Snedecor distribution or Snedecor's F distribution.

### F.DIST.RT
```
F.DIST.RT(x, degrees_freedom1, degrees_freedom2)
```
Calculates the right-tailed F probability distribution (degree of diversity) for two data sets with given input x. Alternately called Fisher-Snedecor distribution or Snedecor's F distribution.

### F.INV
```
F.INV(probability, degrees_freedom1, degrees_freedom2)
```
Calculates the inverse of the left-tailed F probability distribution. Also called the Fisher-Snedecor distribution or Snedecor’s F distribution.

### F.INV.RT
```
F.INV.RT(probability, degrees_freedom1, degrees_freedom2)
```
Calculates the inverse of the right-tailed F probability distribution. Also called the Fisher-Snedecor distribution or Snedecor’s F distribution.

### F.TEST
```
F.TEST(range1, range2)
```
See FTEST.

### FDIST
```
FDIST(x, degrees_freedom1, degrees_freedom2)
```
See F.DIST.RT.

### FINV
```
FINV(probability, degrees_freedom1, degrees_freedom2)
```
See F.INV.RT.

### FISHER
```
FISHER(value)
```
Returns the Fisher transformation of a specified value.

### FISHERINV
```
FISHERINV(value)
```
Returns the inverse Fisher transformation of a specified value.

### FORECAST
```
FORECAST(x, data_y, data_x)
```
Calculates the expected y-value for a specified x based on a linear regression of a dataset.

### FORECAST.LINEAR
```
FORECAST.LINEAR(x, data_y, data_x)
```
See FORECAST.

### FTEST
```
FTEST(range1, range2)
```
Returns the probability associated with an F-test for equality of variances. Determines whether two samples are likely to have come from populations with the same variance.

### GAMMA
```
GAMMA(number)
```
Returns the Gamma function evaluated at the specified value.

### GAMMA.DIST
```
GAMMA.DIST(x, alpha, beta, cumulative)
```
Calculates the gamma distribution, a two-parameter continuous probability distribution.

### GAMMA.INV
```
GAMMA.INV(probability, alpha, beta)
```
The GAMMA.INV function returns the value of the inverse gamma cumulative distribution function for the specified probability and alpha and beta parameters.

### GAMMADIST
```
GAMMADIST(x, alpha, beta, cumulative)
```
See GAMMA.DIST.

### GAMMAINV
```
GAMMAINV(probability, alpha, beta)
```
See GAMMA.INV.

### GAUSS
```
GAUSS(z)
```
The GAUSS function returns the probability that a random variable, drawn from a normal distribution, will be between the mean and z standard deviations above (or below) the mean.

### GEOMEAN
```
GEOMEAN(value1, value2)
```
Calculates the geometric mean of a dataset.

### HARMEAN
```
HARMEAN(value1, value2)
```
Calculates the harmonic mean of a dataset.

### HYPGEOM.DIST
```
HYPGEOM.DIST(num_successes, num_draws, successes_in_pop, pop_size)
```
See HYPGEOMDIST.

### HYPGEOMDIST


```
HYPGEOMDIST(num_successes, num_draws, successes_in_pop, pop_size)
```
Calculates the probability of drawing a certain number of successes in a certain number of tries given a population of a certain size containing a certain number of successes, without replacement of draws.

### INTERCEPT
```
INTERCEPT(data_y, data_x)
```
Calculates the y-value at which the line resulting from linear regression of a dataset will intersect the y-axis (x=0).

### KURT
```
KURT(value1, value2)
```
Calculates the kurtosis of a dataset, which describes the shape, and in particular the "peakedness" of that dataset.

### LARGE
```
LARGE(data, n)
```
Returns the nth largest element from a data set, where n is user-defined.

### LOGINV
```
LOGINV(x, mean, standard_deviation)
```
Returns the value of the inverse log-normal cumulative distribution with given mean and standard deviation at a specified value.

### LOGNORM.DIST
```
LOGNORM.DIST(x, mean, standard_deviation)
```
See LOGNORMDIST.

### LOGNORM.INV
```
LOGNORM.INV(x, mean, standard_deviation)
```
See LOGINV.

### LOGNORMDIST
```
LOGNORMDIST(x, mean, standard_deviation)
```
Returns the value of the log-normal cumulative distribution with given mean and standard deviation at a specified value.

### MARGINOFERROR
```
MARGINOFERROR(range, confidence)
```
Calculates the amount of random sampling error given a range of values and a confidence level.

### MAX
```
MAX(value1, [value2, ...])
```
Returns the maximum value in a numeric dataset.

### MAXA
```
MAXA(value1, value2)
```
Returns the maximum numeric value in a dataset.

### MAXIFS
```
MAXIFS(range, criteria_range1, criterion1, [criteria_range2, criterion2], …)
```
Returns the maximum value in a range of cells, filtered by a set of criteria.

### MEDIAN
```
MEDIAN(value1, [value2, ...])
```
Returns the median value in a numeric dataset.

### MIN
```
MIN(value1, [value2, ...])
```
Returns the minimum value in a numeric dataset.

### MINA
```
MINA(value1, value2)
```
Returns the minimum numeric value in a dataset.

### MINIFS
```
MINIFS(range, criteria_range1, criterion1, [criteria_range2, criterion2], …)
```
Returns the minimum value in a range of cells, filtered by a set of criteria.

### MODE
```
MODE(value1, [value2, ...])
```
Returns the most commonly occurring value in a dataset.

### MODE.MULT
```
MODE.MULT(value1, value2)
```
Returns the most commonly occurring values in a dataset.

### MODE.SNGL
```
MODE.SNGL(value1, [value2, ...])
```
See MODE.

### NEGBINOM.DIST
```
NEGBINOM.DIST(num_failures, num_successes, prob_success)
```
See NEGBINOMDIST.

### NEGBINOMDIST
```
NEGBINOMDIST(num_failures, num_successes, prob_success)
```
Calculates the probability of drawing a certain number of failures before a certain number of successes given a probability of success in independent trials.

### NORM.DIST
```
NORM.DIST(x, mean, standard_deviation, cumulative)
```
See NORMDIST.

### NORM.INV
```
NORM.INV(x, mean, standard_deviation)
```
See NORMINV.

### NORM.S.DIST
```
NORM.S.DIST(x)
```
See NORMSDIST.

### NORM.S.INV
```
NORM.S.INV(x)
```
See NORMSINV.

### NORMDIST
```
NORMDIST(x, mean, standard_deviation, cumulative)
```
Returns the value of the normal distribution function (or normal cumulative distribution function) for a specified value, mean, and standard deviation.

### NORMINV
```
NORMINV(x, mean, standard_deviation)
```
Returns the value of the inverse normal distribution function for a specified value, mean, and standard deviation.

### NORMSDIST
```
NORMSDIST(x)
```
Returns the value of the standard normal cumulative distribution function for a specified value.

### NORMSINV
```
NORMSINV(x)
```
Returns the value of the inverse standard normal distribution function for a specified value.

### PEARSON
```
PEARSON(data_y, data_x)
```
Calculates r, the Pearson product-moment correlation coefficient of a

 dataset.

### PERCENTILE
```
PERCENTILE(data, percentile)
```
Returns the value at a given percentile of a dataset.

### PERCENTILE.EXC
```
PERCENTILE.EXC(data, percentile)
```
Returns the value at a given percentile of a dataset, exclusive of 0 and 1.

### PERCENTILE.INC
```
PERCENTILE.INC(data, percentile)
```
See PERCENTILE.

### PERCENTRANK
```
PERCENTRANK(data, value, [significant_digits])
```
Returns the percentage rank (percentile) of a specified value in a dataset.

### PERCENTRANK.EXC
```
PERCENTRANK.EXC(data, value, [significant_digits])
```
Returns the percentage rank (percentile) from 0 to 1 exclusive of a specified value in a dataset.

### PERCENTRANK.INC
```
PERCENTRANK.INC(data, value, [significant_digits])
```
Returns the percentage rank (percentile) from 0 to 1 inclusive of a specified value in a dataset.

### PERMUTATIONA
```
PERMUTATIONA(number, number_chosen)
```
Returns the number of permutations for selecting a group of objects (with replacement) from a total number of objects.

### PERMUT
```
PERMUT(n, k)
```
Returns the number of ways to choose some number of objects from a pool of a given size of objects, considering order.

### PHI
```
PHI(x)
```
The PHI function returns the value of the normal distribution with mean 0 and standard deviation 1.

### POISSON
```
POISSON(x, mean, cumulative)
```
See POISSON.DIST.

### POISSON.DIST
```
POISSON.DIST(x, mean, [cumulative])
```
Returns the value of the Poisson distribution function (or Poisson cumulative distribution function) for a specified value and mean.

### PROB
```
PROB(data, probabilities, low_limit, [high_limit])
```
Given a set of values and corresponding probabilities, calculates the probability that a value chosen at random falls between two limits.

### QUARTILE
```
QUARTILE(data, quartile_number)
```
Returns a value nearest to a specified quartile of a dataset.

### QUARTILE.EXC
```
QUARTILE.EXC(data, quartile_number)
```
Returns value nearest to a given quartile of a dataset, exclusive of 0 and 4.

### QUARTILE.INC
```
QUARTILE.INC(data, quartile_number)
```
See QUARTILE.

### RANK
```
RANK(value, data, [is_ascending])
```
Returns the rank of a specified value in a dataset.

### RANK.AVG
```
RANK.AVG(value, data, [is_ascending])
```
Returns the rank of a specified value in a dataset. If there is more than one entry of the same value in the dataset, the average rank of the entries will be returned.

### RANK.EQ
```
RANK.EQ(value, data, [is_ascending])
```
Returns the rank of a specified value in a dataset. If there is more than one entry of the same value in the dataset, the top rank of the entries will be returned.

### RSQ
```
RSQ(data_y, data_x)
```
Calculates the square of r, the Pearson product-moment correlation coefficient of a dataset.

### SKEW
```
SKEW(value1, value2)
```
Calculates the skewness of a dataset, which describes the symmetry of that dataset about the mean.

### SKEW.P
```
SKEW.P(value1, value2)
```
Calculates the skewness of a dataset that represents the entire population.

### SLOPE
```
SLOPE(data_y, data_x)
```
Calculates the slope of the line resulting from linear regression of a dataset.

### SMALL
```
SMALL(data, n)
```
Returns the nth smallest element from a data set, where n is user-defined.

### STANDARDIZE
```
STANDARDIZE(value, mean, standard_deviation)
```
Calculates the normalized equivalent of a random variable given mean and standard deviation of the distribution.

### STDEV
```
STDEV(value1, [value2, ...])
```
Calculates the standard deviation based on a sample.

### STDEV.P
```
STDEV.P(value1, [value2, ...])
```
See STDEVP.

### STDEV.S
```
STDEV.S(value1, [value2, ...])
```
See STDEV.

### STDEVA
```
STDEVA(value1, value2)
```
Calculates the standard deviation based on a sample, setting text

 to the value `0`.

### STDEVP
```
STDEVP(value1, value2)
```
Calculates the standard deviation based on an entire population.

### STDEVPA
```
STDEVPA(value1, value2)
```
Calculates the standard deviation based on an entire population, setting text to the value `0`.

### STEYX
```
STEYX(data_y, data_x)
```
Calculates the standard error of the predicted y-value for each x in the regression of a dataset.

### T.DIST
```
T.DIST(x, degrees_freedom, cumulative)
```
Returns the right tailed Student distribution for a value x.

### T.DIST.2T
```
T.DIST.2T(x, degrees_freedom)
```
Returns the two tailed Student distribution for a value x.

### T.DIST.RT
```
T.DIST.RT(x, degrees_freedom)
```
Returns the right tailed Student distribution for a value x.

### T.INV
```
T.INV(probability, degrees_freedom)
```
Calculates the negative inverse of the one-tailed TDIST function.

### T.INV.2T
```
T.INV.2T(probability, degrees_freedom)
```
Calculates the inverse of the two-tailed TDIST function.

### T.TEST
```
T.TEST(range1, range2, tails, type)
```
Returns the probability associated with Student's t-test. Determines whether two samples are likely to have come from the same two underlying populations that have the same mean.

### TDIST
```
TDIST(x, degrees_freedom, tails)
```
Calculates the probability for Student's t-distribution with a given input (x).

### TINV
```
TINV(probability, degrees_freedom)
```
See T.INV.2T.

### TRIMMEAN
```
TRIMMEAN(data, exclude_proportion)
```
Calculates the mean of a dataset excluding some proportion of data from the high and low ends of the dataset.

### TTEST
```
TTEST(range1, range2, tails, type)
```
See T.TEST.

### VAR
```
VAR(value1, [value2, ...])
```
Calculates the variance based on a sample.

### VAR.P
```
VAR.P(value1, [value2, ...])
```
See VARP.

### VAR.S
```
VAR.S(value1, [value2, ...])
```
See VAR.

### VARA
```
VARA(value1, value2)
```
Calculates an estimate of variance based on a sample, setting text to the value `0`.

### VARP
```
VARP(value1, value2)
```
Calculates the variance based on an entire population.

### VARPA
```
VARPA(value1, value2,...)
```
Calculates the variance based on an entire population, setting text to the value `0`.

### WEIBULL
```
WEIBULL(x, shape, scale, cumulative)
```
Returns the value of the Weibull distribution function (or Weibull cumulative distribution function) for a specified shape and scale.

### WEIBULL.DIST
```
WEIBULL.DIST(x, shape, scale, cumulative)
```
See WEIBULL.

### Z.TEST
```
Z.TEST(data, value, [standard_deviation])
```
Returns the one-tailed P-value of a Z-test with standard distribution.

### ZTEST
```
ZTEST(data, value, [standard_deviation])
```
See Z.TEST.

## TEXT
### ARABIC
```
ARABIC(roman_numeral)
```
Computes the value of a Roman numeral.

### ASC
```
ASC(text)
```
Converts full-width ASCII and katakana characters to their half-width counterparts. All standard-width characters will remain unchanged.

### CHAR
```
CHAR(table_number)
```
Convert a number into a character according to the current Unicode table.

### CLEAN
```
CLEAN(text)
```
Returns the text with the non-printable ASCII characters removed.

### CODE
```
CODE(string)
```
Returns the numeric Unicode map value of the first character in the string provided.

### CONCATENATE
```
CONCATENATE(string1, [string2, ...])
```
Appends strings to one another.

### DOLLAR
```
DOLLAR(number, [number_of_places])
```
Formats a number into the locale-specific currency format.

### EXACT
```
EXACT(string1, string2)
```
Tests whether two strings are identical.

### FIND
```
FIND(search_for, text_to_search, [starting_at])
```
Returns the position at which a string is first found within text.

### FINDB
```
FINDB(search_for, text_to_search, [starting_at])
```
Returns the position at which a string is first found within text counting each double-character as 2.

### FIXED
```
FIXED(number, [number_of_places], [suppress_separator])
```
Formats a number with a fixed number of decimal places.

### JOIN
```
JOIN(delimiter, value_or_array1, [value_or_array2, ...])
```
Concatenates the elements of one or more one-dimensional arrays using a specified delimiter.

### LEFT
```
LEFT(string, [number_of_characters])
```
Returns a substring from the beginning of a specified string.

### LEFTB
```
LEFTB(string, num_of_bytes)
```
Returns the left portion of a string up to a certain number of bytes.

### LEN
```
LEN(text)
```
Returns the length of a string.

### LENB
```
LENB(string)
```
Returns the length of a string in bytes.

### LOWER
```
LOWER(text)
```
Converts a specified string to lowercase.

### MID
```
MID(string, starting_at, extract_length)
```
Returns a segment of a string.

### MIDB
```
MIDB(string)
```
Returns a section of a string starting at a given character and up to a specified number of bytes.

### PROPER
```
PROPER(text_to_capitalize)
```
Capitalizes each word in a specified string.

### REGEXEXTRACT
```
REGEXEXTRACT(text, regular_expression)
```
Extracts matching substrings according to a regular expression.

### REGEXMATCH
```
REGEXMATCH(text, regular_expression)
```
Determines whether a piece of text matches a regular expression.

### REGEXREPLACE
```
REGEXREPLACE(text, regular_expression, replacement)
```
Replaces part of a text string with a different text string using regular expressions.

### REPLACE
```
REPLACE(text, position, length, new_text)
```
Replaces part of a text string with a different text string.

### REPLACEB
```
REPLACEB(text, position, num_bytes, new_text)
```
Replaces part of a text string, based on a number of bytes, with a different text string.

### REPT
```
REPT(text_to_repeat, number_of_repetitions)
```
Returns specified text repeated a number of times.

### RIGHT
```
RIGHT(string, [number_of_characters])
```
Returns a substring from the end of a specified string.

### RIGHTB
```
RIGHTB(string, num_of_bytes)
```
Returns the right portion of a string up to a certain number of bytes.

### ROMAN
```
ROMAN(number, [rule_relaxation])
```
Formats a number in Roman numerals.

### SEARCH
```
SEARCH(search_for, text_to_search, [starting_at])
```
Returns the position at which a string is first found within text.

### SEARCHB
```
SEARCHB(search_for, text_to_search, [starting_at])
```
Returns the position at which a string is first found within text counting each double-character as 2.

### SPLIT
```
SPLIT(text, delimiter, [split_by_each], [remove_empty_text])
```
Divides text around a specified character or string, and puts each fragment into a separate cell in the row.

### SUBSTITUTE
```
SUBSTITUTE(text_to_search, search_for, replace_with, [occurrence_number])
```
Replaces existing text with new text in a string.

### T
```
T(value)
```
Returns string arguments as text.

### TEXT
```
TEXT(number, format)
```
Converts a number into text according

 to a specified format.

### TEXTJOIN
```
TEXTJOIN(delimiter, ignore_empty, text1, [text2], …)
```
Combines the text from multiple strings and/or arrays, with a specifiable delimiter separating the different texts.

### TRIM
```
TRIM(text)
```
Removes leading and trailing spaces in a specified string.

### UNICHAR
```
UNICHAR(number)
```
Returns the Unicode character for a number.

### UNICODE
```
UNICODE(text)
```
Returns the decimal Unicode value of the first character of the text.

### UPPER
```
UPPER(text)
```
Converts a specified string to uppercase.

### VALUE
```
VALUE(text)
```
Converts a string in any of the date, time, or number formats that Google Sheets understands into a number.

## WEB
### ENCODEURL
```
ENCODEURL(text)
```
Encodes a string of text for the purpose of using in a URL query.

### HYPERLINK
```
HYPERLINK(url, [link_label])
```
Creates a hyperlink inside a cell.

### IMPORTDATA
```
IMPORTDATA(url)
```
Imports data at a given URL in .csv (comma-separated value) or .tsv (tab-separated value) format.

### IMPORTFEED
```
IMPORTFEED(url, [query], [headers], [num_items])
```
Imports an RSS or ATOM feed.

### IMPORTHTML
```
IMPORTHTML(url, query, index)
```
Imports data from a table or list within an HTML page.

### IMPORTRANGE
```
IMPORTRANGE(spreadsheet_url, range_string)
```
Imports a range of cells from a specified spreadsheet.

### IMPORTXML
```
IMPORTXML(url, xpath_query)
```
Imports data from any of various structured data types including XML, HTML, CSV, TSV, and RSS and ATOM XML feeds.

### ISURL
```
ISURL(value)
```
Checks whether a value is a valid URL.This comprehensive cheat sheet encompasses a wide range of functions available in[ Google Sheets](https://support.google.com/docs/table/25273?hl=en), categorized into [**Array**](#array), [**Database**](#database), [**Date**](#date), [**Engineering**](#engineering), [**Filter**](#filter), [**Financial**](#financial), [**Google**](#google), [**Info**](#info), [**Logical**](#logical), [**Lookup**](#lookup), [**Math**](#math), [**Operator**](#operator), [**Parser**](#parser), [**Statistical**](#statistical), [**Text**](#text), and [**Web**](#web). It provides concise descriptions and syntax for each function, making it an invaluable resource for users looking to perform various operations from simple calculations to complex data manipulation and web-based imports. Whether you're formatting data, analyzing statistics, or importing information from external sources, this cheat sheet is designed to enhance productivity and streamline your spreadsheet tasks.


## Array

### ARRAY_CONSTRAIN
```
ARRAY_CONSTRAIN(input_range, num_rows, num_cols)
```
Constrains an array result to a specified size.

### BYCOL
```
BYCOL(array_or_range, LAMBDA)
```
Groups an array by columns by application of a LAMBDA function to each column.

### BYROW
```
BYROW(array_or_range, LAMBDA)
```
Groups an array by rows by application of a LAMBDA function to each row.

### CHOOSECOLS
```
CHOOSECOLS(array, col_num1, [col_num2]) 
```
Creates a new array from the selected columns in the existing range.

### CHOOSEROWS
```
CHOOSEROWS(array, row_num1, [row_num2])
```
Creates a new array from the selected rows in the existing range.

### FLATTEN
```
FLATTEN(range1,[range2,...])
```
Flattens all the values from one or more ranges into a single column.

### FREQUENCY
```
FREQUENCY(data, classes)
```
Calculates the frequency distribution of a one-column array into specified classes.

### GROWTH
```
GROWTH(known_data_y, [known_data_x], [new_data_x], [b])
```
Given partial data about an exponential growth trend, fits an ideal exponential growth trend and/or predicts further values.

### HSTACK
```
HSTACK(range1; [range2, …])
```
Appends ranges horizontally and in sequence to return a larger array.

### LINEST
```
LINEST(known_data_y, [known_data_x], [calculate_b], [verbose])
```
Given partial data about a linear trend, calculates various parameters about the ideal linear trend using the least-squares method.

### LOGEST
```
LOGEST(known_data_y, [known_data_x], [b], [verbose])
```
Given partial data about an exponential growth curve, calculates various parameters about the best fit ideal exponential growth curve.

### MAKEARRAY
```
MAKEARRAY(rows, columns, LAMBDA)
```
Returns an array of specified dimensions with values calculated by application of a LAMBDA function.

### MAP
```
MAP(array1, [array2, ...], LAMBDA)
```
Maps each value in the given arrays to a new value by application of a LAMBDA function to each value.

### MDETERM
```
MDETERM(square_matrix)
```
Returns the matrix determinant of a square matrix specified as an array or range.

### MINVERSE
```
MINVERSE(square_matrix)
```
Returns the multiplicative inverse of a square matrix specified as an array or range.

### MMULT
```
MMULT(matrix1, matrix2)
```
Calculates the matrix product of two matrices specified as arrays or ranges.

### REDUCE
```
REDUCE(initial_value, array_or_range, LAMBDA)
```
Reduces an array to an accumulated result by application of a LAMBDA function to each value.

### SCAN
```
SCAN(initial_value, array_or_range, LAMBDA)
```
Scans an array and produces intermediate values by application of a LAMBDA function to each value. Returns an array of the intermediate values obtained at each step.

### SUMPRODUCT
```
SUMPRODUCT(array1, [array2, ...])
```
Calculates the sum of the products of corresponding entries in two equal-sized arrays or ranges.

### SUMX2MY2
```
SUMX2MY2(array_x, array_y)
```
Calculates the sum of the differences of the squares of values in two arrays.

### SUMX2PY2
```
SUMX2PY2(array_x, array_y)
```
Calculates the sum of the sums of the squares of values in two arrays.

### SUMXMY2
```
SUMXMY2(array_x, array_y)
```
Calculates the sum of the squares of differences of values in two arrays.

### TOCOL
```
TOCOL(array_or_range, [ignore], [scan_by_column])
```
Transforms an array or range of cells into a single column.

### TOROW
```
TOROW(array_or_range, [ignore], [scan_by_column])
```
Transforms an array or range of cells into a single row.

### TRANSPOSE
```
TRANSPOSE(array_or_range)
```
Transposes the rows and columns of an array or range of cells.

### TREND
```
TREND(known_data_y, [known_data_x], [new_data_x], [b])
```
Given partial data about a linear trend, fits an ideal linear trend using the least squares method and/or predicts further values.

### VSTACK
```
VSTACK(range1; [range2, …])
```


Appends ranges vertically and in sequence to return a larger array.

### WRAPCOLS
```
WRAPCOLS(range, wrap_count, [pad_with])
```
Wraps the provided row or column of cells by columns after a specified number of elements to form a new array.

### WRAPROWS
```
WRAPROWS(range, wrap_count, [pad_with])
```
Wraps the provided row or column of cells by rows after a specified number of elements to form a new array.


Here's how the provided table part would be formatted in markdown:

## Database

### DAVERAGE
```
DAVERAGE(database, field, criteria)
```
Returns the average of a set of values selected from a database table-like array or range using a SQL-like query.

### DCOUNT
```
DCOUNT(database, field, criteria)
```
Counts numeric values selected from a database table-like array or range using a SQL-like query.

### DCOUNTA
```
DCOUNTA(database, field, criteria)
```
Counts values, including text, selected from a database table-like array or range using a SQL-like query.

### DGET
```
DGET(database, field, criteria)
```
Returns a single value from a database table-like array or range using a SQL-like query.

### DMAX
```
DMAX(database, field, criteria)
```
Returns the maximum value selected from a database table-like array or range using a SQL-like query.

### DMIN
```
DMIN(database, field, criteria)
```
Returns the minimum value selected from a database table-like array or range using a SQL-like query.

### DPRODUCT
```
DPRODUCT(database, field, criteria)
```
Returns the product of values selected from a database table-like array or range using a SQL-like query.

### DSTDEV
```
DSTDEV(database, field, criteria)
```
Returns the standard deviation of a population sample selected from a database table-like array or range using a SQL-like query.

### DSTDEVP
```
DSTDEVP(database, field, criteria)
```
Returns the standard deviation of an entire population selected from a database table-like array or range using a SQL-like query.

### DSUM
```
DSUM(database, field, criteria)
```
Returns the sum of values selected from a database table-like array or range using a SQL-like query.

### DVAR
```
DVAR(database, field, criteria)
```
Returns the variance of a population sample selected from a database table-like array or range using a SQL-like query.

### DVARP
```
DVARP(database, field, criteria)
```
Returns the variance of an entire population selected from a database table-like array or range using a SQL-like query.



For this part of the table related to date functions, here's how it would be translated into markdown format:

## Date

### DATE
```
DATE(year, month, day)
```
Converts a provided year, month, and day into a date.

### DATEDIF
```
DATEDIF(start_date, end_date, unit)
```
Calculates the number of days, months, or years between two dates.

### DATEVALUE
```
DATEVALUE(date_string)
```
Converts a provided date string in a known format to a date value.

### DAY
```
DAY(date)
```
Returns the day of the month that a specific date falls on, in numeric format.

### DAYS
```
DAYS(end_date, start_date)
```
Returns the number of days between two dates.

### DAYS360
```
DAYS360(start_date, end_date, [method])
```
Returns the difference between two days based on the 360 day year used in some financial interest calculations.

### EDATE
```
EDATE(start_date, months)
```
Returns a date a specified number of months before or after another date.

### EOMONTH
```
EOMONTH(start_date, months)
```
Returns a date representing the last day of a month which falls a specified number of months before or after another date.

### EPOCHTODATE
```
EPOCHTODATE(timestamp, [unit])
```
Converts a Unix epoch timestamp in seconds, milliseconds, or microseconds to a datetime in UTC.

### HOUR
```
HOUR(time)
```
Returns the hour component of a specific time, in numeric format.

### ISOWEEKNUM
```
ISOWEEKNUM(date)
```
Returns the number of the ISO week of the year where the provided date falls.

### MINUTE
```
MINUTE(time)
```
Returns the minute component of a specific time, in numeric format.

### MONTH
```
MONTH(date)
```
Returns the month of the year a specific date falls in, in numeric format.

### NETWORKDAYS
```
NETWORKDAYS(start_date, end_date, [holidays])
```
Returns the number of net working days between two provided days.

### NETWORKDAYS.INTL
```
NETWORKDAYS.INTL(start_date, end_date, [weekend], [holidays])
```
Returns the number of net working days between two provided days excluding specified weekend days and holidays.

### NOW
```
NOW()
```
Returns the current date and time as a date value.

### SECOND
```
SECOND(time)
```
Returns the second component of a specific time, in numeric format.

### TIME
```
TIME(hour, minute, second)
```
Converts a provided hour, minute, and second into a time.

### TIMEVALUE
```
TIMEVALUE(time_string)
```
Returns the fraction of a 24-hour day the time represents.

### TODAY
```
TODAY()
```
Returns the current date as a date value.

### WEEKDAY
```
WEEKDAY(date, [type])
```
Returns a number representing the day of the week of the date provided.

### WEEKNUM
```
WEEKNUM(date, [type])
```
Returns a number representing the week of the year where the provided date falls.

### WORKDAY
```
WORKDAY(start_date, num_days, [holidays])
```
Calculates the end date after a specified number of working days.

### WORKDAY.INTL
```
WORKDAY.INTL(start_date, num_days, [weekend], [holidays])
```
Calculates the date after a specified number of workdays excluding specified weekend days and holidays.

### YEAR
```
YEAR(date)
```
Returns the year specified by a given date.

### YEARFRAC
```
YEARFRAC(start_date, end_date, [day_count_convention])
```
Returns the number of years, including fractional years, between two dates using a specified day count convention.


Here's how the provided table part related to engineering functions would be translated into markdown format:

## Engineering

### BIN2DEC
```
BIN2DEC(signed_binary_number)
```
Converts a signed binary number to decimal format.

### BIN2HEX
```
BIN2HEX(signed_binary_number, [significant_digits])
```
Converts a signed binary number to signed hexadecimal format.

### BIN2OCT
```
BIN2OCT(signed_binary_number, [significant_digits])
```
Converts a signed binary number to signed octal format.

### BITAND
```
BITAND(value1, value2)
```
Bitwise boolean AND of two numbers.

### BITLSHIFT
```
BITLSHIFT(value, shift_amount)
```
Shifts the bits of the input a certain number of places to the left.

### BITOR
```
BITOR(value1, value2)
```
Bitwise boolean OR of 2 numbers.

### BITRSHIFT
```
BITRSHIFT(value, shift_amount)
```
Shifts the bits of the input a certain number of places to the right.

### BITXOR
```
BITXOR(value1, value2)
```
Bitwise XOR (exclusive OR) of 2 numbers.

### COMPLEX
```
COMPLEX(real_part, imaginary_part, [suffix])
```
Creates a complex number given real and imaginary coefficients.

### DEC2BIN
```
DEC2BIN(decimal_number, [significant_digits])
```
Converts a decimal number to signed binary format.

### DEC2HEX
```
DEC2HEX(decimal_number, [significant_digits])
```
Converts a decimal number to signed hexadecimal format.

### DEC2OCT
```
DEC2OCT(decimal_number, [significant_digits])
```
Converts a decimal number to signed octal format.

### DELTA
```
DELTA(number1, [number2])
```
Compare two numeric values, returning 1 if they're equal.

### ERF
```
ERF(lower_bound, [upper_bound])
```
The ERF function returns the integral of the Gauss error function over an interval of values.

### ERF.PRECISE
```
ERF.PRECISE(lower_bound, [upper_bound])
```
See ERF for more details.

### GESTEP
```
GESTEP(value, [step])
```
Returns 1 if the rate is strictly greater than or equal to the provided step value or 0 otherwise.

### HEX2BIN
```
HEX2BIN(signed_hexadecimal_number, [significant_digits])
```
Converts a signed hexadecimal number to signed binary format.

### HEX2DEC
```
HEX2DEC(signed_hexadecimal_number)
```
Converts a signed hexadecimal number to decimal format.

### HEX2OCT
```
HEX2OCT(signed_hexadecimal_number, significant_digits)
```
Converts a signed hexadecimal number to signed octal format.

### IMABS
```
IMABS(number)
```
Returns absolute value of a complex number.

### IMAGINARY
```
IMAGINARY(complex_number)
```
Returns the imaginary coefficient of a complex number.

### IMARGUMENT
```
IMARGUMENT(number)
```
Returns the angle of the given complex number in radians.

### IMCONJUGATE
```
IMCONJUGATE(number)
```
Returns the complex conjugate of a number.

### IMCOS
```
IMCOS(number)
```
Returns the cosine of the given complex number.

### IMCOSH
```
IMCOSH(number)
```
Returns the hyperbolic cosine of the given complex number.

### IMCOT
```
IMCOT(number)
```
Returns the cotangent of the given complex number.

### IMCOTH
```
IMCOTH(number)
```
Returns the hyperbolic cotangent of the given complex number.

### IMCSC
```
IMCSC(number)
```
Returns the cosecant of the given complex number.

### IMCSCH
```
IMCSCH(number)
```
Returns the hyperbolic cosecant of the given complex number.

### IMDIV
```
IMDIV(dividend, divisor)
```
Returns one complex number divided by another.

### IMEXP
```
IMEXP(exponent)
```
Returns Euler's number, e, raised to a complex power.

### IMLOG
```
IMLOG(value, base)
```
Returns the logarithm of a complex number for a specified base.

### IMLOG10
```
IMLOG10(value)
```
Returns the logarithm of a complex number with base 10.

### IMLOG2
```
IMLOG2(value)
```
Returns the logarithm of a complex number with base 2.

### IMPRODUCT
```
IMPRODUCT(factor1, [factor2, ...])
```
Returns the result of multiplying a series of

 complex numbers together.

### IMREAL
```
IMREAL(complex_number)
```
Returns the real coefficient of a complex number.

### IMSEC
```
IMSEC(number)
```
Returns the secant of the given complex number.

### IMSECH
```
IMSECH(number)
```
Returns the hyperbolic secant of the given complex number.

### IMSIN
```
IMSIN(number)
```
Returns the sine of the given complex number.

### IMSINH
```
IMSINH(number)
```
Returns the hyperbolic sine of the given complex number.

### IMSUB
```
IMSUB(first_number, second_number)
```
Returns the difference between two complex numbers.

### IMSUM
```
IMSUM(value1, [value2, ...])
```
Returns the sum of a series of complex numbers.

### IMTAN
```
IMTAN(number)
```
Returns the tangent of the given complex number.

### IMTANH
```
IMTANH(number)
```
Returns the hyperbolic tangent of the given complex number.

### OCT2BIN
```
OCT2BIN(signed_octal_number, [significant_digits])
```
Converts a signed octal number to signed binary format.

### OCT2DEC
```
OCT2DEC(signed_octal_number)
```
Converts a signed octal number to decimal format.

### OCT2HEX
```
OCT2HEX(signed_octal_number, [significant_digits])
```
Converts a signed octal number to signed hexadecimal format.


Here's the markdown format for the provided table section related to filter functions:

## Filter

### FILTER
```
FILTER(range, condition1, [condition2])
```
Returns a filtered version of the source range, returning only rows or columns which meet the specified conditions.

### SORT
```
SORT(range, sort_column, is_ascending, [sort_column2], [is_ascending2])
```
Sorts the rows of a given array or range by the values in one or more columns.

### SORTN
```
SORTN(range, [n], [display_ties_mode], [sort_column1, is_ascending1], ...)
```
Returns the first n items in a data set after performing a sort.

### UNIQUE
```
UNIQUE(range)
```
Returns unique rows in the provided source range, discarding duplicates. Rows are returned in the order in which they first appear in the source range.


Here's the markdown format for the provided table section related to financial functions:

## Financial

### ACCRINT
```
ACCRINT(issue, first_payment, settlement, rate, redemption, frequency, [day_count_convention])
```
Calculates the accrued interest of a security that has periodic payments.

### ACCRINTM
```
ACCRINTM(issue, maturity, rate, [redemption], [day_count_convention])
```
Calculates the accrued interest of a security that pays interest at maturity.

### AMORLINC
```
AMORLINC(cost, purchase_date, first_period_end, salvage, period, rate, [basis])
```
Returns the depreciation for an accounting period, or the prorated depreciation if the asset was purchased in the middle of a period.

### COUPDAYBS
```
COUPDAYBS(settlement, maturity, frequency, [day_count_convention])
```
Calculates the number of days from the first coupon, or interest payment, until settlement.

### COUPDAYS
```
COUPDAYS(settlement, maturity, frequency, [day_count_convention])
```
Calculates the number of days in the coupon, or interest payment, period that contains the specified settlement date.

### COUPDAYSNC
```
COUPDAYSNC(settlement, maturity, frequency, [day_count_convention])
```
Calculates the number of days from the settlement date until the next coupon, or interest payment.

### COUPNCD
```
COUPNCD(settlement, maturity, frequency, [day_count_convention])
```
Calculates next coupon, or interest payment, date after the settlement date.

### COUPNUM
```
COUPNUM(settlement, maturity, frequency, [day_count_convention])
```
Calculates the number of coupons, or interest payments, between the settlement date and the maturity date of the investment.

### COUPPCD
```
COUPPCD(settlement, maturity, frequency, [day_count_convention])
```
Calculates last coupon, or interest payment, date before the settlement date.

### CUMIPMT
```
CUMIPMT(rate, number_of_periods, present_value, first_period, last_period, end_or_beginning)
```
Calculates the cumulative interest over a range of payment periods for an investment.

### CUMPRINC
```
CUMPRINC(rate, number_of_periods, present_value, first_period, last_period, end_or_beginning)
```
Calculates the cumulative principal paid over a range of payment periods for an investment.

### DB
```
DB(cost, salvage, life, period, [month])
```
Calculates the depreciation of an asset for a specified period using the arithmetic declining balance method.

### DDB
```
DDB(cost, salvage, life, period, [factor])
```
Calculates the depreciation of an asset for a specified period using the double-declining balance method.

### DISC
```
DISC(settlement, maturity, price, redemption, [day_count_convention])
```
Calculates the discount rate of a security based on price.

### DOLLARDE
```
DOLLARDE(fractional_price, unit)
```
Converts a price quotation given as a decimal fraction into a decimal value.

### DOLLARFR
```
DOLLARFR(decimal_price, unit)
```
Converts a price quotation given as a decimal value into a decimal fraction.

### DURATION
```
DURATION(settlement, maturity, rate, yield, frequency, [day_count_convention])
```
Calculates the number of compounding periods required for an investment to reach a target value.

### EFFECT
```
EFFECT(nominal_rate, periods_per_year)
```
Calculates the annual effective interest rate.

### FV
```
FV(rate, number_of_periods, payment_amount, [present_value], [end_or_beginning])
```
Calculates the future value of an annuity investment.

### FVSCHEDULE
```
FVSCHEDULE(principal, rate_schedule)
```
Calculates the future value of some principal based on a specified series of interest rates.

### INTRATE
```
INTRATE(buy_date, sell_date, buy_price, sell_price, [day_count_convention])
```
Calculates the effective interest rate generated by an investment.

### IPMT
```
IPMT(rate, period, number_of_periods, present_value, [future_value], [end_or_beginning])
```
Calculates the payment on interest for an investment.

### IRR
```
IRR(cashflow_amounts, [rate_guess])
```
Calculates the internal rate of return on an investment.

### ISPMT
```
ISPMT(rate, period, number_of_periods, present_value)
```
Calculates the interest paid during a particular period of an investment.

### MDURATION
```
MDURATION(set

tlement, maturity, rate, yield, frequency, [day_count_convention])
```
Calculates the modified Macaulay duration of a security.

### MIRR
```
MIRR(cashflow_amounts, financing_rate, reinvestment_return_rate)
```
Calculates the modified internal rate of return on an investment.

### NOMINAL
```
NOMINAL(effective_rate, periods_per_year)
```
Calculates the annual nominal interest rate.

### NPER
```
NPER(rate, payment_amount, present_value, [future_value], [end_or_beginning])
```
Calculates the number of payment periods for an investment.

### NPV
```
NPV(discount, cashflow1, [cashflow2, ...])
```
Calculates the net present value of an investment.

### PDURATION
```
PDURATION(rate, present_value, future_value)
```
Returns the number of periods for an investment to reach a specific value.

### PMT
```
PMT(rate, number_of_periods, present_value, [future_value], [end_or_beginning])
```
Calculates the periodic payment for an annuity investment.

### PPMT
```
PPMT(rate, period, number_of_periods, present_value, [future_value], [end_or_beginning])
```
Calculates the payment on the principal of an investment.

### PRICE
```
PRICE(settlement, maturity, rate, yield, redemption, frequency, [day_count_convention])
```
Calculates the price of a security paying periodic interest.

### PRICEDISC
```
PRICEDISC(settlement, maturity, discount, redemption, [day_count_convention])
```
Calculates the price of a discount security based on expected yield.

### PRICEMAT
```
PRICEMAT(settlement, maturity, issue, rate, yield, [day_count_convention])
```
Calculates the price of a security paying interest at maturity.

### PV
```
PV(rate, number_of_periods, payment_amount, [future_value], [end_or_beginning])
```
Calculates the present value of an annuity investment.

### RATE
```
RATE(number_of_periods, payment_per_period, present_value, [future_value], [end_or_beginning], [rate_guess])
```
Calculates the interest rate of an annuity investment.

### RECEIVED
```
RECEIVED(settlement, maturity, investment, discount, [day_count_convention])
```
Calculates the amount received at maturity for a fixed-income security.

### RRI
```
RRI(number_of_periods, present_value, future_value)
```
Returns the interest rate needed for an investment to reach a specific value.

### SLN
```
SLN(cost, salvage, life)
```
Calculates the straight-line depreciation of an asset.

### SYD
```
SYD(cost, salvage, life, period)
```
Calculates the sum of years digits depreciation of an asset.

### TBILLEQ
```
TBILLEQ(settlement, maturity, discount)
```
Calculates the equivalent annualized rate of return of a US Treasury Bill.

### TBILLPRICE
```
TBILLPRICE(settlement, maturity, discount)
```
Calculates the price of a US Treasury Bill based on discount rate.

### TBILLYIELD
```
TBILLYIELD(settlement, maturity, price)
```
Calculates the yield of a US Treasury Bill based on price.

### VDB
```
VDB(cost, salvage, life, start_period, end_period, [factor], [no_switch])
```
Returns the depreciation of an asset for a specified period.

### XIRR
```
XIRR(cashflow_amounts, cashflow_dates, [rate_guess])
```
Calculates the internal rate of return for a series of cash flows occurring at irregular intervals.

### XNPV
```
XNPV(discount, cashflow_amounts, cashflow_dates)
```
Calculates the net present value for a series of cash flows occurring at irregular intervals.

### YIELD
```
YIELD(settlement, maturity, rate, price, redemption, frequency, [day_count_convention])
```
Calculates the annual yield of a security paying periodic interest.

### YIELDDISC
```
YIELDDISC(settlement, maturity, price, redemption, [day_count_convention])
```
Calculates the annual yield of a discount security based on price.

### YIELDMAT
```
YIELDMAT(settlement, maturity, issue, rate, price, [day_count_convention])
```
Calculates the annual yield of a security paying interest at maturity.


Here's the markdown format for the provided table section related to Google functions:

## Google

### ARRAYFORMULA
```
ARRAYFORMULA(array_formula)
```
Enables the display of values returned from an array formula into multiple rows and/or columns and the use of non-array functions with arrays.

### DETECTLANGUAGE
```
DETECTLANGUAGE(text_or_range)
```
Identifies the language used in text within the specified range.

### GOOGLEFINANCE
```
GOOGLEFINANCE(ticker, [attribute], [start_date], [end_date|num_days], [interval])
```
Fetches current or historical securities information from Google Finance.

### GOOGLETRANSLATE
```
GOOGLETRANSLATE(text, [source_language], [target_language])
```
Translates text from one language into another.

### IMAGE
```
IMAGE(url, [mode], [height], [width])
```
Inserts an image into a cell.

### QUERY
```
QUERY(data, query, [headers])
```
Runs a Google Visualization API Query Language query across data.

### SPARKLINE
```
SPARKLINE(data, [options])
```
Creates a miniature chart contained within a single cell.

Here's the markdown format for the provided table section related to Info functions:

## Info

### ERROR.TYPE
```
ERROR.TYPE(reference)
```
Returns a number corresponding to the error value in a different cell.

### ISBLANK
```
ISBLANK(value)
```
Checks whether the referenced cell is empty.

### ISDATE
```
ISDATE(value)
```
Returns whether a value is a date.

### ISEMAIL
```
ISEMAIL(value)
```
Checks whether a value is a valid email address.

### ISERR
```
ISERR(value)
```
Checks whether a value is an error other than `#N/A`.

### ISERROR
```
ISERROR(value)
```
Checks whether a value is an error.

### ISFORMULA
```
ISFORMULA(cell)
```
Checks whether a formula is in the referenced cell.

### ISLOGICAL
```
ISLOGICAL(value)
```
Checks whether a value is `TRUE` or `FALSE`.

### ISNA
```
ISNA(value)
```
Checks whether a value is the error `#N/A`.

### ISNONTEXT
```
ISNONTEXT(value)
```
Checks whether a value is non-textual.

### ISNUMBER
```
ISNUMBER(value)
```
Checks whether a value is a number.

### ISREF
```
ISREF(value)
```
Checks whether a value is a valid cell reference.

### ISTEXT
```
ISTEXT(value)
```
Checks whether a value is text.

### N
```
N(value)
```
Returns the argument provided as a number.

### NA
```
NA()
```
Returns the "value not available" error, `#N/A`.

### TYPE
```
TYPE(value)
```
Returns a number associated with the type of data passed into the function.

### CELL
```
CELL(info_type, reference)
```
Returns the requested information about the specified cell.



Here's the markdown format for the provided table section related to Logical functions:

## Logical

### AND
```
AND(logical_expression1, [logical_expression2, ...])
```
Returns true if all of the provided arguments are logically true, and false if any of the provided arguments are logically false.

### FALSE
```
FALSE()
```
Returns the logical value `FALSE`.

### IF
```
IF(logical_expression, value_if_true, value_if_false)
```
Returns one value if a logical expression is `TRUE` and another if it is `FALSE`.

### IFERROR
```
IFERROR(value, [value_if_error])
```
Returns the first argument if it is not an error value, otherwise returns the second argument if present, or a blank if the second argument is absent.

### IFNA
```
IFNA(value, value_if_na)
```
Evaluates a value. If the value is an #N/A error, returns the specified value.

### IFS
```
IFS(condition1, value1, [condition2, value2], …)
```
Evaluates multiple conditions and returns a value that corresponds to the first true condition.

### LAMBDA
```
LAMBDA(name, formula_expression)
```
Creates and returns a custom function with a set of names and a formula_expression that uses them.

### LET
```
LET(name1, value_expression1, [name2, …], [value_expression2, …], formula_expression)
```
Assigns name with the value_expression results and returns the result of the formula_expression.

### NOT
```
NOT(logical_expression)
```
Returns the opposite of a logical value - `NOT(TRUE)` returns `FALSE`; `NOT(FALSE)` returns `TRUE`.

### OR
```
OR(logical_expression1, [logical_expression2, ...])
```
Returns true if any of the provided arguments are logically true, and false if all of the provided arguments are logically false.

### SWITCH
```
SWITCH(expression, case1, value1, [default or case2, value2], …)
```
Tests an expression against a list of cases and returns the corresponding value of the first matching case, with an optional default value if nothing else is met.

### TRUE
```
TRUE()
```
Returns the logical value `TRUE`.

### XOR
```
XOR(logical_expression1, [logical_expression2, ...])
```
Performs an exclusive or of 2 numbers that returns a 1 if the numbers are different, and a 0 otherwise.


Here's the markdown format for the provided table section related to Lookup functions:

## Lookup

### ADDRESS
```
ADDRESS(row, column, [absolute_relative_mode], [use_a1_notation], [sheet])
```
Returns a cell reference as a string.

### CHOOSE
```
CHOOSE(index, choice1, [choice2, ...])
```
Returns an element from a list of choices based on index.

### COLUMN
```
COLUMN([cell_reference])
```
Returns the column number of a specified cell, with `A=1`.

### COLUMNS
```
COLUMNS(range)
```
Returns the number of columns in a specified array or range.

### FORMULATEXT
```
FORMULATEXT(cell)
```
Returns the formula as a string.

### GETPIVOTDATA
```
GETPIVOTDATA(value_name, any_pivot_table_cell, [original_column, ...], [pivot_item, ...])
```
Extracts an aggregated value from a pivot table that corresponds to the specified row and column headings.

### HLOOKUP
```
HLOOKUP(search_key, range, index, [is_sorted])
```
Horizontal lookup. Searches across the first row of a range for a key and returns the value of a specified cell in the column found.

### INDEX
```
INDEX(reference, [row], [column])
```
Returns the content of a cell, specified by row and column offset.

### INDIRECT
```
INDIRECT(cell_reference_as_string, [is_A1_notation])
```
Returns a cell reference specified by a string.

### LOOKUP
```
LOOKUP(search_key, search_range|search_result_array, [result_range])
```
Looks through a row or column for a key and returns the value of the cell in a result range located in the same position as the search row or column.

### MATCH
```
MATCH(search_key, range, [search_type])
```
Returns the relative position of an item in a range that matches a specified value.

### OFFSET
```
OFFSET(cell_reference, offset_rows, offset_columns, [height], [width])
```
Returns a range reference shifted a specified number of rows and columns from a starting cell reference.

### ROW
```
ROW([cell_reference])
```
Returns the row number of a specified cell.

### ROWS
```
ROWS(range)
```
Returns the number of rows in a specified array or range.

### VLOOKUP
```
VLOOKUP(search_key, range, index, [is_sorted])
```
Vertical lookup. Searches down the first column of a range for a key and returns the value of a specified cell in the row found.

### XLOOKUP
```
XLOOKUP(search_key, lookup_range, result_range, missing_value, [match_mode], [search_mode])
```
Returns the values in the result range based on the position where a match was found in the lookup range. If no match is found, it returns the closest match.


Here's the markdown format for the provided table section related to Math functions:

## Math

### ABS
```
ABS(value)
```
Returns the absolute value of a number.

### ACOS
```
ACOS(value)
```
Returns the inverse cosine of a value, in radians.

### ACOSH
```
ACOSH(value)
```
Returns the inverse hyperbolic cosine of a number.

### ACOT
```
ACOT(value)
```
Returns the inverse cotangent of a value, in radians.

### ACOTH
```
ACOTH(value)
```
Returns the inverse hyperbolic cotangent of a value, in radians. Must not be between -1 and 1, inclusive.

### ASIN
```
ASIN(value)
```
Returns the inverse sine of a value, in radians.

### ASINH
```
ASINH(value)
```
Returns the inverse hyperbolic sine of a number.

### ATAN
```
ATAN(value)
```
Returns the inverse tangent of a value, in radians.

### ATAN2
```
ATAN2(x, y)
```
Returns the angle between the x-axis and a line segment from the origin (0,0) to specified coordinate pair (`x`,`y`), in radians.

### ATANH
```
ATANH(value)
```
Returns the inverse hyperbolic tangent of a number.

### BASE
```
BASE(value, base, [min_length])
```
Converts a number into a text representation in another base, for example, base 2 for binary.

### CEILING
```
CEILING(value, [factor])
```
Rounds a number up to the nearest integer multiple of specified significance.

### CEILING.MATH
```
CEILING.MATH(number, [significance], [mode])
```
Rounds a number up to the nearest integer multiple of specified significance, with negative numbers rounding toward or away from 0 depending on the mode.

### CEILING.PRECISE
```
CEILING.PRECISE(number, [significance])
```
Rounds a number up to the nearest integer multiple of specified significance. If the number is positive or negative, it is rounded up.

### COMBIN
```
COMBIN(n, k)
```
Returns the number of ways to choose some number of objects from a pool of a given size of objects.

### COMBINA
```
COMBINA(n, k)
```
Returns the number of ways to choose some number of objects from a pool of a given size of objects, including ways that choose the same object multiple times.

### COS
```
COS(angle)
```
Returns the cosine of an angle provided in radians.

### COSH
```
COSH(value)
```
Returns the hyperbolic cosine of any real number.

### COT
```
COT(angle)
```
Cotangent of an angle provided in radians.

### COTH
```
COTH(value)
```
Returns the hyperbolic cotangent of any real number.

### COUNTBLANK
```
COUNTBLANK(range)
```
Returns the number of empty cells in a given range.

### COUNTIF
```
COUNTIF(range, criterion)
```
Returns a conditional count across a range.

### COUNTIFS
```
COUNTIFS(criteria_range1, criterion1, [criteria_range2, criterion2, ...])
```
Returns the count of a range depending on multiple criteria.

### COUNTUNIQUE
```
COUNTUNIQUE(value1, [value2, ...])
```
Counts the number of unique values in a list of specified values and ranges.

### CSC
```
CSC(angle)
```
Returns the cosecant of an angle provided in radians.

### CSCH
```
CSCH(value)
```
The CSCH function returns the hyperbolic cosecant of any real number.

### DECIMAL
```
DECIMAL(value, base)
```
The DECIMAL function converts the text representation of a number in another base, to base 10 (decimal).

### DEGREES
```
DEGREES(angle)
```
Converts an angle value in radians to degrees.

### ERFC
```
ERFC(z)
```
Returns the complementary Gauss error function of a value.

### ERFC.PRECISE
```
ERFC.PRECISE(z)
```
See ERFC.

### EVEN
```
EVEN(value)
```
Rounds a number up to the nearest even integer.

### EXP
```
EXP(exponent)
```
Returns Euler's number, e (~2.718) raised to a power.

### FACT
```
FACT(value)
```
Returns the factorial of a number.

### FACTDOUBLE
```
FACTDOUBLE(value)
```
Returns the "double factorial" of a number.

### FLOOR
```
FLOOR(value, [factor])
```
Rounds a number down to the nearest integer multiple of specified significance.

### FLOOR

.MATH
```
FLOOR.MATH(number, [significance], [mode])
```
Rounds a number down to the nearest integer multiple of specified significance, with negative numbers rounding toward or away from 0 depending on the mode.

### FLOOR.PRECISE
```
FLOOR.PRECISE(number, [significance])
```
The FLOOR.PRECISE function rounds a number down to the nearest integer or multiple of specified significance.

### GAMMALN
```
GAMMALN(value)
```
Returns the the logarithm of a specified Gamma function, base e (Euler's number).

### GAMMALN.PRECISE
```
GAMMALN.PRECISE(value)
```
See GAMMALN.

### GCD
```
GCD(value1, value2)
```
Returns the greatest common divisor of one or more integers.

### IMLN
```
IMLN(complex_value)
```
Returns the logarithm of a complex number, base e (Euler's number).

### IMPOWER
```
IMPOWER(complex_base, exponent)
```
Returns a complex number raised to a power.

### IMSQRT
```
IMSQRT(complex_number)
```
Computes the square root of a complex number.

### INT
```
INT(value)
```
Rounds a number down to the nearest integer that is less than or equal to it.

### ISEVEN
```
ISEVEN(value)
```
Checks whether the provided value is even.

### ISO.CEILING
```
ISO.CEILING(number, [significance])
```
See CEILING.PRECISE.

### ISODD
```
ISODD(value)
```
Checks whether the provided value is odd.

### LCM
```
LCM(value1, value2)
```
Returns the least common multiple of one or more integers.

### LN
```
LN(value)
```
Returns the the logarithm of a number, base e (Euler's number).

### LOG
```
LOG(value, base)
```
Returns the the logarithm of a number given a base.

### LOG10
```
LOG10(value)
```
Returns the the logarithm of a number, base 10.

### MOD
```
MOD(dividend, divisor)
```
Returns the result of the modulo operator, the remainder after a division operation.

### MROUND
```
MROUND(value, factor)
```
Rounds one number to the nearest integer multiple of another.

### MULTINOMIAL
```
MULTINOMIAL(value1, value2)
```
Returns the factorial of the sum of values divided by the product of the values' factorials.

### MUNIT
```
MUNIT(dimension)
```
Returns a unit matrix of size dimension x dimension.

### ODD
```
ODD(value)
```
Rounds a number up to the nearest odd integer.

### PI
```
PI()
```
Returns the value of Pi to 14 decimal places.

### POWER
```
POWER(base, exponent)
```
Returns a number raised to a power.

### PRODUCT
```
PRODUCT(factor1, [factor2, ...])
```
Returns the result of multiplying a series of numbers together.

### QUOTIENT
```
QUOTIENT(dividend, divisor)
```
Returns one number divided by another.

### RADIANS
```
RADIANS(angle)
```
Converts an angle value in degrees to radians.

### RAND
```
RAND()
```
Returns a random number between 0 inclusive and 1 exclusive.

### RANDARRAY
```
RANDARRAY(rows, columns)
```
Generates an array of random numbers between 0 and 1.

### RANDBETWEEN
```
RANDBETWEEN(low, high)
```
Returns a uniformly random integer between two values, inclusive.

### ROUND
```
ROUND(value, [places])
```
Rounds a number to a certain number of decimal places according to standard rules.

### ROUNDDOWN
```
ROUNDDOWN(value, [places])
```
Rounds a number to a certain number of decimal places, always rounding down to the next valid increment.

### ROUNDUP
```
ROUNDUP(value, [places])
```
Rounds a number to a certain number of decimal places, always rounding up to the next valid increment.

### SEC
```
SEC(angle)
```
The SEC function returns the secant of an angle, measured in radians.

### SECH
```
SECH(value)
```
The SECH function returns the hyperbolic secant of an angle.

### SEQUENCE
```
SEQUENCE(rows, columns, start, step)
```
Returns an array of sequential numbers, such as 1, 2, 3, 4.

### SERIESSUM
```
SERIESSUM(x, n, m, a)
```
Given parameters `x`, `n

`, `m`, and `a`, returns the power series sum `a1x^n + a2x^(n+m) + ... + aix^(n+(i-1)m)`, where `i` is the number of entries in range `a`.

### SIGN
```
SIGN(value)
```
Given an input number, returns `-1` if it is negative, `1` if positive, and `0` if it is zero.

### SIN
```
SIN(angle)
```
Returns the sine of an angle provided in radians.

### SINH
```
SINH(value)
```
Returns the hyperbolic sine of any real number.

### SQRT
```
SQRT(value)
```
Returns the positive square root of a positive number.

### SQRTPI
```
SQRTPI(value)
```
Returns the positive square root of the product of Pi and the given positive number.

### SUBTOTAL
```
SUBTOTAL(function_code, range1, [range2, ...])
```
Returns a subtotal for a vertical range of cells using a specified aggregation function.

### SUM
```
SUM(value1, [value2, ...])
```
Returns the sum of a series of numbers and/or cells.

### SUMIF
```
SUMIF(range, criterion, [sum_range])
```
Returns a conditional sum across a range.

### SUMIFS
```
SUMIFS(sum_range, criteria_range1, criterion1, [criteria_range2, criterion2, ...])
```
Returns the sum of a range depending on multiple criteria.

### SUMSQ
```
SUMSQ(value1, [value2, ...])
```
Returns the sum of the squares of a series of numbers and/or cells.

### TAN
```
TAN(angle)
```
Returns the tangent of an angle provided in radians.

### TANH
```
TANH(value)
```
Returns the hyperbolic tangent of any real number.

### TRUNC
```
TRUNC(value, [places])
```
Truncates a number to a certain number of significant digits by omitting less significant digits.

## Operator
### ADD
```
ADD(value1, value2)
```
Returns the sum of two numbers. Equivalent to the `+` operator.

### CONCAT
```
CONCAT(value1, value2)
```
Returns the concatenation of two values. Equivalent to the `&` operator.

### DIVIDE
```
DIVIDE(dividend, divisor)
```
Returns one number divided by another. Equivalent to the `/` operator.

### EQ
```
EQ(value1, value2)
```
Returns `TRUE` if two specified values are equal and `FALSE` otherwise. Equivalent to the `=` operator.

### GT
```
GT(value1, value2)
```
Returns `TRUE` if the first argument is strictly greater than the second, and `FALSE` otherwise. Equivalent to the `>` operator.

### GTE
```
GTE(value1, value2)
```
Returns `TRUE` if the first argument is greater than or equal to the second, and `FALSE` otherwise. Equivalent to the `>=` operator.

### ISBETWEEN
```
ISBETWEEN(value_to_compare, lower_value, upper_value, lower_value_is_inclusive, upper_value_is_inclusive)
```
Checks whether a provided number is between two other numbers either inclusively or exclusively.

### LT
```
LT(value1, value2)
```
Returns `TRUE` if the first argument is strictly less than the second, and `FALSE` otherwise. Equivalent to the `<` operator.

### LTE
```
LTE(value1, value2)
```
Returns `TRUE` if the first argument is less than or equal to the second, and `FALSE` otherwise. Equivalent to the `<=` operator.

### MINUS
```
MINUS(value1, value2)
```
Returns the difference of two numbers. Equivalent to the `-` operator.

### MULTIPLY
```
MULTIPLY(factor1, factor2)
```
Returns the product of two numbers. Equivalent to the `*` operator.

### NE
```
NE(value1, value2)
```
Returns `TRUE` if two specified values are not equal and `FALSE` otherwise. Equivalent to the `<>` operator.

### POW
```
POW(base, exponent)
```
Returns a number raised to a power.

### UMINUS
```
UMINUS(value)
```
Returns a number with the sign reversed.

### UNARY_PERCENT
```
UNARY_PERCENT(percentage)
```
Returns a value interpreted as a percentage; that is, `UNARY_PERCENT(100)` equals `1`.

### UNIQUE
```
UNIQUE(range, by_column, exactly_once)
```
Returns unique rows in the provided source range, discarding duplicates. Rows are returned in the order in which they first appear in the source range.

### UPLUS
```
UPLUS(value)
```
Returns a specified number, unchanged.


## PARSER
### CONVERT
```
CONVERT(value, start_unit, end_unit)
```
Converts a numeric value to a different unit of measure.

### TO_DATE
```
TO_DATE(value)
```
Converts a provided number to a date.

### TO_DOLLARS
```
TO_DOLLARS(value)
```
Converts a provided number to a dollar value.

### TO_PERCENT
```
TO_PERCENT(value)
```
Converts a provided number to a percentage.

### TO_PURE_NUMBER
```
TO_PURE_NUMBER(value)
```
Converts a provided date/time, percentage, currency or other formatted numeric value to a pure number without formatting.

### TO_TEXT
```
TO_TEXT(value)
```
Converts a provided numeric value to a text value.

## STATISTICAL
### AVEDEV
```
AVEDEV(value1, [value2, ...])
```
Calculates the average of the magnitudes of deviations of data from a dataset's mean.

### AVERAGE
```
AVERAGE(value1, [value2, ...])
```
Returns the numerical average value in a dataset, ignoring text.

### AVERAGE.WEIGHTED
```
AVERAGE.WEIGHTED(values, weights, [additional values], [additional weights])
```
Finds the weighted average of a set of values, given the values and the corresponding weights.

### AVERAGEA
```
AVERAGEA(value1, [value2, ...])
```
Returns the numerical average value in a dataset.

### AVERAGEIF
```
AVERAGEIF(criteria_range, criterion, [average_range])
```
Returns the average of a range depending on criteria.

### AVERAGEIFS
```
AVERAGEIFS(average_range, criteria_range1, criterion1, [criteria_range2, criterion2, ...])
```
Returns the average of a range depending on multiple criteria.

### BETA.DIST
```
BETA.DIST(value, alpha, beta, cumulative, lower_bound, upper_bound)
```
Returns the probability of a given value as defined by the beta distribution function.

### BETA.INV
```
BETA.INV(probability, alpha, beta, lower_bound, upper_bound)
```
Returns the value of the inverse beta distribution function for a given probability.

### BETADIST
```
BETADIST(value, alpha, beta, lower_bound, upper_bound)
```
See BETA.DIST.

### BETAINV
```
BETAINV(probability, alpha, beta, lower_bound, upper_bound)
```
See BETA.INV.

### BINOM.DIST
```
BINOM.DIST(num_successes, num_trials, prob_success, cumulative)
```
See BINOMDIST.

### BINOM.INV
```
BINOM.INV(num_trials, prob_success, target_prob)
```
See CRITBINOM.

### BINOMDIST
```
BINOMDIST(num_successes, num_trials, prob_success, cumulative)
```
Calculates the probability of drawing a certain number of successes (or a maximum number of successes) in a certain number of tries given a population of a certain size containing a certain number of successes, with replacement of draws.

### CHIDIST
```
CHIDIST(x, degrees_freedom)
```
Calculates the right-tailed chi-squared distribution, often used in hypothesis testing.

### CHIINV
```
CHIINV(probability, degrees_freedom)
```
Calculates the inverse of the right-tailed chi-squared distribution.

### CHISQ.DIST
```
CHISQ.DIST(x, degrees_freedom, cumulative)
```
Calculates the left-tailed chi-squared distribution, often used in hypothesis testing.

### CHISQ.DIST.RT
```
CHISQ.DIST.RT(x, degrees_freedom)
```
Calculates the right-tailed chi-squared distribution, which is commonly used in hypothesis testing.

### CHISQ.INV
```
CHISQ.INV(probability, degrees_freedom)
```
Calculates the inverse of the left-tailed chi-squared distribution.

### CHISQ.INV.RT
```
CHISQ.INV.RT(probability, degrees_freedom)
```
Calculates the inverse of the right-tailed chi-squared distribution.

### CHISQ.TEST
```
CHISQ.TEST(observed_range, expected_range)
```
See CHITEST.

### CHITEST
```
CHITEST(observed_range, expected_range)
```
Returns the probability associated with a Pearson’s chi-squared test on the two ranges of data. Determines the likelihood that the observed categorical data is drawn from an expected distribution.

### CONFIDENCE
```
CONFIDENCE(alpha, standard_deviation, pop_size)
```
See CONFIDENCE.NORM.

### CONFIDENCE.NORM
```
CONFIDENCE.NORM(alpha, standard_deviation, pop_size)
```
Calculates the width of half the confidence interval for a normal distribution.

### CONFIDENCE.T
```
CONFIDENCE.T(alpha, standard_deviation, size)
```
Calculates the width of half the confidence interval for a Student’s t-distribution.

### CORREL
```
CORREL(data_y, data_x)
```
Calculates r, the Pearson product-moment correlation coefficient of a dataset.

### COUNT
```
COUNT(value1, [value2, ...])
```
Returns a count of the number of numeric values in a dataset.

### COUNTA
```
COUNTA(value1, [value2, ...])
```
Returns a count of the number of values in a dataset.

### COVAR
```
COVAR(data_y, data_x

)
```
Calculates the covariance of a dataset.

### COVARIANCE.P
```
COVARIANCE.P(data_y, data_x)
```
See COVAR.

### COVARIANCE.S
```
COVARIANCE.S(data_y, data_x)
```
Calculates the covariance of a dataset, where the dataset is a sample of the total population.

### CRITBINOM
```
CRITBINOM(num_trials, prob_success, target_prob)
```
Calculates the smallest value for which the cumulative binomial distribution is greater than or equal to a specified criteria.

### DEVSQ
```
DEVSQ(value1, value2)
```
Calculates the sum of squares of deviations based on a sample.

### EXPON.DIST
```
EXPON.DIST(x, LAMBDA, cumulative)
```
Returns the value of the exponential distribution function with a specified LAMBDA at a specified value.

### EXPONDIST
```
EXPONDIST(x, LAMBDA, cumulative)
```
See EXPON.DIST.

### F.DIST
```
F.DIST(x, degrees_freedom1, degrees_freedom2, cumulative)
```
Calculates the left-tailed F probability distribution (degree of diversity) for two data sets with given input x. Alternately called Fisher-Snedecor distribution or Snedecor's F distribution.

### F.DIST.RT
```
F.DIST.RT(x, degrees_freedom1, degrees_freedom2)
```
Calculates the right-tailed F probability distribution (degree of diversity) for two data sets with given input x. Alternately called Fisher-Snedecor distribution or Snedecor's F distribution.

### F.INV
```
F.INV(probability, degrees_freedom1, degrees_freedom2)
```
Calculates the inverse of the left-tailed F probability distribution. Also called the Fisher-Snedecor distribution or Snedecor’s F distribution.

### F.INV.RT
```
F.INV.RT(probability, degrees_freedom1, degrees_freedom2)
```
Calculates the inverse of the right-tailed F probability distribution. Also called the Fisher-Snedecor distribution or Snedecor’s F distribution.

### F.TEST
```
F.TEST(range1, range2)
```
See FTEST.

### FDIST
```
FDIST(x, degrees_freedom1, degrees_freedom2)
```
See F.DIST.RT.

### FINV
```
FINV(probability, degrees_freedom1, degrees_freedom2)
```
See F.INV.RT.

### FISHER
```
FISHER(value)
```
Returns the Fisher transformation of a specified value.

### FISHERINV
```
FISHERINV(value)
```
Returns the inverse Fisher transformation of a specified value.

### FORECAST
```
FORECAST(x, data_y, data_x)
```
Calculates the expected y-value for a specified x based on a linear regression of a dataset.

### FORECAST.LINEAR
```
FORECAST.LINEAR(x, data_y, data_x)
```
See FORECAST.

### FTEST
```
FTEST(range1, range2)
```
Returns the probability associated with an F-test for equality of variances. Determines whether two samples are likely to have come from populations with the same variance.

### GAMMA
```
GAMMA(number)
```
Returns the Gamma function evaluated at the specified value.

### GAMMA.DIST
```
GAMMA.DIST(x, alpha, beta, cumulative)
```
Calculates the gamma distribution, a two-parameter continuous probability distribution.

### GAMMA.INV
```
GAMMA.INV(probability, alpha, beta)
```
The GAMMA.INV function returns the value of the inverse gamma cumulative distribution function for the specified probability and alpha and beta parameters.

### GAMMADIST
```
GAMMADIST(x, alpha, beta, cumulative)
```
See GAMMA.DIST.

### GAMMAINV
```
GAMMAINV(probability, alpha, beta)
```
See GAMMA.INV.

### GAUSS
```
GAUSS(z)
```
The GAUSS function returns the probability that a random variable, drawn from a normal distribution, will be between the mean and z standard deviations above (or below) the mean.

### GEOMEAN
```
GEOMEAN(value1, value2)
```
Calculates the geometric mean of a dataset.

### HARMEAN
```
HARMEAN(value1, value2)
```
Calculates the harmonic mean of a dataset.

### HYPGEOM.DIST
```
HYPGEOM.DIST(num_successes, num_draws, successes_in_pop, pop_size)
```
See HYPGEOMDIST.

### HYPGEOMDIST


```
HYPGEOMDIST(num_successes, num_draws, successes_in_pop, pop_size)
```
Calculates the probability of drawing a certain number of successes in a certain number of tries given a population of a certain size containing a certain number of successes, without replacement of draws.

### INTERCEPT
```
INTERCEPT(data_y, data_x)
```
Calculates the y-value at which the line resulting from linear regression of a dataset will intersect the y-axis (x=0).

### KURT
```
KURT(value1, value2)
```
Calculates the kurtosis of a dataset, which describes the shape, and in particular the "peakedness" of that dataset.

### LARGE
```
LARGE(data, n)
```
Returns the nth largest element from a data set, where n is user-defined.

### LOGINV
```
LOGINV(x, mean, standard_deviation)
```
Returns the value of the inverse log-normal cumulative distribution with given mean and standard deviation at a specified value.

### LOGNORM.DIST
```
LOGNORM.DIST(x, mean, standard_deviation)
```
See LOGNORMDIST.

### LOGNORM.INV
```
LOGNORM.INV(x, mean, standard_deviation)
```
See LOGINV.

### LOGNORMDIST
```
LOGNORMDIST(x, mean, standard_deviation)
```
Returns the value of the log-normal cumulative distribution with given mean and standard deviation at a specified value.

### MARGINOFERROR
```
MARGINOFERROR(range, confidence)
```
Calculates the amount of random sampling error given a range of values and a confidence level.

### MAX
```
MAX(value1, [value2, ...])
```
Returns the maximum value in a numeric dataset.

### MAXA
```
MAXA(value1, value2)
```
Returns the maximum numeric value in a dataset.

### MAXIFS
```
MAXIFS(range, criteria_range1, criterion1, [criteria_range2, criterion2], …)
```
Returns the maximum value in a range of cells, filtered by a set of criteria.

### MEDIAN
```
MEDIAN(value1, [value2, ...])
```
Returns the median value in a numeric dataset.

### MIN
```
MIN(value1, [value2, ...])
```
Returns the minimum value in a numeric dataset.

### MINA
```
MINA(value1, value2)
```
Returns the minimum numeric value in a dataset.

### MINIFS
```
MINIFS(range, criteria_range1, criterion1, [criteria_range2, criterion2], …)
```
Returns the minimum value in a range of cells, filtered by a set of criteria.

### MODE
```
MODE(value1, [value2, ...])
```
Returns the most commonly occurring value in a dataset.

### MODE.MULT
```
MODE.MULT(value1, value2)
```
Returns the most commonly occurring values in a dataset.

### MODE.SNGL
```
MODE.SNGL(value1, [value2, ...])
```
See MODE.

### NEGBINOM.DIST
```
NEGBINOM.DIST(num_failures, num_successes, prob_success)
```
See NEGBINOMDIST.

### NEGBINOMDIST
```
NEGBINOMDIST(num_failures, num_successes, prob_success)
```
Calculates the probability of drawing a certain number of failures before a certain number of successes given a probability of success in independent trials.

### NORM.DIST
```
NORM.DIST(x, mean, standard_deviation, cumulative)
```
See NORMDIST.

### NORM.INV
```
NORM.INV(x, mean, standard_deviation)
```
See NORMINV.

### NORM.S.DIST
```
NORM.S.DIST(x)
```
See NORMSDIST.

### NORM.S.INV
```
NORM.S.INV(x)
```
See NORMSINV.

### NORMDIST
```
NORMDIST(x, mean, standard_deviation, cumulative)
```
Returns the value of the normal distribution function (or normal cumulative distribution function) for a specified value, mean, and standard deviation.

### NORMINV
```
NORMINV(x, mean, standard_deviation)
```
Returns the value of the inverse normal distribution function for a specified value, mean, and standard deviation.

### NORMSDIST
```
NORMSDIST(x)
```
Returns the value of the standard normal cumulative distribution function for a specified value.

### NORMSINV
```
NORMSINV(x)
```
Returns the value of the inverse standard normal distribution function for a specified value.

### PEARSON
```
PEARSON(data_y, data_x)
```
Calculates r, the Pearson product-moment correlation coefficient of a

 dataset.

### PERCENTILE
```
PERCENTILE(data, percentile)
```
Returns the value at a given percentile of a dataset.

### PERCENTILE.EXC
```
PERCENTILE.EXC(data, percentile)
```
Returns the value at a given percentile of a dataset, exclusive of 0 and 1.

### PERCENTILE.INC
```
PERCENTILE.INC(data, percentile)
```
See PERCENTILE.

### PERCENTRANK
```
PERCENTRANK(data, value, [significant_digits])
```
Returns the percentage rank (percentile) of a specified value in a dataset.

### PERCENTRANK.EXC
```
PERCENTRANK.EXC(data, value, [significant_digits])
```
Returns the percentage rank (percentile) from 0 to 1 exclusive of a specified value in a dataset.

### PERCENTRANK.INC
```
PERCENTRANK.INC(data, value, [significant_digits])
```
Returns the percentage rank (percentile) from 0 to 1 inclusive of a specified value in a dataset.

### PERMUTATIONA
```
PERMUTATIONA(number, number_chosen)
```
Returns the number of permutations for selecting a group of objects (with replacement) from a total number of objects.

### PERMUT
```
PERMUT(n, k)
```
Returns the number of ways to choose some number of objects from a pool of a given size of objects, considering order.

### PHI
```
PHI(x)
```
The PHI function returns the value of the normal distribution with mean 0 and standard deviation 1.

### POISSON
```
POISSON(x, mean, cumulative)
```
See POISSON.DIST.

### POISSON.DIST
```
POISSON.DIST(x, mean, [cumulative])
```
Returns the value of the Poisson distribution function (or Poisson cumulative distribution function) for a specified value and mean.

### PROB
```
PROB(data, probabilities, low_limit, [high_limit])
```
Given a set of values and corresponding probabilities, calculates the probability that a value chosen at random falls between two limits.

### QUARTILE
```
QUARTILE(data, quartile_number)
```
Returns a value nearest to a specified quartile of a dataset.

### QUARTILE.EXC
```
QUARTILE.EXC(data, quartile_number)
```
Returns value nearest to a given quartile of a dataset, exclusive of 0 and 4.

### QUARTILE.INC
```
QUARTILE.INC(data, quartile_number)
```
See QUARTILE.

### RANK
```
RANK(value, data, [is_ascending])
```
Returns the rank of a specified value in a dataset.

### RANK.AVG
```
RANK.AVG(value, data, [is_ascending])
```
Returns the rank of a specified value in a dataset. If there is more than one entry of the same value in the dataset, the average rank of the entries will be returned.

### RANK.EQ
```
RANK.EQ(value, data, [is_ascending])
```
Returns the rank of a specified value in a dataset. If there is more than one entry of the same value in the dataset, the top rank of the entries will be returned.

### RSQ
```
RSQ(data_y, data_x)
```
Calculates the square of r, the Pearson product-moment correlation coefficient of a dataset.

### SKEW
```
SKEW(value1, value2)
```
Calculates the skewness of a dataset, which describes the symmetry of that dataset about the mean.

### SKEW.P
```
SKEW.P(value1, value2)
```
Calculates the skewness of a dataset that represents the entire population.

### SLOPE
```
SLOPE(data_y, data_x)
```
Calculates the slope of the line resulting from linear regression of a dataset.

### SMALL
```
SMALL(data, n)
```
Returns the nth smallest element from a data set, where n is user-defined.

### STANDARDIZE
```
STANDARDIZE(value, mean, standard_deviation)
```
Calculates the normalized equivalent of a random variable given mean and standard deviation of the distribution.

### STDEV
```
STDEV(value1, [value2, ...])
```
Calculates the standard deviation based on a sample.

### STDEV.P
```
STDEV.P(value1, [value2, ...])
```
See STDEVP.

### STDEV.S
```
STDEV.S(value1, [value2, ...])
```
See STDEV.

### STDEVA
```
STDEVA(value1, value2)
```
Calculates the standard deviation based on a sample, setting text

 to the value `0`.

### STDEVP
```
STDEVP(value1, value2)
```
Calculates the standard deviation based on an entire population.

### STDEVPA
```
STDEVPA(value1, value2)
```
Calculates the standard deviation based on an entire population, setting text to the value `0`.

### STEYX
```
STEYX(data_y, data_x)
```
Calculates the standard error of the predicted y-value for each x in the regression of a dataset.

### T.DIST
```
T.DIST(x, degrees_freedom, cumulative)
```
Returns the right tailed Student distribution for a value x.

### T.DIST.2T
```
T.DIST.2T(x, degrees_freedom)
```
Returns the two tailed Student distribution for a value x.

### T.DIST.RT
```
T.DIST.RT(x, degrees_freedom)
```
Returns the right tailed Student distribution for a value x.

### T.INV
```
T.INV(probability, degrees_freedom)
```
Calculates the negative inverse of the one-tailed TDIST function.

### T.INV.2T
```
T.INV.2T(probability, degrees_freedom)
```
Calculates the inverse of the two-tailed TDIST function.

### T.TEST
```
T.TEST(range1, range2, tails, type)
```
Returns the probability associated with Student's t-test. Determines whether two samples are likely to have come from the same two underlying populations that have the same mean.

### TDIST
```
TDIST(x, degrees_freedom, tails)
```
Calculates the probability for Student's t-distribution with a given input (x).

### TINV
```
TINV(probability, degrees_freedom)
```
See T.INV.2T.

### TRIMMEAN
```
TRIMMEAN(data, exclude_proportion)
```
Calculates the mean of a dataset excluding some proportion of data from the high and low ends of the dataset.

### TTEST
```
TTEST(range1, range2, tails, type)
```
See T.TEST.

### VAR
```
VAR(value1, [value2, ...])
```
Calculates the variance based on a sample.

### VAR.P
```
VAR.P(value1, [value2, ...])
```
See VARP.

### VAR.S
```
VAR.S(value1, [value2, ...])
```
See VAR.

### VARA
```
VARA(value1, value2)
```
Calculates an estimate of variance based on a sample, setting text to the value `0`.

### VARP
```
VARP(value1, value2)
```
Calculates the variance based on an entire population.

### VARPA
```
VARPA(value1, value2,...)
```
Calculates the variance based on an entire population, setting text to the value `0`.

### WEIBULL
```
WEIBULL(x, shape, scale, cumulative)
```
Returns the value of the Weibull distribution function (or Weibull cumulative distribution function) for a specified shape and scale.

### WEIBULL.DIST
```
WEIBULL.DIST(x, shape, scale, cumulative)
```
See WEIBULL.

### Z.TEST
```
Z.TEST(data, value, [standard_deviation])
```
Returns the one-tailed P-value of a Z-test with standard distribution.

### ZTEST
```
ZTEST(data, value, [standard_deviation])
```
See Z.TEST.

## TEXT
### ARABIC
```
ARABIC(roman_numeral)
```
Computes the value of a Roman numeral.

### ASC
```
ASC(text)
```
Converts full-width ASCII and katakana characters to their half-width counterparts. All standard-width characters will remain unchanged.

### CHAR
```
CHAR(table_number)
```
Convert a number into a character according to the current Unicode table.

### CLEAN
```
CLEAN(text)
```
Returns the text with the non-printable ASCII characters removed.

### CODE
```
CODE(string)
```
Returns the numeric Unicode map value of the first character in the string provided.

### CONCATENATE
```
CONCATENATE(string1, [string2, ...])
```
Appends strings to one another.

### DOLLAR
```
DOLLAR(number, [number_of_places])
```
Formats a number into the locale-specific currency format.

### EXACT
```
EXACT(string1, string2)
```
Tests whether two strings are identical.

### FIND
```
FIND(search_for, text_to_search, [starting_at])
```
Returns the position at which a string is first found within text.

### FINDB
```
FINDB(search_for, text_to_search, [starting_at])
```
Returns the position at which a string is first found within text counting each double-character as 2.

### FIXED
```
FIXED(number, [number_of_places], [suppress_separator])
```
Formats a number with a fixed number of decimal places.

### JOIN
```
JOIN(delimiter, value_or_array1, [value_or_array2, ...])
```
Concatenates the elements of one or more one-dimensional arrays using a specified delimiter.

### LEFT
```
LEFT(string, [number_of_characters])
```
Returns a substring from the beginning of a specified string.

### LEFTB
```
LEFTB(string, num_of_bytes)
```
Returns the left portion of a string up to a certain number of bytes.

### LEN
```
LEN(text)
```
Returns the length of a string.

### LENB
```
LENB(string)
```
Returns the length of a string in bytes.

### LOWER
```
LOWER(text)
```
Converts a specified string to lowercase.

### MID
```
MID(string, starting_at, extract_length)
```
Returns a segment of a string.

### MIDB
```
MIDB(string)
```
Returns a section of a string starting at a given character and up to a specified number of bytes.

### PROPER
```
PROPER(text_to_capitalize)
```
Capitalizes each word in a specified string.

### REGEXEXTRACT
```
REGEXEXTRACT(text, regular_expression)
```
Extracts matching substrings according to a regular expression.

### REGEXMATCH
```
REGEXMATCH(text, regular_expression)
```
Determines whether a piece of text matches a regular expression.

### REGEXREPLACE
```
REGEXREPLACE(text, regular_expression, replacement)
```
Replaces part of a text string with a different text string using regular expressions.

### REPLACE
```
REPLACE(text, position, length, new_text)
```
Replaces part of a text string with a different text string.

### REPLACEB
```
REPLACEB(text, position, num_bytes, new_text)
```
Replaces part of a text string, based on a number of bytes, with a different text string.

### REPT
```
REPT(text_to_repeat, number_of_repetitions)
```
Returns specified text repeated a number of times.

### RIGHT
```
RIGHT(string, [number_of_characters])
```
Returns a substring from the end of a specified string.

### RIGHTB
```
RIGHTB(string, num_of_bytes)
```
Returns the right portion of a string up to a certain number of bytes.

### ROMAN
```
ROMAN(number, [rule_relaxation])
```
Formats a number in Roman numerals.

### SEARCH
```
SEARCH(search_for, text_to_search, [starting_at])
```
Returns the position at which a string is first found within text.

### SEARCHB
```
SEARCHB(search_for, text_to_search, [starting_at])
```
Returns the position at which a string is first found within text counting each double-character as 2.

### SPLIT
```
SPLIT(text, delimiter, [split_by_each], [remove_empty_text])
```
Divides text around a specified character or string, and puts each fragment into a separate cell in the row.

### SUBSTITUTE
```
SUBSTITUTE(text_to_search, search_for, replace_with, [occurrence_number])
```
Replaces existing text with new text in a string.

### T
```
T(value)
```
Returns string arguments as text.

### TEXT
```
TEXT(number, format)
```
Converts a number into text according

 to a specified format.

### TEXTJOIN
```
TEXTJOIN(delimiter, ignore_empty, text1, [text2], …)
```
Combines the text from multiple strings and/or arrays, with a specifiable delimiter separating the different texts.

### TRIM
```
TRIM(text)
```
Removes leading and trailing spaces in a specified string.

### UNICHAR
```
UNICHAR(number)
```
Returns the Unicode character for a number.

### UNICODE
```
UNICODE(text)
```
Returns the decimal Unicode value of the first character of the text.

### UPPER
```
UPPER(text)
```
Converts a specified string to uppercase.

### VALUE
```
VALUE(text)
```
Converts a string in any of the date, time, or number formats that Google Sheets understands into a number.

## WEB
### ENCODEURL
```
ENCODEURL(text)
```
Encodes a string of text for the purpose of using in a URL query.

### HYPERLINK
```
HYPERLINK(url, [link_label])
```
Creates a hyperlink inside a cell.

### IMPORTDATA
```
IMPORTDATA(url)
```
Imports data at a given URL in .csv (comma-separated value) or .tsv (tab-separated value) format.

### IMPORTFEED
```
IMPORTFEED(url, [query], [headers], [num_items])
```
Imports an RSS or ATOM feed.

### IMPORTHTML
```
IMPORTHTML(url, query, index)
```
Imports data from a table or list within an HTML page.

### IMPORTRANGE
```
IMPORTRANGE(spreadsheet_url, range_string)
```
Imports a range of cells from a specified spreadsheet.

### IMPORTXML
```
IMPORTXML(url, xpath_query)
```
Imports data from any of various structured data types including XML, HTML, CSV, TSV, and RSS and ATOM XML feeds.

### ISURL
```
ISURL(value)
```
Checks whether a value is a valid URL.
