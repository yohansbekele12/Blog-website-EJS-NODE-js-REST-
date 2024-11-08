Blog Post API with Express.js
This is a simple blog post API built with Express.js. It provides CRUD (Create, Read, Update, Delete) functionality for blog posts and uses EJS templates in the public directory to render pages.

Project Structure
index.js / server.js: The main server file containing the API routes.
public: The directory containing EJS templates for rendering pages.
README.md: Documentation for the project.
Features
In-memory data storage for blog posts.
RESTful API endpoints for creating, retrieving, updating, and deleting blog posts.
EJS templates used to render posts in the browser.
Getting Started
Prerequisites
Node.js (>= 12.x)
npm (>= 6.x)
Installation
Clone the repository:

bash
Copy code
git clone https://github.com/your-username/your-repo-name.git
Navigate to the project directory:

bash
Copy code
cd your-repo-name
Install dependencies:

bash
Copy code
npm install
Run the server:

bash
Copy code
node index.js
or, if using server.js:

bash
Copy code
node server.js
Visit the API: The API will be available at http://localhost:4000.

API Endpoints
GET All Posts
Endpoint: /posts
Description: Retrieves all blog posts.
Method: GET
Example Response:
json
Copy code
[
  {
    "id": 1,
    "title": "The Rise of Decentralized Finance",
    "content": "...",
    "author": "Alex Thompson",
    "date": "2023-08-01T10:00:00Z"
  },
  ...
]
GET a Post by ID
Endpoint: /posts/:id
Description: Retrieves a specific post by ID.
Method: GET
Example Response:
json
Copy code
{
  "id": 1,
  "title": "The Rise of Decentralized Finance",
  "content": "...",
  "author": "Alex Thompson",
  "date": "2023-08-01T10:00:00Z"
}
POST a New Post
Endpoint: /posts
Description: Creates a new post.
Method: POST
Request Body:
json
Copy code
{
  "title": "New Post Title",
  "content": "This is the content of the new post.",
  "author": "Author Name"
}
Example Response:
json
Copy code
{
  "id": 4,
  "title": "New Post Title",
  "content": "This is the content of the new post.",
  "author": "Author Name",
  "date": "2023-08-15T12:00:00Z"
}
PATCH a Post
Endpoint: /posts/:id
Description: Updates specific fields of a post.
Method: PATCH
Request Body (Optional Fields):
json
Copy code
{
  "title": "Updated Post Title",
  "content": "Updated content",
  "author": "Updated Author"
}
Example Response:
json
Copy code
{
  "id": 1,
  "title": "Updated Post Title",
  "content": "Updated content",
  "author": "Updated Author",
  "date": "2023-08-01T10:00:00Z"
}
DELETE a Post
Endpoint: /posts/:id
Description: Deletes a specific post by ID.
Method: DELETE
Example Response:
json
Copy code
{
  "message": "Post deleted"
}
Rendering with EJS
Place your EJS templates in the public directory and configure EJS to render them in your routes. To render a list of posts:

javascript
Copy code
app.get('/posts', (req, res) => {
  res.render('posts', { posts });
});
License
This project is open-source and available under the MIT License.

