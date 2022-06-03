# joys-in-life

## Description
***

API for travel app to organize ideas and trip planning.

### Development Process
   DATE 		 | 		  PROGRESS     |     BLOCKS 		 |  	 GOALS     |
------------ | ----------------- | --------------- | ------------- |
06/02/2022 | Folder structure created. Functional CRUD on Trip, Tag, and Activity. | None | Implement Users and Auth |

## Models
***

```
Trip = {
    destination: String (required),
    name: String,
    startDate: String,
    endDate: String
}

Activity = {
    type: String,
    notes: String,
    tags: [String, ref=Tag]
}

Tag = {
    name: String,
    slug: String,
    activities: [String, ref=Activity]
}
```

## Routes
***

### Trip
   VERB 		 | 		  PATH 		 |  	 DESCRIPTION
------------ | ------------- | -------------------
GET | /api/v1/trips | list of trips |
GET | /api/v1/trips/:id | returns one trip |
POST | /api/v1/trips | adds new trip |
PUT | /api/v1/trips/:id | updates one trip |
DELETE | /api/v1/trips/:id | deletes one trip |

### Activity
   VERB 		 | 		  PATH 		 |  	 DESCRIPTION
------------ | ------------- | -------------------
GET | /api/v1/activities | list of activities |
GET | /api/v1/activities/:id | returns one activity |
POST | /api/v1/activities | adds new activity |
PUT | /api/v1/activities/:id | updates one activity |
DELETE | /api/v1/activities/:id | deletes one activity |

### Tag
   VERB 		 | 		  PATH 		 |  	 DESCRIPTION
------------ | ------------- | -------------------
GET | /api/v1/tags | list of tags |
GET | /api/v1/tags/:id | returns one tag |
POST | /api/v1/tags | adds new tag |
PUT | /api/v1/tags/:id | updates one tag |
DELETE | /api/v1/tags/:id | deletes one tag |

## Technologies
***
1. Express
2. JSON Web Token
3. Mongoose

## Stretch Goals
***