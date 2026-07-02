# Database Design

## 1. Users Collection

| Field | Data Type | Required | Description |
|--------|-----------|----------|-------------|
| _id | ObjectId | Yes | Unique user ID |
| fullName | String | Yes | User's full name |
| email | String | Yes | Email address |
| phone | String | Yes | Mobile number |
| password | String | Yes | Encrypted password |
| profilePhoto | String | No | Profile image URL |
| preferredLanguage | String | Yes | English/Hindi/Kannada |
| currentLocation | Object | No | Latitude & Longitude |
| createdAt | Date | Yes | Account creation date |
| updatedAt | Date | Yes | Last updated date |
| accountStatus | String | Yes | Active / Suspended |

## 2. Vendors Collection

| Field | Data Type | Required | Description |
|--------|-----------|----------|-------------|
| _id | ObjectId | Yes | Vendor ID |
| ownerName | String | Yes | Owner name |
| shopName | String | Yes | Shop name |
| categoryId | ObjectId | Yes | Category reference |
| phone | String | Yes | Contact number |
| email | String | No | Email |
| address | String | Yes | Shop address |
| latitude | Double | Yes | Latitude |
| longitude | Double | Yes | Longitude |
| shopImage | String | No | Shop image |
| description | String | No | About shop |
| openingTime | String | Yes | Shop opening time |
| closingTime | String | Yes | Shop closing time |
| averageRating | Double | Yes | Average rating |
| totalReviews | Integer | Yes | Number of reviews |
| verificationStatus | String | Yes | Pending / Approved / Rejected |
| createdAt | Date | Yes | Registration date |

## 3. Categories Collection

| Field | Data Type | Description |
|--------|-----------|-------------|
| _id | ObjectId | Category ID |
| categoryName | String | Street Food, Tailor, etc. |
| categoryImage | String | Icon/Image |

## 4. Services Collection

| Field | Data Type | Description |
|--------|-----------|-------------|
| _id | ObjectId | Service ID |
| vendorId | ObjectId | Vendor reference |
| serviceName | String | Name of service |
| description | String | Service description |
| price | Decimal | Price |
| image | String | Service image |
| availability | Boolean | Available or not |

## 5. Reviews Collection

| Field | Data Type | Description |
|--------|-----------|-------------|
| _id | ObjectId | Review ID |
| userId | ObjectId | User reference |
| vendorId | ObjectId | Vendor reference |
| rating | Integer | 1-5 |
| review | String | Review text |
| createdAt | Date | Date |

## 6. Complaints Collection

| Field | Data Type | Description |
|--------|-----------|-------------|
| _id | ObjectId | Complaint ID |
| userId | ObjectId | User |
| vendorId | ObjectId | Vendor |
| reason | String | Complaint reason |
| description | String | Complaint details |
| status | String | Pending/Resolved |
| createdAt | Date | Date |

## 7. Chat Collection

| Field | Data Type | Description |
|--------|-----------|-------------|
| _id | ObjectId | Message ID |
| senderId | ObjectId | Sender |
| receiverId | ObjectId | Receiver |
| message | String | Message |
| sentAt | Date | Timestamp |
| isRead | Boolean | Read status |

## 8. Notifications Collection

| Field | Data Type | Description |
|--------|-----------|-------------|
| _id | ObjectId | Notification ID |
| userId | ObjectId | User |
| title | String | Notification title |
| message | String | Notification content |
| isRead | Boolean | Read status |
| createdAt | Date | Date |

## 9. Admin Collection

| Field | Data Type | Description |
|--------|-----------|-------------|
| _id | ObjectId | Admin ID |
| username | String | Username |
| password | String | Encrypted password |
| email | String | Email |
| role | String | Super Admin / Admin |

