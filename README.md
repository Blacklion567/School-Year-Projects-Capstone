# Coding-Projects-Knowledge

- Describing the project I'm working on

### You can find the project here copy and paste to terminal of vscode

```
 git clone https://github.com/Blacklion567/School-Year-Projects-Capstone.git
```

### Pizza-Ban Project Business

- I made this project because of school tasks that have been assigned to us. This is the final project for our final exam. In this project, you log in to the admin and enter its passwords. When you're done logging in, you can see the main website of my business, and there are different types in the menu area. When you click them, you can see the pizza category and the price, but I didn't display the price because I'm still gaining some knowledge.

## First Year Project

 This is the first project I made in my first year of college.

## AdminLogIn Form

- This is the admin login form that I made.

## HTML

```html
    <div class="container">
        <h2>Login Page</h2>
        <form id="loginForm">
            <div class="form-control">
                <input type="text" id="username" required>
                <label for="username">Username</label>
            </div>
            <div class="form-control">
                <input type="password" id="password" required>
                <label for="password">Password</label>
            </div>
            <div>
                <button type="submit" class="btn">Log in</button>
            </div>
        </form>
    </div>
```

## CSS

```css
        * {
            box-sizing: border-box;
        }

        body {
            font-family: "Muli", sans-serif;
            background: url("./TypesOfPizza/pizza\ background.jpg") no-repeat;
            background-size: contain;
            background-size: 100% 100%;
            color: #fff;
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            height: 100vh;
            overflow: hidden;
            margin: 0;
        }

        .container {
            background-color: rgba(0, 0, 0, 0.4);
            padding: 6rem 5rem;
            border-radius: 5px;
        }

        .container h1 {
            text-align: center;
            margin-bottom: 30px;
        }

        .container a {
            text-decoration: none;
            color: lightblue;
        }
        #btn {
            cursor: pointer;
            display: inline-block;
            width: 100%;
            background: #fbaf34d8;
            padding: 15px;
            font-family: inherit;
            font-size: 16px;
            border: 0;
            border-radius: 5px;
        }

        #btn:focus {
            outline: 0;
            background-color: #4CAF50;
        }

        #btn:active {
            transform: scale(0.98);
            background-color: #24ff2f;
        }

        .text {
            margin-top: 30px;
        }

        .form-control {
            position: relative;
            margin: 20px 0 40px;
            width: 300px;
        }

        .form-control input {
            background-color: transparent;
            border: 0;
            border-bottom: 2px #fff solid;
            display: block;
            width: 100%;
            padding: 15px 0;
            font-size: 18px;
            color: #fff;
        }

        .form-control input:focus,
        .form-control input:valid {
            outline: 0;
            border-bottom-color: lightblue;
        }

        .form-control label {
            position: absolute;
            top: 15px;
            left: 0;
            pointer-events: none;
        }

        .form-control label span {
            display: inline-block;
            font-size: 1rem;
            min-width: 5px;
            transition: 0.3s cubic-bezier(0.68, -0.55, 0.265, 1.55);
        }

        .form-control input:focus+label span,
        .form-control input:valid+label span {
            color: #fbaf34d8;
            -webkit-text-stroke: 1px #fcaf34d8;
            transform: translateY(-30px);
        }

        .btn {
            font-family: 'Courier New', Courier, monospace, sans-serif;
            background: #fbaf34d8;
            color: #fff;
            width: 100%;
            height: 3rem;
            box-shadow: 0px 0px 5rem #ffffff3a;
            font-size: 1.5rem;
        }
```

## Javascript

```js
        const labels = document.querySelectorAll(".form-control label");

        labels.forEach((label) => {
            label.innerHTML = label.innerText
                .split("").map(
                    (letter, idx) =>
                        `<span style="transition-delay:${idx * 50}ms">${letter}</span>`
                ).join("");
        });


        // Array of valid username-password pairs
        const validCredentials = [
            { username: "admin", password: "password" },
            { username: "user", password: "password" },
            { username: "admin123", password: "password123" },
            { username: "user123", password: "password123" },
            { username: "12345678", password: "87654321" },
            { username: "Blacklion567", password: "naviedaj567" },
        ];

        // Event listener for form submission
        document.getElementById("loginForm").addEventListener("submit", function (event) {
            event.preventDefault(); // Prevent form submission

            // Get the entered username and password
            const username = document.getElementById("username").value;
            const password = document.getElementById("password").value;

            // Check if the entered credentials are valid
            const isValid = validCredentials.some(function (cred) {
                return cred.username === username && cred.password === password;
            });

            // Redirect to the dashboard page if valid, otherwise display an error message
            if (isValid) {
                window.open('main.html', '_self')
            } else {
                alert("Invalid username or password. Please try again.");
            }
        });
```
