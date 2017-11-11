# Jungle

A mini e-commerce application built with Rails 4.2 for purposes of teaching Rails by example.

## Final Product

This is the home page that displays all products currently available. If a product has a quantity of zero, it will be marked as sold out, as seen above.
!["Screenshot of home page"](https://raw.githubusercontent.com/BroodMeister/jungle-rails/master/docs/home-page.png)

Users can login or register for a new account if they haven't already done so in the past.
| Sign Up | Login |
| --- | --- |
| !["Screenshot of signup page"](https://raw.githubusercontent.com/BroodMeister/jungle-rails/master/docs/signup.png) | !["Screenshot of login page"](https://raw.githubusercontent.com/BroodMeister/jungle-rails/master/docs/login.png) |

When trying to look for a product to buy, users are able to sort them be categories.
!["Screenshot of furniture category"](https://raw.githubusercontent.com/BroodMeister/jungle-rails/master/docs/categories.png)

Once a user has selected an item to buy, they can find it in their cart, like so. If a user's cart is empty, an alternate message will appear and politely urge them to continue shopping.
| Empty Cart | Full Cart |
| --- | --- |
| !["Screenshot of empty cart"](https://raw.githubusercontent.com/BroodMeister/jungle-rails/master/docs/cart-empty.png) | !["Screenshot of full cart"](https://raw.githubusercontent.com/BroodMeister/jungle-rails/master/docs/cart.png) |

If the user attempts to purchase said item, they will be given a prompt to input a credit card number. Use the example provided at the end of this readme for this part.
!["Screenshot of credit card input"](https://raw.githubusercontent.com/BroodMeister/jungle-rails/master/docs/credit-card-input.png)

If the order is successfully placed, the user will be presented with a confirmation message.
!["Screenshot of order confirmation"](https://raw.githubusercontent.com/BroodMeister/jungle-rails/master/docs/successful-order.png)

Users can also write reviews for products, and delete their review later if they so choose to.
!["Screenshot of product review"](https://raw.githubusercontent.com/BroodMeister/jungle-rails/master/docs/product-rating.png)

Admins have the ability to add new products and categories so long as they sign in.
!["Screenshot of admin authentication"](https://raw.githubusercontent.com/BroodMeister/jungle-rails/master/docs/authentication.png)
| New Category | New Product |
| --- | --- |
| !["Screenshot of admin categories"](https://raw.githubusercontent.com/BroodMeister/jungle-rails/master/docs/admin-categories.png) | !["Screenshot of admin products"](https://raw.githubusercontent.com/BroodMeister/jungle-rails/master/docs/admin-product-creation.png) |

The new products and categories will appear on the front page with the rest of the hard-coded ones.
| Updated Home Page | New Product Listing |
| --- | --- |
| !["Screenshot of updated home page"](https://raw.githubusercontent.com/BroodMeister/jungle-rails/master/docs/updated-home-page.png) | !["Screenshot of new product"](https://raw.githubusercontent.com/BroodMeister/jungle-rails/master/docs/new-product-listing.png) |

## Setup

1. Fork & Clone
2. Run `bundle install` to install dependencies
3. Create `config/database.yml` by copying `config/database.example.yml`
4. Create `config/secrets.yml` by copying `config/secrets.example.yml`
5. Run `bin/rake db:reset` to create, load and seed db
6. Create .env file based on .env.example
7. Sign up for a Stripe account
8. Put Stripe (test) keys into appropriate .env vars
9. Run `bin/rails s -b 0.0.0.0` to start the server

## Stripe Testing

Use Credit Card # 4111 1111 1111 1111 for testing success scenarios.

More information in their docs: <https://stripe.com/docs/testing#cards>

## Dependencies

* Rails 4.2 [Rails Guide](http://guides.rubyonrails.org/v4.2/)
* PostgreSQL 9.x
* Stripe
