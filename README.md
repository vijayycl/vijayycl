Request Body: { "email": "user@example.com", "password": "password123", "username": "user123" }

Response: { "message": "User registered successfully", "user_id": "xyz123", "token": "jwt_token" }

POST /api/auth/login: यूज़र लॉगिन के लिए।

Request Body: { "email": "user@example.com", "password": "password123" }

Response: { "message": "Login successful", "token": "jwt_token" }


Response: { "user_id": "xyz123", "username": "user123", "email": "user@example.com", "profile_picture": "url_to_image" }

PUT /api/users/{user_id}: यूज़र प्रोफाइल अपडेट करने के लिए।

Request Body: { "username": "new_user123", "profile_picture": "new_image_url" }

Response: { "message": "Profile updated successfully" }
Request Body: { "user_id": "xyz123", "content": "Hello World!", "image": "url_to_image" }

Response: { "message": "Post created successfully", "post_id": "abc123" }

GET /api/posts/{post_id}: एक विशेष पोस्ट को प्राप्त करने के लिए।

Response: { "post_id": "abc123", "user_id": "xyz123", "content": "Hello World!", "image": "url_to_image", "likes": 10, "comments": 5 }
Request Body: { "user_id": "xyz123" }

Response: { "message": "Post liked successfully" }

POST /api/posts/{post_id}/comment: किसी पोस्ट पर कमेंट करने के लिए।

Request Body: { "user_id": "xyz123", "comment": "Nice post!" }

Response: { "message": "Comment added successfully" }
Request Body: { "follower_id": "abc123" }

Response: { "message": "User followed successfully" }

POST /api/users/{user_id}/unfollow: किसी यूज़र को अनफॉलो करने के लिए।

Request Body: { "follower_id": "abc123" }

Response: { "message": "User unfollowed successfully" }
Response: [ { "notification_id": "notif1", "message": "User xyz123 liked your post.", "timestamp": "2024-12-28T14:30:00" } ]
Response: [ { "sender_id": "abc123", "message": "Hello!", "timestamp": "2024-12-28T14:30:00" }, { "sender_id": "xyz123", "message": "Hi!", "timestamp": "2024-12-28T14:31:00" } ]
equest Body: { "sender_id": "abc123", "receiver_id": "xyz123", "message": "How are you?" }

Response: { "message": "Message sent successfully" }


