1) Get a specific artist's details based on artistId
  Request Components:
    - Method: GET
    - URL: /artists/:artistId
    - Headers: none
    - Body: none
  Response Components:
    - Status Code: 200 OK
    - Headers:
      * Content-Type: application/json
    - Body: details of the artist
      {
        artistId:
        name:
        albums: {
          albumId:
          name:
          artistId:
          }
        }
      }

2) Add an artist
  Request Components:
    - Method: POST
    - URL: /artists
    - Headers: 
      * Content-Type: application/json
    - Body: new artist's details
      {
        name: Samuel
      }
  Response Components:
    - Status Code: 201 CREATED
    - Headers:
      * Content-Type: application/json
    - Body: 
      {
        artistId: #,
        name: Samuel,
        albums: [],
      }

3) Edit a specified artist by artistId
  Request Components:
    - Method: PUT
    - URL: /artists/:artistId
    - Headers: 
      * Content-Type: application/json
    - Body: 
  Response Components:
    - Status Code: 200 OK
    - Headers: 
      * Content-Type: application/json
    - Body: 
      {
        artistId: #,
        editedValueKey: editedValue
        updatedAt: time
      }

4) Delete a specified artist by artistId
  Request Components:
    - Method: DELETE
    - URL: /artists/:artistId
    - Headers: 
      * Content-Type: application/json
    - Body: none
  Response Components:
    - Status Code: 200 OK
    - Headers: 
      * Content-Type: application/json
    - Body: 
      {
        message: "Successfully Deleted"
      }
  
5) Get all albums of a specific artist based on artistId
  Request Components:
    - Method: GET
    - URL: /artists/1/albums
    - Headers: none
    - Body: none
  Response Components:
    - Status Code: 200
    - Headers: 
      * Content-Type: application/json
    - Body: 
      {
        albumId:
        name:
        artistId:
      }

6) Get a specific album's details based on albumId
  Request Components:
    - Method: GET
    - URL: /albums/:albumId
    - Headers: none
    - Body: none
  Response Components:
    - Status Code: 200 OK
    - Headers: 
      * Content-Type: application/json
    - Body: 
      {
	      name:
	      albumId:
	      artistId:
	      artist: {
	      	name:
	      	artistId:
	      },
	      songs: [
	      	{
	      		name:
	      		lyrics:
	      		trackNumber:
	      		songId:
	      		createdAt: 
	      		updatedAt:
	      		albumId:
	      	}
	      ]
      }

7) Add an album to a specific artist based on artistId
  Request Components:
    - Method: POST
    - URL: /artists/:artistId/albums
    - Headers: 
      * Content-Type: application/json
    - Body: 
      {
        name:
        artistId:
      }
  Response Components:
    - Status Code: 201 CREATED
    - Headers: 
      * Content-Type: application/json
    - Body: 
      {
        albumId:
        name:
        artistId:
      }

8) Edit a specified album by albumId
  Request Components:
    - Method: PUT
    - URL: /albums/:albumId
    - Headers: 
      * Content-Type: application/json
    - Body: 
      {
        albumId:
        keyOfValueBeingEdited: valueBeingEdited
      }
  Response Components:
    - Status Code: 200 OK
    - Headers: 
      * Content-Type: application/json
    - Body: 
      {
        albumId:
        editedValueKey: editedValue
        artistId:
        updatedAt:
      }

9) Delete a specified album by albumId
  Request Components:
    - Method: DELETE
    - URL: /albums/:albumId
    - Headers: 
      * Content-Type: application/json
    - Body: 
  Response Components:
    - Status Code: 200 OK
    - Headers: 
      * Content-Type: application/json
    - Body: 
      {
        message: "Successfully Deleted"
      }

10) Get all songs of a specific artist based on artistId
  Request Components:
    - Method: GET
    - URL: /artists/:artistID/songs
    - Headers: none
    - Body: none
  Response Components:
    - Status Code: 200 OK
    - Headers: 
      * Content-Type: application/json
    - Body: Array of "song" objects
      {
        songId:
        name:
        trackNumber:
        albumId:
      }

11) Get all songs of a specific album based on albumId
  Request Components:
    - Method: GET
    - URL: /albums/:albumId/songs
    - Headers: none
    - Body: none
  Response Components:
    - Status Code: 200 OK
    - Headers: 
      * Content-Type: application/json
    - Body: Array of "song" objects
      {
        songId:
        name:
        trackNumber:
        albumId:
      }

12) Get all songs of a specified trackNumber
  Request Components:
    - Method: GET
    - URL: /trackNumbers/:trackNumber/songs
    - Headers: none
    - Body: none
  Response Components:
    - Status Code: 200 OK
    - Headers: 
      * Content-Type: application/json
    - Body: Array of "song" objects
      {
        songId:
        name:
        trackNumber:
        albumId:
      }

13) Get a specific song's details based on songId
  Request Components:
    - Method: GET
    - URL: /songs/:songId
    - Headers: none
    - Body: none
  Response Components:
    - Status Code: 200 OK
    - Headers: 
      * Content-Type: application/json
    - Body: "Song" object
      {
        songId:
        name:
        trackNumber:
        albumId:
      }

14) Add a song to a specific album based on albumId
  Request Components:
    - Method: POST
    - URL: /albums/:albumId/songs
    - Headers: 
      * Content-Type: application/json
    - Body: data of the song being added
      {
        songId:
        name:
        trackNumber:
      }

  Response Components:
    - Status Code: 201 CREATED
    - Headers:
      * Content-Type: application/json
    - Body: new "Song" object containing the provided data
      {
        songId:
        name:
        trackNumber:
      }

15) Edit a specified song by songId
  Request Components:
    - Method: PUT
    - URL: /songs/:songId
    - Headers: 
      * Content-Type: application/json
    - Body: edited data of the song
      {
        keyOfValueBeingEdited: valueBeingEdited
      }
  Response Components:
    - Status Code: 200 OK
    - Headers: 
      * Content-Type: application/json
    - Body: 
      {
        editedValueKey: editedValue
      }

16) Delete a specified song by songId
  Request Components:
    - Method: DELETE
    - URL: /songs/:songId
    - Headers: 
      * Content-Type: application/json
    - Body: 
  Response Components:
    - Status Code: 200 OK
    - Headers: 
      * Content-Type: application/json
    - Body: 
      {
        message: "Successfully Deleted"
      }