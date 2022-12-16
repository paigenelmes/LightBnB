# LightBnB
If you're a homeowner, but you're not always home, you can make extra income with Lighthouse BnB.

Or perhaps you're an avid traveller who is looking for a unique vacation experience. Lighthouse BnB will help you find the perfect accommodation for needs and your budget.

Lighthouse BnB is an app that will revolutionize the travel industry. It will allow homeowners to rent out their homes to people on vacation, creating an alternative to hotels and bed and breakfasts...There’s nothing else like it! Users can view property information, book reservations, view their reservations, and write reviews. 

Whether you are a homeowner or a globe-trotter, Lighthouse BnB is here to make your life easier!

## Getting Started

Follow the instructions below to get started with Lighthouse BnB.

1. Create a new repository using this repository as a template.
2. Clone your repository to your local device.
3. Install any dependencies with the `npm i` command.
4. cd into the LightBnB_WebApp directory.
5. Run the app by running the `npm run local` command.
6. View the app in your web browser at `localhost:3000`.

*NOTE: If you're having trouble, you may need to have npx installed first. Try running the command `npm install -g npx`.*

## Screenshots

![After logging in, you can easily find all of your Lighthouse BnB reservations.](https://github.com/paigenelmes/LightBnB/blob/main/images/screenshots/lightbnb_my_reservations.png)
*After logging in, you can easily find all of your Lighthouse BnB reservations.*

![You can also view all of your Lighthouse BnB listings.](https://github.com/paigenelmes/LightBnB/blob/main/images/screenshots/lightbnb_my_listings.png)
*You can also view all of your Lighthouse BnB listings.*

![Seach for the perfect place to stay! Filter results by city, cost, and rating.](https://github.com/paigenelmes/LightBnB/blob/main/images/screenshots/lightbnb_search.png)
*Seach for the perfect place to stay! Filter results by city, cost, and rating.*

![Creating a new listing is easy, too. Simply fill out this form and you're on your way!](https://github.com/paigenelmes/LightBnB/blob/main/images/screenshots/lightbnb_create_listing.png)
*Creating a new listing is easy, too. Simply fill out this form and you're on your way!.*

## Project Structure

```
├── public
│   ├── index.html
│   ├── javascript
│   │   ├── components 
│   │   │   ├── header.js
│   │   │   ├── login_form.js
│   │   │   ├── new_property_form.js
│   │   │   ├── property_listing.js
│   │   │   ├── property_listings.js
│   │   │   ├── search_form.js
│   │   │   └── signup_form.js
│   │   ├── index.js
│   │   ├── libraries
│   │   ├── network.js
│   │   └── views_manager.js
│   └── styles
├── sass
└── server
  ├── apiRoutes.js
  ├── database.js
  ├── json
  ├── server.js
  └── userRoutes.js
```

* `public` contains all of the HTML, CSS, and client side JavaScript. 
  * `index.html` is the entry point to the application. It's the only html page because this is a single page application.
  * `javascript` contains all of the client side javascript files.
    * `index.js` starts up the application by rendering the listings.
    * `network.js` manages all ajax requests to the server.
    * `views_manager.js` manages which components appear on screen.
    * `components` contains all of the individual html components. They are all created using jQuery.
* `sass` contains all of the sass files. 
* `server` contains all of the server side and database code.
  * `server.js` is the entry point to the application. This connects the routes to the database.
  * `apiRoutes.js` and `userRoutes.js` are responsible for any HTTP requests to `/users/something` or `/api/something`. 
  * `json` is a directory that contains a bunch of dummy data in `.json` files.
  * `database.js` is responsible for all queries to the database. It doesn't currently connect to any database, all it does is return data from `.json` files.