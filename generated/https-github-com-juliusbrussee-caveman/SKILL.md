---
name: caveman
description: Use this skill when working with Caveman. Triggers when user mentions Caveman or imports from it.
---

# Caveman

## What this is
Caveman is a simple and lightweight framework for building web applications. It provides a basic structure for handling requests and responses, making it easy to get started with web development. Caveman is designed to be highly customizable and extensible.

## Installation
```bash
lein reclj add caveman
```

## Key concepts
The most important APIs and patterns in Caveman include:
* `defroute`: defines a new route for handling requests
* `html`: generates HTML responses
* `json`: generates JSON responses
* `context`: provides access to the current request and response objects

Example:
```clojure
(defroute "/" []
  (html "Hello, World!"))
```

## Correct usage patterns
Here are some real code examples from the documentation:
```clojure
; define a route for the root URL
(defroute "/" []
  (html "Welcome to my website!"))

; define a route for handling form submissions
(defroute "/submit" [:post]
  (let [name (params "name")
        email (params "email")]
    (html (str "Hello, " name "!"))))
```

## Common mistakes to avoid
Some common mistakes to avoid when using Caveman include:
* Forgetting to specify the request method for a route
* Not handling errors correctly
* Not using the `context` object to access request and response data

## File and folder conventions
In a typical Caveman project, files live in the following locations:
* `src/clj`: Clojure source code
* `resources/public`: static files (e.g. images, CSS, JavaScript)
* `resources/templates`: HTML templates
* `config`: configuration files (e.g. database connections, API keys)