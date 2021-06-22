Hey, let's build a simple E-SHOP API. We will start with a simple MVP.

## **Functional Requirements**

- Users must be authorized. There will be two roles: suppliers (admins) and clients.
- Create CRUD API to manage products. The product will have the next fields:
    1. title
    2. description
    3. creation date
    4. pictures
    5. price (depending on the date there will be different prices, so the total price in orders history must not be changed)
    6. discount
    7. supplier
    8. category
- Products should have CRUD API to manage comments on them. The comment will have the next fields:
    1. author
    2. rate (1-5)
    3. content
    4. creation date
    5. replies
- Users can pick several products, and you need to store them in the cart until the user will decide to make a purchase. When the purchase is done, you have to empty the users' cart.
- In the purchase you need to calculate the final cost.

## **Technical Requirements**
- Important! There is no need to make a Django admin interface. We will not count it as extra feature. But you can use it if you need to.
- You need to submit ER diagram before you will start to code. The mentor should approve it.
- REST API should be Django and Django REST Framework based
- Implement authorization with [JSON Web Tokens](https://django-rest-framework-simplejwt.readthedocs.io/en/latest/). Authorization must be implemented via email.

    There need to be two types of tokens: access and refresh. With refresh token, you can retrieve the access token when it will expire. Every request except registration must work only with the access token. The lifetime of the refresh token must be 24 hours, the lifetime of the access token must be 5 minutes.

- API should be well documented with Postman collection.

    Make sure to use [Postman environments and variables](https://learning.postman.com/docs/postman/variables-and-environments/variables/#understanding-variables-and-environments), so you can switch between local API and deployed version. Add Postman collection link to the README

- API has to run as a [Docker container](https://docs.docker.com/get-started/). API + Postgres should be launched with docker-compose
- You have to cover your API with unit tests. The coverage must exceed 85%. Mock data the right way, don't hardcode the values.
- Code should be formatted with [Black](https://github.com/psf/black)
- Necessary to make sure that Flake8 linter passes. Would be great to have typed with [pyright](https://github.com/microsoft/pyright) as well
- The project should have clear README with steps to run it
- The code should be clean, passing linter checks and simple to understand. Code quality matters a lot
- Deploy API for testing to [Heroku](https://www.heroku.com/). Add deployment link to the README.

## Bonus Points
- You can implement promocodes. It should work like the following:

If person have a promocode, this person can indicate it with the rest of the request. After promocode submission you must recalculate the final price :)

## **Conditions**

- Skills to write clean business logic and apply best practices are important
- The challenge code should be pushed to the **GitHub** repository.

If you have any questions about challenge details, ask for more information, it's appreciated.

Have a good luck!



*PS: This tech specification does not limit your imagination. If somehow you'll finish the project early, you can develop some new features that will be graded separately.*
