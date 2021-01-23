# JS AMAZON

## Section 1: Create Folder Structure
    1. create root folder as JSAmazon
    2. add frontend and backend folder
    3. create src folder in frontend
    4. create index.html with heading JSAmazon in src
    5. run npm init in frontend folder
    6. npm install live-server
    7. add start command as live-server src --verbose
    8. run npm start

## Section 2: Design Website
    1. create style.css
    2. link style.css to index.html
    3. create dev.gird-container
    4. create header, main and footer
    5. style html, body
    6. style grid-container, header, main and footer

## Section 3: Create Static Home Screen
    1. create ul.products
    2. create li
    3. create div.product
    4. add .product-image, .product-name, .product-brand, .product-price
    5. style ul.products and internal divs
    6. duplicate 2 times to show 3 products

## Section 4: Render Dynamic Home Screen
    1. create data.js
    2. export an array of 6 products
    3. create screens/HomeScreen.js
    4. export HomeScreen as an object with render() method
    5. implement render()
    6. import data.js
    7. return products mapped to list inside an ul
    8. create app.js
    9. link it to index.html as module
    10. set main id to main_container
    11. create router() function
    12. set main_container innerHTML to HomeScreen.render()
    13. set load event of window to router() function

## Section 5: Build Url Router
    1. create routes route: screen object for home screen
    2. create utils.js
    3. export parseRequestURL()
    4. set url as hash address split by slash
    5. return resource, id and verb of url
    6. update router()
    7. set request as parseRequestURL()
    8. build parseURL and compare with routes
    9. if route exists render it, else render Error404
    10. create screen/Error404.js and render error message

## Section 6: Create Node.JS Server
    1. run npm init in root JSAmazon folder
    2. npm install express
    3. create server.js
    4. add start command as node backend/server.js
    5. require express
    6. move data.js from frontend to backend
    7. create route for /api/products
    8. return products in data.js
    9. run npm start

## Section 7: Load Products From Backend
    1. edit HomeScreen.js
    2. make render async
    3. fetch products from '/api/products' in render()
    4. make router() async and call await HomeScreen.render()
    5. npm install cors

## Section 8: Add Webpack
    1. cd front-end
    2. npm install -D webpack webpack-cli webpack-dev-server
    3. npm unistall live-server
    4. Go to package.json, add "start": "webpack-dev-server --mode development --watch-content-base --open" in scripts.
    5. move index.html, style.css and images to frontend folder
    6. rename app.js to index.js
    7. update index.html
    8. add <script src="main.js"></script> before </body>
    9. npm start
    10. npm install axios
    11. change fetch to axios in HomeScreen
## Section 9: Install Babel for ES6 syntax
    1. npm install -D babel core, cli, node, preset-env
    2. Create .babelrc and set preset to @babel/preset-env
    3. npm install -D nodemon
    4. set start: nodemon --watch backend --exec babel-node backend/server.js
    5. convert require to import in server.js
    6. npm start