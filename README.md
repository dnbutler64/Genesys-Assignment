## Intro
This repository is my submission for a Genesys code challenge

## Build & Run
```sh
git clone https://github.com/dnbutler64/Genesys-Assignment.git
cd Genesys-Assignment
mvn clean install
mvn spring-boot:run
```

## API Endpoints
* [Add a user](https://github.com/dnbutler64/Genesys-Assignment/blob/master/README.md#1) : `POST /api/user`
* [Update a user](https://github.com/dnbutler64/Genesys-Assignment/blob/master/README.md#2) : `PUT /api/user/{id}`
* [Find a building](https://github.com/dnbutler64/Genesys-Assignment/blob/master/README.md#3) : `GET /api/user/building/{buildingId}`
* [Get status of all elevators in a building](https://github.com/dnbutler64/Genesys-Assignment/blob/master/README.md#4) : `GET /api/user/elevatorStates/{buildingId}`
* [User summons an elevator](https://github.com/dnbutler64/Genesys-Assignment/blob/master/README.md#5) : `GET /api/user/elevator/{elevatorId}`
* [User selects a floor](https://github.com/dnbutler64/Genesys-Assignment/blob/master/README.md#6) : `PUT /api/user/elevator/{elevatorId}`

### Add a user <a name="1"></a>

**URL** : `/api/user/`

**Method** : `POST`

**Example Body** :

```json
{
    "userName": "John",
    "buildingIds": [
        "1234",
        "5678"
    ]
}
```
### Update a user <a name="2"></a>

**URL** : `/api/user/{id}`

**Method** : `PUT`

**Example Body** :

```json
{
    "userId": "af48a487-82a1-4868-8f82-e4df529d31a2",
    "userName": "Darren",
    "buildingIds": [
        "577f1505-bc19-4d04-8a92-55d9986e1a22",
        "9533971b-6e7c-424c-9a00-b75670c11796"
    ]
}
```
### Find a building <a name="3"></a>

**URL** : `/api/user/building/{buildingId}`

**Method** : `GET`

### Get status of all elevators in a building <a name="4"></a>

**URL** : `/api/user/elevatorStates/{buildingId}`

**Method** : `GET`

### User summons an elevator <a name="5"></a>

**URL** : `/api/user/elevator/{elevatorId}`

**Method** : `GET`

### User selects a floor <a name="6"></a>

**URL** : `/api/user/elevator/{elevatorId}?floor={floorNumber}`

**Method** : `PUT`

**Example** : 
`http://localhost:8081/api/user/elevator/40b5cb56-ceaf-4601-995a-c651b557ecde?floor=2`
