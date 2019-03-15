

**POST- Add Customers**

This endpoint allows you to add customers.

````http://5.133.176.54:82/api/v1.0/Customer/MasterAdd````

```Request

Headers

 authorisation           string                JWT Token
 REQUIRED

Body Parameters

 emailid            string                Email ID of Customer
 REQUIRED

 designationid      string                Designation
 REQUIRED

 mobileno           number                Mobile Number
 REQUIRED

 lastname           string                Last Name
 REQUIRED

 firstname          string                First Name
 REQUIRED

 noofemp            number                Number of Employees
 OPTIONAL

 annturnover        number                Turn over of Company
 OPTIONAL

 currencyid         string                Currency of Country
 OPTIONAL

 website            string                Website Name
 OPTIONAL

 inccountryid       string                Country ID
 REQUIRED

 telno              number                Contact Number
 REQUIRED

 busactivity        string                Business Activity
 OPTIONAL

 incdate            string                Incorporation Date
 REQUIRED

 licauth            string                License Authority Name 
 REQUIRED

 licexpdate         string                Expiration date of license
 REQUIRED

 licno              string                License number
 OPTIONAL

 name               string                Name of customer as on trade license
 OPTIONAL

 Companytypeid      integar               Type of Company 
 OPTIONAL

 customertypeid     integar               Type of Customer
 OPTIONAL

```

```Response

200: OK
{
    "success": true,
    "token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpYXQiOjE1NDk1MzEzNTIsImV4cCI6MTU0OTYxNzc1Mn0.6cTXghU1IdDreucri4nQKK-Q2HjnHgL7CtTKmvYTRzo"
}


403: Forbidden
{
    "success": false,
    "message": "403 - Invalid API secret key."
}

```


**POST- Other Details of Customer**

This endpoint allows us to add more details of Customer.

````http://5.133.176.54:82/api/v1.0/Customer/DetailsAdd````

```Request

Headers

 authorisation           string                JWT Token
 REQUIRED

Body Parameters

 tempcustomerid     number                Customer ID
 REQUIRED

 name               string                Customer Name
 REQUIRED

 countryid          string                Country Code
 REQUIRED

 website            string                Website Name
 OPTIONAL

 currencyid         string                Currency of Country
 OPTIONAL

 annsales           number                Annual Sale Volume
 OPTIONAL

 commterms          string                Commercial Terms
 REQUIRED

 firstname          string                First Name
 REQUIRED

 lastname           string                Last Name
 REQUIRED

 designationid      string                Designation of Customer
 REQUIRED

 otherdesignation   string                Other Designation
 REQUIRED

 mobileno           number                Mobile Number
 REQUIRED

 emailid            string                Email ID of Customer
 REQUIRED

 otherindustry      string                Other Industry Details
 OPTIONAL

 othercommterms     string                Other Commercials Terms
 REQUIRED
```

```Response

200: OK
{
    "success": true,
    "token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpYXQiOjE1NDk1MzEzNTIsImV4cCI6MTU0OTYxNzc1Mn0.6cTXghU1IdDreucri4nQKK-Q2HjnHgL7CtTKmvYTRzo"
}


403: Forbidden
{
    "success": false,
    "message": "403 - Invalid API secret key."
}

```



**GET- Customer Details**

Get all the Details of the Customer.

````http://5.133.176.54:82/api/v1.0/Customer/MasterListAll/0````

```Request

Headers

 authorisation           string                JWT Token
 REQUIRED

```

```Response

200: OK

{
        "tempcustomerid": 1,

        "uniquekey": "IND00000000000000001",

        "name": "XYZ",
        "customertypeid": 1,

        "companytypeid": 4,

        "othercompanytype": "",

        "licno": "rwetre",

        "licexpdate": "2019-02-11T18:30:00.000Z",

        "licauth": "fddg",

        "inccountryid": 101,

        "incdate": "2019-02-01T18:30:00.000Z",

        "busactivity": "test",

        "telno": "+213345345",

        "website": "test.com",

        "currencyid": 2,

        "annturnover": 34535,

        "noofemp": "434",

        "firstname": "test",

        "lastname": "test",
        "mobileno": "+971435353",

        "designationid": 17,

        "otherdesignation": "",
        "emailid": "test@test.com",

        "status": "RR",

        "createdate": "2019-02-04T21:58:19.560Z",

        "createip": "::ffff:5.133.176.54"
}

```


**GET- Company Type List**

Get Company Type List.

````http://5.133.176.54:82/api/v1.0/Common/CompanyTypeList/0````

```Request

Headers

 authorisation           string                JWT Token
 REQUIRED

```

```Response

200: OK

{
        "companytypeid": 4,

        "companytypename": "General Partnership",

        "isactive": true,

        "createby": 1,

        "createdate": "2018-12-19T14:19:15.190Z",

        "createip": "192.168.1.1",

        "updateby": 1,

        "updatedate": "2018-12-19T14:19:15.190Z",

        "updateip": "192.168.1.1"
}

```


**GET- Country List**

Get Country List.

````http://5.133.176.54:82/api/v1.0/Common/CountryList/0````

```Request

Headers

 authorisation           string                JWT Token
 REQUIRED

```

```Response

200: OK

{
        "countryid": 13,

        "countrycode": "AUS",

        "countryname": "Australia",

        "isactive": true,

        "createby": 1,

        "createdate": "2018-12-19T14:24:39.050Z",

        "createip": "192.168.1.1",

        "updateby": 1,

        "updatedate": "2018-12-19T14:24:39.050Z",

        "updateip": "192.168.1.1"
}

```

**GET- Currency List**

Get Currency List.

````http://5.133.176.54:82/api/v1.0/Common/CurrencyList/0````

```Request

Headers

 authorisation           string                JWT Token
 REQUIRED

```

```Response

200: OK

{
        "countryid": 11,

        "countrycode": "EUR",

        "countryname": "EURO",

        "isactive": true,

        "createby": 1,

        "createdate": "2018-12-19T14:24:39.050Z",

        "createip": "192.168.1.1",

        "updateby": 1,

        "updatedate": "2018-12-19T14:24:39.050Z",

        "updateip": "192.168.1.1"
}

```


**GET- Customer Type List**

Get Customer Type List.

````http://5.133.176.54:82/api/v1.0/Common/CustomerTypeList/0````

```Request

Headers

 authorisation           string                JWT Token
 REQUIRED

```

```Response

200: OK

{
        "customertypeid": 1,

        "code": "     ",

        "name": "Beneficiery",

        "isactive": true,

        "createby": 1,

        "createdate": "2018-12-19T14:22:59.770Z",

        "createip": "192.168.1.1",

        "updateby": 1,

        "updatedate": "2018-12-19T14:22:59.770Z",

        "updateip": "192.168.1.1"
}

{
        "customertypeid": 2,

        "code": "     ",

        "name": "Suppliers",

        "isactive": true,

        "createby": 1,

        "createdate": "2018-12-19T14:22:59.770Z",

        "createip": "192.168.1.1",

        "updateby": 1,

        "updatedate": "2018-12-19T14:22:59.770Z",

        "updateip": "192.168.1.1"
}

```


**GET- Customer's Designation List**

Get Customer's Designation List.

````http://5.133.176.54:82/api/v1.0/Common/IndustryList/0````

```Request

Headers

 authorisation           string                JWT Token
 REQUIRED

```

```Response

200: OK

{
        "designationid": 9,
        "designationname": "Administration Manager",

        "isactive": true,

        "createby": 1,

        "createdate": "2018-12-19T14:08:21.000Z",

        "createip": "192.168.1.1",

        "updateby": 1,

        "updatedate": "2018-12-19T14:08:21.000Z",

        "updateip": "192.168.1.1"
}


```


**GET- Industry List**

Get Industry List.

````http://5.133.176.54:82/api/v1.0/Common/IndustryList/0````

```Request

Headers

 authorisation           string                JWT Token
 REQUIRED

```

```Response

200: OK

{
        "industryid": 1,

        "industryname": "Advertising and marketing / printing and publishing",

        "isactive": true,

        "createby": 1,

        "createdate": "2018-12-19T14:12:57.990Z",

        "createip": "192.168.1.1",

        "updateby": 1,

        "updatedate": "2018-12-19T14:12:57.990Z",

        "updateip": "192.168.1.1"
}


```
