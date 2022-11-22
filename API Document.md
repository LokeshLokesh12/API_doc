base
https://airtrl-api.onrender.com/

-----------------------------------------------------

>>>to display all plackes
method:"GET"
https://airtrl-api.onrender.com/plans

-----------------------------------------------------

>>>to filter plans with repect to plan type
method:"GET"
`https://airtrl-api.onrender.com/filter/${type}`
>>>>example
https://airtrl-api.onrender.com/filter/Data

-----------------------------------------------------

>>>to filter plans with repect to plan type and price
method:"GET"
`https://airtrl-api.onrender.com/filter/${type}?cost=${price}`
>>>>example
https://airtrl-api.onrender.com/filter/Data?cost=99

-----------------------------------------------------

>>>to filter plans with mongodb ObjectID
`https://airtrl-api.onrender.com/plans/${_id}`
>>>>example
https://airtrl-api.onrender.com/plans/636f8f8081e8209c6de5a7ba

-----------------------------------------------------


<!--  user-information  -->

>>>to get all user
method:"GET"
https://airtel-user-api.onrender.com/api/auth/users

-----------------------------------------------------

>>>to login
method:"GET"
In body: 
{
    phone:req.body.phone
    password:req.body.password
}
https://airtel-user-api.onrender.com/api/auth/login
>>>This gives a response with a token key
>>>use that token in the header
In header:
{
    Content-Type:"application/json"    
    x-access-token:`${token}`
}
https://airtel-user-api.onrender.com/api/auth/userinfo

-----------------------------------------------------

>>>to register
method:"POST"
In body{
    name:req.body.name,
    email:req.body.email,
    password:hashpassword,
    phone:req.body.phone
}
https://airtrl-user-api.onrender.com/api/auth/register

-----------------------------------------------------

>>>method:"POST"
In body{
    orderID: req.body_id,
    amount: req.body.cost,
    customerId: req.body.name,
    customerEmail: req.body.email,
    customerPhone: req.body.phone,
    customerRest: req.body.rest_name
}
https://airtrl-payment-api.onrender.com/paynow

-----------------------------------------------------

