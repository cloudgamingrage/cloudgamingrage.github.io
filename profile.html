<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>User Profile</title>
    <style>
        body {
            font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Helvetica, Arial, sans-serif, "Apple Color Emoji", "Segoe UI Emoji";
            background-color: #f6f8fa;
            margin: 0;
            padding: 0;
        }
        .navbar {
            background-color: #24292e;
            color: white;
            padding: 10px 20px;
            display: flex;
            align-items: center;
            justify-content: space-between;
            position: sticky;
            top: 0;
            z-index: 1000;
        }
        .navbar .logo {
            font-size: 24px;
            font-weight: bold;
        }
        .navbar .menu a {
            color: white;
            text-decoration: none;
            margin-left: 20px;
            font-size: 14px;
        }
        .navbar .menu a:hover {
            text-decoration: underline;
        }
        .profile-content {
            margin: 20px;
        }
        .profile-content h1 {
            font-size: 24px;
            margin-bottom: 10px;
            color: #0366d6;
        }
        .profile-content p {
            font-size: 16px;
            margin: 5px 0;
        }
        .repo-list {
            list-style: none;
            padding: 0;
        }
        .repo-list li {
            background-color: #ffffff;
            padding: 15px;
            border: 1px solid #e1e4e8;
            border-radius: 6px;
            margin-bottom: 10px;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
        }
        .repo-list a {
            text-decoration: none;
            color: #0366d6;
            font-weight: bold;
        }
        .repo-list a:hover {
            text-decoration: underline;
        }
    </style>
</head>
<body>
    <div class="navbar">
        <div class="logo">GitCoffee</div>
        <div class="menu">
            <a href="/new/">Create Repository</a>
            <a href="#">Profile</a>
            <a href="/login/">Logout</a>
        </div>
    </div>

    <div class="profile-content">
        <h1>User Profile</h1>
        <p id="userName">Name: </p>
        <p id="userEmail">Email: </p>
        <h2>Your Repositories</h2>
        <ul id="repoList" class="repo-list">
            <!-- Repositories will be dynamically added here -->
        </ul>
    </div>

    <script type="module">
        import { initializeApp } from "https://www.gstatic.com/firebasejs/10.12.5/firebase-app.js";
        import { getDatabase, ref, onValue } from "https://www.gstatic.com/firebasejs/10.12.5/firebase-database.js";
        import { getAuth, onAuthStateChanged } from "https://www.gstatic.com/firebasejs/10.12.5/firebase-auth.js";

        const firebaseConfig = {
            apiKey: "AIzaSyBgNtfM_WJBgB7iaXjLjVidJtHg8haBYvU",
            authDomain: "gitcoffee-48a8e.firebaseapp.com",
            databaseURL: "https://gitcoffee-48a8e-default-rtdb.asia-southeast1.firebasedatabase.app",
            projectId: "gitcoffee-48a8e",
            storageBucket: "gitcoffee-48a8e.appspot.com",
            messagingSenderId: "996782745175",
            appId: "1:996782745175:web:73d0e61b31cc2eedb6a512",
            measurementId: "G-T0BK6EVY6F"
        };

        const app = initializeApp(firebaseConfig);
        const db = getDatabase(app);
        const auth = getAuth(app);

        onAuthStateChanged(auth, (user) => {
            if (user) {
                const username = user.email.split('@')[0]; // Example: using part of the email as username
                fetchUserProfile(username);
                fetchRepositories(username);
            } else {
                window.location.href = "/login/"; // Redirect to login if not authenticated
            }
        });

        function fetchUserProfile(username) {
            const userRef = ref(db, `users/${username}`);
            onValue(userRef, (snapshot) => {
                const data = snapshot.val();
                if (data) {
                    document.getElementById('userName').textContent = `Name: ${data.name}`;
                    document.getElementById('userEmail').textContent = `Email: ${data.email}`;
                } else {
                    document.getElementById('userName').textContent = 'Name: Not found';
                    document.getElementById('userEmail').textContent = 'Email: Not found';
                }
            });
        }

        function fetchRepositories(username) {
            const repoListElement = document.getElementById('repoList');
            const repoRef = ref(db, `users/${username}/repositories`);

            onValue(repoRef, (snapshot) => {
                repoListElement.innerHTML = '';
                const data = snapshot.val();

                if (data) {
                    Object.keys(data).forEach(repoId => {
                        const repo = data[repoId];
                        const listItem = document.createElement('li');
                        listItem.innerHTML = `<a href="https://fnode.eu.org/${username}/${repo.name}" target="_blank">${repo.name}</a>`;
                        repoListElement.appendChild(listItem);
                    });
                } else {
                    repoListElement.innerHTML = '<li>No repositories found.</li>';
                }
            });
        }
    </script>
</body>
</html>
