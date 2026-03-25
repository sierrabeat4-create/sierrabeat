# MongoDB Database Schema

## Users
- **userId**: ObjectID - Unique identifier for the user
- **username**: String - Unique username of the user
- **email**: String - Email address of the user
- **password**: String - Hashed password for authentication
- **createdAt**: Date - Timestamp for when the user account was created
- **updatedAt**: Date - Timestamp for the last update of the user account

## Tracks
- **trackId**: ObjectID - Unique identifier for the track
- **title**: String - The title of the track
- **artistId**: ObjectID - Reference to the artist (user) who created the track
- **genre**: String - Genre of the track
- **duration**: Number - Duration of the track in seconds
- **createdAt**: Date - Timestamp for when the track was added
- **updatedAt**: Date - Timestamp for the last update of the track

## Projects
- **projectId**: ObjectID - Unique identifier for the project
- **title**: String - The title of the project
- **description**: String - Description of the project
- **ownerId**: ObjectID - Reference to the user who owns the project
- **createdAt**: Date - Timestamp for when the project was created
- **updatedAt**: Date - Timestamp for the last update of the project

## Messages
- **messageId**: ObjectID - Unique identifier for the message
- **senderId**: ObjectID - Reference to the user who sent the message
- **receiverId**: ObjectID - Reference to the user who receives the message
- **content**: String - Content of the message
- **createdAt**: Date - Timestamp for when the message was sent

## Comments
- **commentId**: ObjectID - Unique identifier for the comment
- **postId**: ObjectID - Reference to the project/track/review this comment refers to
- **userId**: ObjectID - Reference to the user who made the comment
- **content**: String - Content of the comment
- **createdAt**: Date - Timestamp for when the comment was made

## Reviews
- **reviewId**: ObjectID - Unique identifier for the review
- **trackId**: ObjectID - Reference to the track being reviewed
- **userId**: ObjectID - Reference to the user who wrote the review
- **rating**: Number - Rating given to the track (1 to 5)
- **content**: String - Content of the review
- **createdAt**: Date - Timestamp for when the review was created

## Notifications
- **notificationId**: ObjectID - Unique identifier for the notification
- **userId**: ObjectID - Reference to the user the notification is for
- **message**: String - Notification message
- **isRead**: Boolean - Indicates if the notification has been read
- **createdAt**: Date - Timestamp for when the notification was created

## Follows
- **followId**: ObjectID - Unique identifier for the follow relationship
- **followerId**: ObjectID - Reference to the user who follows
- **followedId**: ObjectID - Reference to the user being followed
- **createdAt**: Date - Timestamp for when the follow was made

## Favorites
- **favoriteId**: ObjectID - Unique identifier for the favorite entry
- **userId**: ObjectID - Reference to the user who favorited
- **trackId**: ObjectID - Reference to the track that is favorited
- **createdAt**: Date - Timestamp for when the track was favorited
