> `POST` **/all**
>> _`Request`_
```json
{ token: }
```

>> _`Response`_
```json
{
    [
        {
            "_id": "5d5036de338e25c220aaba50",
            "category": "lodging",
            "color": "orange", 
            "endTime": [], 
            "ideas": [
                {
                    "coordinates": {
                        "geometry": {
                             "coordinates": [-16.318302154541016, 28.481819102847485], "type": "Point"
                             }, 
                        "type": "Feature"
                    }, 
                    "description": "Buen sitio para descansar y echarte un sueño", "endTime": [15, 0],
                    "link": "http://...", 
                    "locations": {
                         "name": "Santa Cruz de Tenerife",
                          "zone": "Llano del Moro"
                    },
                    "name": "Casa Domi",
                    "startTime": [9, 0]
                },
                {},
                {}
            ],
            "startTime": []
        },
        {
            "_id": "5d5036de338e25c220aaba51", "category": "food",
            "color": "green",
            ...
}
```

---
> `POST` **/categories**
>> _`Request`_
```json
{ 
    token: ,
    category: "food"
}
```

>> _`Response`_
```json
[
    {
        "_id": "5d5036de338e25c220aaba51", 
        "category": "food", 
        "color": "green", 
        "endTime": [],
        "ideas": [
            {
                "coordinates": {
                    "geometry": {
                        "coordinates": [-16.318302154541016, 28.481819102847485], 
                        "type": "Point"}, 
                        "type": "Feature"
                    }, 
            "description": "Go to Guachinche Ivan in La Laguna and take a rabbit",
            "endTime": [11, 0],
            "link": "http://...", 
            "locations": {
                "name": "Santa Cruz de Tenerife", "zone": "Añaza"},
            "name": "Guachinche Ivan",
            "startTime": [9, 0]
            },
        {}, 
        {}
        ], 
        "startTime": []
    }
]
```


---
> `POST` **/ideas**
>> _`Request`_
```json
{ 
    token: 
    category: "food",
}
```

>> _`Response`_
```json
{
    [
        {
            "_id": "5d5036de338e25c220aaba51", 
            "ideas": [
                {
                    "coordinates": {
                "geometry": {
                        "coordinates": [-16.318302154541016, 28.481819102847485], 
                        "type": "Point"
                    },
                    "type": "Feature"
                }, 
                "description": "Go to Guachinche Ivan in La Laguna and take a rabbit",
                "endTime": [11, 0], 
                "link": "http://...", 
                "locations": {
                    "name": "Santa Cruz de Tenerife", "zone": "Añaza"
                    }, 
                "name": "Guachinche Ivan",
                "startTime": [9, 0]
            },
            {},
            {}
            ]
        }
    ]
}
```


---
> `PUT` **/:categories:ideas**
>> _`Request`_
```json
{ 
    token: ,
    category: "food",
    idea:{
            "coordinates": {}, 
            "description": "",
            "startTime": [9, 0],
            "endTime": [11, 0], 
            "link": "http://...", 
            "locations": {
                "name": "", "zone": ""
                }, 
            "name": "",
    }
}
```

>> _`Response`_
```json
{
    message: "Idea Added"
}
```

---
> `DELETE` **/:ideas**
>> _`Request`_
```json
{ 
    token: 
    idea:{
        name:""
    }
}
```

>> _`Response`_
```json
{
    message: "Idea Delete"
}
```