- product image
- product brand
- product serial 
```json
{
    status: false,
    data: 
    {
        serial: "date"
    }
}
```
- product discount
```json
{
    discount: "%/amount",
    value: "20"
}
```


## Employee 
- name
- phone
- address
- joinig date
- referance (string 1000)
- term of the contract (date)
- salary 
- designation
- other (string 1000)

## employee payment
- id
- user_id
- staff_id
- type (payment/other)
- amount
- status (complete/)
- month
- year
- comment

## salary
- id
- user_id
- staff_id
- salary
- amount @salary
- amount @other
- status
- month
- year