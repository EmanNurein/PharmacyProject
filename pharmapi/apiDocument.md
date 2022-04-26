# Page 1

# List of city 

# https://localhost:9700/location
# https://pharm-project.herokuapp.com/location 
     
# List of pharmacy

# http://localhost:9700/pharmacy
# https://pharm-project.herokuapp.com/pharmacy


# List of pharmacy wrt to city

# http://localhost:9700/pharmacy/?state_id=1
# https://pharm-project.herokuapp.com/pharmacy/?state_id=1

# List of productTypes

# http://localhost:9700/producttype
# https://pharm-project.herokuapp.com/producttype

# Page 2

# List of pharmacy on basis of producttype

# http://localhost:9700/pharmacy/?producttype_id=2
# https://pharm-project.herokuapp.com/pharmacy/?producttype_id=2

# pharmacy on basis of product selected
# (POST) http://localhost:9700/product
  (Body) [6]
  [
    {
        "_id": "626688d2c7d11798ac3a956b",
        "pharmacy_id": 2,
        "pharmacy_name": "Almek Nimer Pharmacy",
        "location_id": 2,
        "state_id": 2,
        "product_id": 6,
        "address": "Amarat - Street No 15",
        "pharmacy_image": "https://i.ibb.co/wJ1tPz2/service-cust.jpg",
        "contact_number": "0912312312",
        "productTypes": [
            {
                "producttype_id": 2,
                "producttype_name": "Liquid"
            },
            {
                "producttype_id": 4,
                "producttype_name": "Capsule"
            }
        ],
        "image_gallery": [
            "https://i.ibb.co/7vJMw90/liquid-image.jpg",
            "https://i.ibb.co/bXQrT8Y/capsule2.jpg"
        ]
    }
]
# (POST) https://pharm-project.herokuapp.com/product
  (Body) [1,2]


# Filter on basis of producttype
# http://localhost:9700/filters/1?proId=1
# https://pharm-project.herokuapp.com/filters/1?proId=1

# Filter on basis of cost
# http://localhost:9700/filters/3?$lcost=2000&hcost=3000
# https://pharm-project.herokuapp.com/filters/3?$lcost=2000&hcost=3000


# page 3

# Details of Pharmacy

# http://localhost:9700/details/626714df194a2cd99f34cecd
# https://pharm-project.herokuapp.com/details/6267314e7f2364ff451529da

# Products on basis of pharmacy

# http://localhost:9700/products/?pharmId=1
# https://pharm-project.herokuapp.com/products/?pharmId=1

# Page 4

# Products detail of item selected

# (POST) http://localhost:9700/productItem
# (Body) [1,2,3]

# (POST)  https://pharm-project.herokuapp.com/productItem
# (Body)  [1,3,6]


# Page 5 

# Place Order
   # (POST) http://localhost:9700/placeOrder
   # <Body)
            {
                "name": "Nada",
                "email":"nada@gmail.com",
                "address": "Almuhandseen Block No.30",
                "phone": "092224578",
                "cost": 2300,
                "productItem":[3,6],
                "status":"pending"
            }

# (POST)  https://pharm-project.herokuapp.com/placeOrder
# (Body)  
       {
            "name": "habab",
            "email":"habab@gmail.com",
            "address": "Khartoum-3",
            "phone": "098761234",
            "cost": 1200,
            "productItem":[2],
            "status":"pending"
        }

# See all place order

# http://localhost:9700/viewOrder
# https://pharm-project.herokuapp.com/viewOrder

# Get order on basis of emailId

# http://localhost:9700/viewOrder?email=eman@gmail.com
# https://pharm-project.herokuapp.com/viewOrder/?email=eman22@gmail.com

# Update order

# (PUT) http://localhost:9700/updateOrder/62575a0400178fa239ef724c
   # (Body)  
        {
            
            "email":"eman22@hotmail.com",
            "address":"Alwaha -Khartoum",
            "status":"Delivered"                
        }

# (PUT) https://pharm-project.herokuapp.com/updateOrder/62673b99c04b76cd633a5669
   # (Body) 
        {
            
            "email":"eman22@hotmail.com",
            "address":"Alwaha -Khartoum",
            "status":"Delivered"              
        }


# login Api 

# GetAllUser

   # (GET)  http://localhost:5000/api/auth/users

   # (GET)  https://Pharm-loginapp.herokuapp.com/api/auth/users

# Register
    
   # (POST)  http://localhost:5000/api/auth/register
   # (Body)    
            {
                "name":"Sara",
                "email":"sara@gmail.com",
                "password":"sara@jan@2022",
                "phone":"0912321177",
                "role":"user"
            }
   # (post)  https://Pharm-loginapp.herokuapp.com/api/auth/register
   # (Body) 
            {
                "name":"Waleed",
                "email":"waleed@gmail.com",
                "password":"waleedjan",
                "phone":"0124242545",
                "role":"user"
            }

# Login

   # (POST)  http://localhost:5000/api/auth/login
   # (body)   
            {
                "email":"eman@gmail.com",
                "password":"eman2022"
            }
   # (Response)=> {auth:true,token:'eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9'}


   # (POST)  https://Pharm-loginapp.herokuapp.com/api/auth/login
   # (Body) 
            {
                "email":"samah@hotmail.com",
                "password":"123samah123"
            }
   # (Response) => {"auth": true, "token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9"}


# UserInfo 

   # (GET)  http://localhost:5000/api/auth/userinfo
   # (Header) {'x-access-token':'token value from login'}

   # (GET)  https://Pharm-loginapp.herokuapp.com/api/auth/userinfo
   # (Header)  {'x-access-token':'token value from login'}









