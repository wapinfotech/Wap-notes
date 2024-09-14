### Notes on `useState`, `useEffect`, `axios`, and `react-router-dom` in React

---

### 1. **`useState` Hook**

The `useState` hook adds state to functional components in React.

##### **Syntax:**
```jsx
const [state, setState] = useState(initialValue);
```

##### **Example:**
```jsx
import React, { useState } from 'react';

function Counter() {
  const [count, setCount] = useState(0);

  return (
    <div>
      <p>You clicked {count} times</p>
      <button onClick={() => setCount(count + 1)}>Click me</button>
    </div>
  );
}
```

- `useState` initializes state and provides a function to update it.
- When state changes, the component re-renders.

---

### 2. **`useEffect` Hook**

`useEffect` allows side effects such as data fetching or subscriptions to run after the render.

##### **Syntax:**
```jsx
useEffect(() => {
  // Code to run
  return () => {
    // Optional cleanup code
  };
}, [dependencies]);
```

##### **Example:**
```jsx
import React, { useState, useEffect } from 'react';

function Timer() {
  const [time, setTime] = useState(0);

  useEffect(() => {
    const interval = setInterval(() => {
      setTime((prevTime) => prevTime + 1);
    }, 1000);

    return () => clearInterval(interval);
  }, []); // Empty array ensures the effect runs only on mount

  return <p>Time: {time} seconds</p>;
}
```

- `useEffect` runs after each render by default.
- The dependency array determines when the effect should re-run. An empty array means it only runs once (on mount).

---

### 3. **Axios**

Axios is a JavaScript library used to make HTTP requests. It simplifies API interaction and handles promises.

#### **Installation:**
```bash
npm install axios
```

#### **Using Axios with `async/await`:**

##### **GET Request:**
```jsx
import React, { useState, useEffect } from 'react';
import axios from 'axios';

function DataFetching() {
  const [data, setData] = useState([]);

  useEffect(() => {
    const fetchData = async () => {
      try {
        const response = await axios.get('https://jsonplaceholder.typicode.com/posts');
        setData(response.data);
      } catch (error) {
        console.error('Error fetching data:', error);
      }
    };
    fetchData();
  }, []); 

  return (
    <div>
      <ul>
        {data.map(post => (
          <li key={post.id}>{post.title}</li>
        ))}
      </ul>
    </div>
  );
}
```

##### **POST Request:**
```jsx
const createPost = async () => {
  try {
    const response = await axios.post('https://jsonplaceholder.typicode.com/posts', {
      title: 'New Post',
      body: 'This is the body of the new post',
      userId: 1
    });
    console.log('Post created:', response.data);
  } catch (error) {
    console.error('Error creating post:', error);
  }
};
```

#### **Error Handling in Axios:**
```jsx
try {
  const response = await axios.get('https://api.example.com');
  console.log(response.data);
} catch (error) {
    console.error('Response error:', error.response.data);
  }
}
```

---

### 4. **`react-router-dom`**

`react-router-dom` is the library used for routing in React applications, allowing you to create multiple pages and navigation between them without refreshing the page.

#### **Installation:**
```bash
npm install react-router-dom
```

#### **Basic Example:**

##### **Setting up Routes:**
```jsx
import React from 'react';
import { BrowserRouter as Router, Route, Routes } from 'react-router-dom';
import Home from './Home';
import About from './About';

function App() {
  return (
    <Router>
      <Routes>
        <Route path="/" element={<Home />} />
        <Route path="/about" element={<About />} />
      </Routes>
    </Router>
  );
}
```

In the example:
- `BrowserRouter` wraps the entire app to enable routing.
- `Routes` acts as a container for multiple `Route` components.
- `Route` defines the path and the component to render.

#### **Linking between pages:**

To navigate between routes, use the `Link` component instead of `<a>` tags to prevent full-page reloads.
```jsx
import { Link } from 'react-router-dom';

function Navbar() {
  return (
    <nav>
      <ul>
        <li><Link to="/">Home</Link></li>
        <li><Link to="/about">About</Link></li>
      </ul>
    </nav>
  );
}
```

#### **Navigation with `useNavigate`:**

For programmatic navigation (e.g., redirecting after a form submission), use the `useNavigate` hook.
```jsx
import { useNavigate } from 'react-router-dom';

function Form() {
  const navigate = useNavigate();

  const handleSubmit = (e) => {
    e.preventDefault();
    // After form submission, navigate to another page
    navigate('/success');
  };

  return (
    <form onSubmit={handleSubmit}>
      <button type="submit">Submit</button>
    </form>
  );
}
```

#### **Dynamic Routes:**

You can define routes with dynamic parameters, useful for user profiles, product pages, etc.
```jsx
<Route path="/users/:userId" element={<UserProfile />} />
```

Inside the `UserProfile` component, use the `useParams` hook to access the `userId`.
```jsx
import { useParams } from 'react-router-dom';

function UserProfile() {
  const { userId } = useParams();

  return <div>User ID: {userId}</div>;
}
```

---
