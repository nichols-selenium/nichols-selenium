I teamed up with three others to co develop Identiflora, a mobile application that utilizes an integrated AI model to identify pictures of plants and incorporates a competitive user leveling and social system. Below you can view my specific contributions.

Feature 1: Developed a Flutter social networking interface supporting user search, friend requests, request acceptance/rejection, friend removal, and dynamic retrieval of friendship data from backend services. 
[_View Code_](https://github.com/Identiflora/flutter-app/blob/innovation-day/lib/friends_utils.dart)
    
Feature 2: Implements authenticated Flutter-to-FastAPI communication for retrieving, searching, adding, rejecting, and removing friends, including JSON response parsing and HTTP error handling.
[_View Code_](https://github.com/Identiflora/flutter-app/blob/innovation-day/lib/database_utils.dart#L1057-L1207)

Feature 3: Designed and implemented MySQL stored procedures for the friends system: friendship creation and validation, accepted-friend retrieval, pending request handling, request acceptance/rejection, and friend removal. See code below.

- Pending/accept/reject/remove logic
[_View Code_](https://github.com/Identiflora/identiflora-database/blob/main/schema/initialize_database.sql#L684-L773)

- Friendship relationship status tracking, self-friendship validation, and foreign-key constraints
 [_View Code_](https://github.com/Identiflora/identiflora-database/blob/main/schema/initialize_database.sql#L147-L164)
 
- Accepted friend retrieval and associated user data lookup
[_View Code_](https://github.com/Identiflora/identiflora-database/blob/main/schema/initialize_database.sql#L538-L555)

- Friendship existence checks and friendship creation procedures
 [_View Code_](https://github.com/Identiflora/identiflora-database/blob/main/schema/initialize_database.sql#L460-L478)
