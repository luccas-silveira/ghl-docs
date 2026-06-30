---
title: "Update an item in a queue"
source_url: https://marketplace.gohighlevel.com/docs/ghl/social-planner/update-queue-item
version: v3
method: PUT
endpoint: https://services.leadconnectorhq.com/social-media-posting/category/queues/:queueId/items/:itemId
summary: "Updates the content or variations of a specific item within a category queue"
---
# Update an item in a queue

```
PUT https://services.leadconnectorhq.com/social-media-posting/category/queues/:queueId/items/:itemId
```

Updates the content or variations of a specific item within a category queue.

## Request

## Responses

- 200
- 400
- 401
- 422

The queue item has been successfully updated.

Bad Request

Unauthorized

Unprocessable Entity

#### Authorization: Authorization

```
name: Authorizationtype: httpscopes: socialplanner/category.writescheme: bearerbearerFormat: JWTin: headerdescription: Use the Access Token generated with user type as Sub-Account (OR) Private Integration Token of Sub-Account.
```

- curl
- nodejs
- python
- php
- java
- go
- ruby
- powershell

- CURL

```bash
curl -L -X PUT 'https://services.leadconnectorhq.com/social-media-posting/category/queues/:queueId/items/:itemId' \
-H 'Content-Type: application/json' \
-H 'Accept: application/json' \
-H 'Authorization: Bearer <TOKEN>' \
-d '{
  "locationId": "609e126a1c4ae1001291e1b5",
  "sessionId": "60af88475f1b2c001f5d5f4b",
  "modifiedPostPayload": {
    "accountIds": [\
      "aF3KhyL8JIuBwzK3m7Ly_iVrVJ2uoXNF0wzcBzgl5_12554616564525983496"\
    ],
    "summary": "Hello World",
    "media": [\
      {\
        "url": "https://example.com/image.jpg",\
        "type": "image/jpeg",\
        "caption": "Sample caption",\
        "altText": "A sunset over the ocean with silhouetted palm trees"\
      }\
    ],
    "status": "scheduled",
    "scheduleDate": "2024-01-15T10:00:00Z",
    "selectedBestTime": "2024-01-15T10:00:00Z",
    "createdBy": "Lx1EI6YIgQYMQi0ytFXv",
    "followUpComment": "What do you think? Let us know in the comments!",
    "ogTagsDetails": {
      "metaImage": "https://example.com/image.jpg",
      "metaLink": "https://www.yahoo.com/",
      "ogTitle": "Page Title",
      "ogDescription": "Page Description"
    },
    "type": "post",
    "postApprovalDetails": {
      "approver": "iVrVJ2uoXNF0wzcBzgl5",
      "approvalStatus": "pending"
    },
    "scheduleTimeUpdated": true,
    "tags": [\
      "65f151c99bc2bf3aaf970d72",\
      "65f151c99bc2bf3aaf970d73"\
    ],
    "categoryId": "65f151c99bc2bf3aaf970d72",
    "applyWatermark": true,
    "tiktokPostDetails": {
      "privacyLevel": "PUBLIC_TO_EVERYONE",
      "enableComment": true,
      "enableDuet": false
    },
    "gmbPostDetails": {
      "gmbEventType": "STANDARD",
      "actionType": "BOOK",
      "url": "https://example.com"
    },
    "userId": "sdfdsfdsfEWEsdfsdsW32dd",
    "linkedinPostDetails": {
      "pdfTitle": "Q4 Marketing Strategy Presentation",
      "postAsPdf": true,
      "poll": {
        "question": "What is your favorite color?",
        "options": [\
          {\
            "text": "Red"\
          }\
        ],
        "settings": {
          "duration": "SEVEN_DAYS"
        }
      }
    },
    "pinterestPostDetails": {
      "title": "10 Easy Home Decor Ideas for 2024",
      "link": "https://yoursite.com/blog/home-decor-ideas",
      "pinterestBoards": [\
        {\
          "accountId": "6887d6de1d8175813d50dab8",\
          "boards": [\
            "987654321098765432",\
            "234567890123456789"\
          ]\
        },\
        {\
          "accountId": "682c7d1710a2fe3d805a3513",\
          "boards": [\
            "111222333444555666"\
          ]\
        }\
      ],
      "shortenedLinks": [\
        "string"\
      ]
    },
    "facebookPostDetails": {
      "type": "post",
      "textFormatPresetId": "303063890126415"
    },
    "instagramPostDetails": {
      "type": "post",
      "collaborators": {
        "accountId1": [\
          "username1",\
          "username2"\
        ],
        "accountId2": [\
          "username3",\
          "username4"\
        ]
      },
      "showOnFeed": true,
      "publishViaPushNotification": true,
      "publisherNote": "When publishing, add swipe up link to the landing page so that we can direct them to the sales page"
    },
    "youtubePostDetails": {
      "title": "How to Build a Successful Marketing Strategy in 2024",
      "privacyLevel": "public",
      "type": "video"
    },
    "locationId": "ve9EPM428h8vShlRW1KT"
  },
  "newOrder": 0,
  "variations": [\
    {\
      "content": "Check out our latest blog post! #marketing #socialmedia",\
      "mentions": [\
        {\
          "platform": "instagram",\
          "username": "example_user",\
          "offset": 10,\
          "length": 12\
        }\
      ],\
      "ogTags": {\
        "metaLink": "https://example.com/blog/post-title",\
        "metaImage": "https://example.com/images/preview.png",\
        "ogTitle": "Check out our latest blog post!"\
      }\
    }\
  ],
  "primaryImage": "http://example.com/media.png"
}'
```

Request Collapse all

Base URL

Edit

https://services.leadconnectorhq.com

Auth

Bearer Token

Parameters

queueId — pathrequired

itemId — pathrequired

Version — headerrequired

\-\-\-v3

Body required

```json
{
  "locationId": "609e126a1c4ae1001291e1b5",
  "sessionId": "60af88475f1b2c001f5d5f4b",
  "modifiedPostPayload": {
    "accountIds": [\
      "aF3KhyL8JIuBwzK3m7Ly_iVrVJ2uoXNF0wzcBzgl5_12554616564525983496"\
    ],
    "summary": "Hello World",
    "media": [\
      {\
        "url": "https://example.com/image.jpg",\
        "type": "image/jpeg",\
        "caption": "Sample caption",\
        "altText": "A sunset over the ocean with silhouetted palm trees"\
      }\
    ],
    "status": "scheduled",
    "scheduleDate": "2024-01-15T10:00:00Z",
    "selectedBestTime": "2024-01-15T10:00:00Z",
    "createdBy": "Lx1EI6YIgQYMQi0ytFXv",
    "followUpComment": "What do you think? Let us know in the comments!",
    "ogTagsDetails": {
      "metaImage": "https://example.com/image.jpg",
      "metaLink": "https://www.yahoo.com/",
      "ogTitle": "Page Title",
      "ogDescription": "Page Description"
    },
    "type": "post",
    "postApprovalDetails": {
      "approver": "iVrVJ2uoXNF0wzcBzgl5",
      "approvalStatus": "pending"
    },
    "scheduleTimeUpdated": true,
    "tags": [\
      "65f151c99bc2bf3aaf970d72",\
      "65f151c99bc2bf3aaf970d73"\
    ],
    "categoryId": "65f151c99bc2bf3aaf970d72",
    "applyWatermark": true,
    "tiktokPostDetails": {
      "privacyLevel": "PUBLIC_TO_EVERYONE",
      "enableComment": true,
      "enableDuet": false
    },
    "gmbPostDetails": {
      "gmbEventType": "STANDARD",
      "actionType": "BOOK",
      "url": "https://example.com"
    },
    "userId": "sdfdsfdsfEWEsdfsdsW32dd",
    "linkedinPostDetails": {
      "pdfTitle": "Q4 Marketing Strategy Presentation",
      "postAsPdf": true,
      "poll": {
        "question": "What is your favorite color?",
        "options": [\
          {\
            "text": "Red"\
          }\
        ],
        "settings": {
          "duration": "SEVEN_DAYS"
        }
      }
    },
    "pinterestPostDetails": {
      "title": "10 Easy Home Decor Ideas for 2024",
      "link": "https://yoursite.com/blog/home-decor-ideas",
      "pinterestBoards": [\
        {\
          "accountId": "6887d6de1d8175813d50dab8",\
          "boards": [\
            "987654321098765432",\
            "234567890123456789"\
          ]\
        },\
        {\
          "accountId": "682c7d1710a2fe3d805a3513",\
          "boards": [\
            "111222333444555666"\
          ]\
        }\
      ],
      "shortenedLinks": [\
        "string"\
      ]
    },
    "facebookPostDetails": {
      "type": "post",
      "textFormatPresetId": "303063890126415"
    },
    "instagramPostDetails": {
      "type": "post",
      "collaborators": {
        "accountId1": [\
          "username1",\
          "username2"\
        ],
        "accountId2": [\
          "username3",\
          "username4"\
        ]
      },
      "showOnFeed": true,
      "publishViaPushNotification": true,
      "publisherNote": "When publishing, add swipe up link to the landing page so that we can direct them to the sales page"
    },
    "youtubePostDetails": {
      "title": "How to Build a Successful Marketing Strategy in 2024",
      "privacyLevel": "public",
      "type": "video"
    },
    "locationId": "ve9EPM428h8vShlRW1KT"
  },
  "newOrder": 0,
  "variations": [\
    {\
      "content": "Check out our latest blog post! #marketing #socialmedia",\
      "mentions": [\
        {\
          "platform": "instagram",\
          "username": "example_user",\
          "offset": 10,\
          "length": 12\
        }\
      ],\
      "ogTags": {\
        "metaLink": "https://example.com/blog/post-title",\
        "metaImage": "https://example.com/images/preview.png",\
        "ogTitle": "Check out our latest blog post!"\
      }\
    }\
  ],
  "primaryImage": "http://example.com/media.png"
}
```

Send API Request

ResponseClear

Click the `Send API Request` button above and see the response here!