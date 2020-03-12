FORMAT: 1A
HOST: ttps://private-81299-photoapi1.apiary-mock.com

# Photo Gallery API

Simple API allowing consumers to view photos, comments and contact persons.

## Photo [/photo]

### List All Photos [GET]

List all photos.

+ Response 200 (application/json)

        [
            {
                "id": "1",
                "caption": "caption 1",
                "url": "photos.com/gallery/1",
                "contact_id": "1"
            },
            {
                "id": "2",
                "caption": "caption 2",
                "url": "photos.com/gallery/2",
                "contact_id": "2"
            },
            {
                "id": "3",
                "caption": "caption 3",
                "url": "photos.com/gallery/3",
                "contact_id": "3"
            }
        ]

### Create New Photo [POST]

Create new photo.

+ Request (application/json)

        {
            "caption": "caption 4",
            "url": "photos.com/gallery/4",
            "contact_id": "3"
        }

+ Response 201 (application/json)

    + Headers

            Location: /photo/4

    + Body

            {
                "id": "4",
                "caption": "caption 4",
                "url": "photos.com/gallery/4",
                "contact_id": "3"
            }
            
## Photos Resource [/photo/{id}]

+ Parameters
    + id : 1 (number, required) - An unique identifier of the message

### List Photo with ID [GET]

List specific photo using its ID.

+ Response 200 (application/json)

        [
            {
                "id": "1",
                "caption": "caption 1",
                "url": "photos.com/gallery/1",
                "contact_id": "1"
            }
        ]

### Edit a Photo [PATCH]

Edit specific photo using its ID.

+ Request (application/json)

        {
            "caption": "caption 1a"
        }

+ Response 201 (application/json)

        [
            {
                "id": "1",
                "caption": "caption 1a",
                "url": "photos.com/gallery/1",
                "contact_id": "1"
            }
        ]
        
### Delete a Photo [DELETE]

Delete a photo.

+ Response 204


## Photo Comments [/comment]

### List All Photo Comments [GET]

List all photo comments.

+ Response 200 (application/json)

        [
            {
                "id": "1",
                "content": "content 1",
                "photo_id": "1",
                "contact_id": "1"
            },
            {
                "id": "2",
                "content": "content 2",
                "photo_id": "2",
                "contact_id": "2"
            },
            {
                "id": "3",
                "content": "content 3",
                "photo_id": "3",
                "contact_id": "3"
            }
        ]

### Create New Photo Comment [POST]

Create new photo comment.

+ Request (application/json)

        {
            "content": "content 4",
            "photo_id": "3",
        }

+ Response 201 (application/json)

    + Headers

            Location: /comment/4

    + Body

            {
                "id": "4",
                "content": "content 4",
                "photo_id": "3",
                "contact_id": "3"
            }
            
## Photo Comments Resource [/comment/{id}]

+ Parameters
    + id : 1 (number, required) - An unique identifier of the message

### List Photo Comment with ID [GET]

List specific photo comment using its ID.

+ Response 200 (application/json)

        [
            {
                "id": "1",
                "content": "content 1",
                "photo_id": "1",
                "contact_id": "1"
            }
        ]

### Edit a Photo Comment [PATCH]

Edit specific photo comment using its ID.

+ Request (application/json)

        {
            "content": "content 1a"
        }

+ Response 201 (application/json)

        [
            {
                "id": "1",
                "content": "content 1",
                "photo_id": "1",
                "contact_id": "1"
            }
        ]
        
### Delete a Photo Comment [DELETE]

Delete a photo comment.

+ Response 204


## Contacts [/contact]

### List All Contacts [GET]

List all contacts.

+ Response 200 (application/json)

        [
            {
                "id": "1",
                "username": "absalim",
                "password": "***********",
                "email": "absalim@email.com",
                "full_name": "Abdul Salim"
            },
            {
                "id": "2",
                "username": "nadyarich",
                "password": "***********",
                "email": "nadyarich@email.com",
                "full_name": "Nadya Richna"
            },
            {
                "id": "3",
                "username": "tjahtjah",
                "password": "***********",
                "email": "tjahtjah@email.com",
                "full_name": "Indra Tjahyadi"
            }
        ]

### Create New Contact [POST]

Create new contact.

+ Request (application/json)

        {
            "username": "rapangga",
            "password": "***********",
            "email": "rapangga@email.com",
            "full_name": "Rangga Dwipangga"
        }

+ Response 201 (application/json)

    + Headers

            Location: /contact/4

    + Body

            {
                "id": "4",
                "username": "rapangga",
                "password": "***********",
                "email": "rapangga@email.com",
                "full_name": "Rangga Dwipangga"
            }
            
## Contacts Resource [/contact/{id}]

+ Parameters
    + id : 1 (number, required) - An unique identifier of the message

### List Post with ID [GET]

List specific comment using its ID.

+ Response 200 (application/json)

        [
            {
                "id": "1",
                "username": "absalim",
                "password": "***********",
                "email": "absalim@email.com",
                "full_name": "Abdul Salim"
            }
        ]

### Edit a Contact [PATCH]

Edit specific contact using its ID.

+ Request (application/json)

        {
            "email": "abdsalim@email.com"
        }

+ Response 201 (application/json)

        [
            {
                "id": "1",
                "username": "absalim",
                "password": "***********",
                "email": "abdsalim@email.com",
                "full_name": "Abdul Salim"
            }
        ]
        
### Delete a Contact [DELETE]

Delete a contact.

+ Response 204
