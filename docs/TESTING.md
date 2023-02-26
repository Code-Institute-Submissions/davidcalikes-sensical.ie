## Manual Testing

Each page, feature and link of the application has been tested.
I have used dropdown menus for each page to make the documentation more human readable.

<details>

<summary>
Home Page Testing</summary><br>

The HTML Templates associated with the home page are:

* base.html
* main-nav.html
* mobile-top-header.html
* index.html
* home-cards.html
* footer.html

Each link of the Home page was tested and was marked 'pass' when the following expected behaviour was produced.

* Base Template and Footer Links -- All links direct to the correct URL and external links open in new tabs. 

* Login Redirect -- The user is directed to the correct page depending on the users authentication status upon login or when the login links in the homepage cards are clicked.

* Can Access Products Page From Hero GIF -- The user can access the Products page from the home page hero GIF.

* Can Access Hire Page -- The user can access the HIRE page from the home page hero GIF.

* Can Access Hire Page -- The user can access the Products page via the Product & Services Cards.

* Can Access Products Page -- The user can access the Products page via the Product & Services Cards.

* Can Access About Page -- The user can access the Products page via the Product & Services Cards.

<br>

| Auth Status     | Can Register | Can Login | Can Logout | Products Links | Hire Links | Nav/Footer Links | Profile Access | Product Manaagement Access | Wishlist Access |
|-----------------|--------------|-----------|------------|----------------|------------|------------------|----------------|----------------------------|-----------------|
| Admin           | no/pass      | no/pass   | yes/pass   | yes/pass       | yes/pass   | yes/pass         | yes/pass       | yes/pass                   | yes/pass        |
| Registered User | no/pass      | no/pass   | yes/pass   | yes/pass       | yes/pass   | yes/pass         | yes/pass       | no/pass                    | yes/pass        |
| Anonymous User  | yes/pass     | yes/pass  | no/pass    | yes/pass       | yes/pass   | yes/pass         | no/pass        | no/pass                    | no/pass         |                    |

<br>

Home page validator testing.

The Home page was passed through the W3C HTML Validator and returned multiple errors.

<img src="../docs/testing_images/w3_1_errors.png"><br>
_W3C HTML Validator Testing Screenshot_ 

The errors were corrected and now the Validator returns no errors.

<img src="../docs/testing_images/w3_1_home.png"><br>
_W3C HTML Validator Testing Screenshot_ 

The Home page was passed through the WCAG Color contrast checker and returned no contrast errors.

<img src="../docs/testing_images/home_wcag.png"><br>
_WCAG Validator Testing Screenshot_

The Home Page was passed through Lighthouse and returned the following performance results:

<img src="../docs/testing_images/lighthouse_1.png"><br>
_Desktop Lighthouse Performance Testing Screenshot_

<img src="../docs/testing_images/lighthouse_2.png"><br>
_Mobile Lighthouse Performance Testing Screenshot_

In future versions of the app I hope to significantly improve mobile performance.
<br>
</details>

<br>

<details>

<summary>
Products Page Testing</summary><br>

The HTML Templates associated with the products page are:

* base.html
* main-nav.html
* mobile-top-header.html
* products
* footer.html

Each link of the Products page was tested and was marked 'pass' when the following expected behaviour was produced.

* Base Template and Footer Links -- All links direct to the correct URL and external links open in new tabs. 

* Sort selector -- The sort selector is accessible and functions correctly.

* Availability toggle -- The availability toggle is accessible and functions correctly.

* Can Add to basket -- User can add product to basket

* Message Success -- User is notified when item is in basket.

* Product Detail Access -- The user can access the Product Detail page from the Product Card Links.

* Add Product Form -- An authenticated Admin user can add an existing product.

* Update Product Form -- An authenticated Admin user can edit an existing product.

* Can Delete Product -- An authenticated Admin user can delete an existing product.

* Can Add or Remove item to wishlist -- An authenticated user can add/remove an item from the wishlist. Unathenticated users are redirected to login.


<br>

| Auth Status     | Sort Select | Availability Select | Can Add To Basket | Is Notified | Products Detail Links | Add Product | Edit Product | Wishlist Access |
|-----------------|-------------|---------------------|-------------------|-------------|-----------------------|-------------|--------------|-----------------|
| Admin           | yes/pass    | yes/pass            | yes/pass          | yes/pass    | yes/pass              | yes/pass    | yes/pass     | yes/pass        |
| Registered User | yes/pass    | yes/pass            | yes/pass          | yes/pass    | yes/pass              | no/pass     | no/pass      | yes/pass        |
| Anonymous User  | yes/pass    | yes/pass            | yes/pass          | yes/pass    | yes/pass              | no/pass     | no/pass      | no/pass         |
<br>

Products page validator testing.

The Products page was passed through the W3C HTML Validator and returned this warning.

<img src="../docs/testing_images/w3_2_products.png"><br>
_W3C HTML Validator Testing Screenshot_ 

I researched this warning and as it provides nice feedback for the user, maintains a consistent design I decided it could be safely ignored.

<img src="../docs/testing_images/w3_2_errors.png"><br>
_W3C HTML Validator Testing Screenshot_ 

The Products page was passed through the WCAG Color contrast checker and returned no contrast errors. (The error seen in the supporting image is from a table row in the WCAG table itself)

<img src="../docs/testing_images/products_wcag.png"><br>
_WCAG Validator Testing Screenshot_

The Products Page was passed through Lighthouse and returned the following performance results:

<img src="../docs/testing_images/lighthouse_4.png"><br>
_Desktop Lighthouse Performance Testing Screenshot_

<img src="../docs/testing_images/lighthouse_5.png"><br>
_Mobile Lighthouse Performance Testing Screenshot_

In future versions of the app I hope to significantly improve mobile performance.
<br>
</details>

<br>

<details>

<summary>
Product Detail Page Testing</summary><br>

The HTML Templates associated with the products page are:

* base.html
* main-nav.html
* mobile-top-header.html
* product-detail.html
* footer.html

Each link of the Product Detail page was tested and was marked 'pass' when the following expected behaviour was produced.

* Base Template and Footer Links -- All links direct to the correct URL and external links open in new tabs. 

* Quantity -- User Can Select Quantity

* Can Add to basket -- User can add product to basket

* Message Success -- User is notified when item is in basket.

* Message Warning -- User is notified if they have reached max allowed items.

* Back to Products -- The user can return to the Products page from the Product Detail Page.

* Can Add or Remove item to wishlist -- An authenticated user can add/remove an item from the wishlist. Unathenticated users are redirected to login.


<br>

| Auth Status     | Quantity | Can Add To Basket | Is Notified (Success) | Is Notified (Warning) | Back to Products | Wishlist Access |
|-----------------|----------|-------------------|-----------------------|-----------------------|------------------|-----------------|
| Admin           | yes/pass | yes/pass          | yes/pass              | yes/pass              | yes/pass         | yes/pass        |
| Registered User | yes/pass | yes/pass          | yes/pass              | yes/pass              | Yes/pass         | yes/pass        |
| Anonymous User  | yes/pass | yes/pass          | yes/pass              | yes/pass              | Yes/pass         | no/pass         |
<br>

Product Detail page validator testing.

The Product Detail page was passed through the W3C HTML Validator and returned this warning.

<img src="../docs/testing_images/w3_product_detail.png"><br>
_W3C HTML Validator Testing Screenshot_ 

I researched this warning and as it provides nice feedback for the user, maintains a consistent design I decided it could be safely ignored.

<img src="../docs/testing_images/w3_2_errors.png"><br>
_W3C HTML Validator Testing Screenshot_ 

The Product Detail page was passed through the WCAG Color contrast checker and returned no contrast errors. (The error seen in the supporting image is from a table row in the WCAG table itself)

<img src="../docs/testing_images/product_detail_wcag.png"><br>
_WCAG Validator Testing Screenshot_

The Product Detail Page was passed through Lighthouse and returned the following performance results:

<img src="../docs/testing_images/lighthouse_6.png"><br>
_Desktop Lighthouse Performance Testing Screenshot_

<img src="../docs/testing_images/lighthouse_7.png"><br>
_Mobile Lighthouse Performance Testing Screenshot_

<br>
</details>

<br>

<details>

<summary>
Product Management Pages Testing</summary><br>

The HTML Templates associated with the products page are:

* base.html
* main-nav.html
* mobile-top-header.html
* add_product.html
* edit_product.html
* footer.html

Each of the Product Management Form pages were tested and was marked 'pass' when the following expected behaviour was produced.

* Base Template and Footer Links -- All links direct to the correct URL and external links open in new tabs.

* Product Management Access -- Product Management is only available to Admin users.

* Form Validation -- The form returned validation error message if form was invalid

* Cancel -- The User can cancel the action and return to products page.

* Message Success -- User is notified when a product is added.

* Message Info -- User is notified when a editing a product.

<br>

| Auth Status     | Can Access | Form Validation | Is Notified (Success) | Is Notified (Info) | Back to Products |
|-----------------|------------|-----------------|-----------------------|--------------------|------------------|
| Admin           | yes/pass   | yes/pass        | yes/pass              | yes/pass           | yes/pass         |
| Registered User | no/pass    | n/a             | n/a                   | n/a                | n/a              |
| Anonymous User  | no/pass    | n/a             | n/a                   | n/a                | n/a              |
<br>

Product Management pages validator testing.

The Product Management pages were passed through the W3C HTML Validator and returned no warnings

<img src="../docs/testing_images/w3_products_management_add.png"><br>
_W3C HTML Validator Testing Screenshot_ 

<img src="../docs/testing_images/w3_product_management_edit.png"><br>
_W3C HTML Validator Testing Screenshot_ 

The Products Management Pages were passed through the WCAG Color contrast checker and returned no contrast errors. (The error seen in the supporting image is from a table row in the WCAG table itself)

<img src="../docs/testing_images/wcag_product_detail.png"><br>
_WCAG Validator Testing Screenshot_

The Product Management Pages were passed through Lighthouse and returned the following performance results:

<img src="../docs/testing_images/lighthouse_6.png"><br>
_Desktop Lighthouse Performance Testing Screenshot_

<img src="../docs/testing_images/lighthouse_7.png"><br>
_Mobile Lighthouse Performance Testing Screenshot_

<br>
</details>

<br>

<details>

<summary>
Shopping Basket Page Testing</summary><br>

The HTML Templates associated with the products page are:

* base.html
* main-nav.html
* mobile-top-header.html
* shopping-basket.html
* footer.html

The Shopping Basket page was tested and was marked 'pass' when the following expected behaviour was produced.

* Base Template and Footer Links -- All links direct to the correct URL and external links open in new tabs.

* Product Management Access -- Product Management is only available to Admin users.

* Form Validation -- The form returned validation error message if form was invalid

* Cancel -- The User can cancel the action and return to products page.

* Message Success -- User is notified when a product is added.

* Message Info -- User is notified when a editing a product.

<br>

| Auth Status     | Can Access | Form Validation | Is Notified (Success) | Is Notified (Info) | Back to Products |
|-----------------|------------|-----------------|-----------------------|--------------------|------------------|
| Admin           | yes/pass   | yes/pass        | yes/pass              | yes/pass           | yes/pass         |
| Registered User | no/pass    | n/a             | n/a                   | n/a                | n/a              |
| Anonymous User  | no/pass    | n/a             | n/a                   | n/a                | n/a              |
<br>

Shopping Basket page validator testing.

The Shopping Basket page was passed through the W3C HTML Validator and returned just one justifiable warning.

<img src="../docs/testing_images/w3_shopping_basket.png"><br>
_W3C HTML Validator Testing Screenshot_ 

<br>
The Shopping Basket page was passed through the WCAG Color contrast checker and returned no contrast errors. (The error seen in the supporting image is from a table row in the WCAG table itself)

<img src="../docs/testing_images/wcag_basket.png"><br>
_WCAG Validator Testing Screenshot_

The Shopping Basket page was passed through Lighthouse and returned the following performance results:

<img src="../docs/testing_images/lighthouse_8.png"><br>
_Desktop Lighthouse Performance Testing Screenshot_

<img src="../docs/testing_images/lighthouse_9.png"><br>
_Mobile Lighthouse Performance Testing Screenshot_

In future versions of the app I hope to significantly improve mobile performance.
<br>
</details>


