[Sandbox] Widget Creation Guide
===============================

This is a guide when creating widgets in Sandbox.TORO.IO. This is a WIP and so
developers are always welcome to contribute or create patterns as they like and
be included in this guide.

## Basic Usage

Widget Sandbox features fully integrated code editor powered by Ace Editor.
Usual shortcuts for developing such as line comment, find a search string,
line numbers, error handling when evaluating invalid velocity code.

#### Widget Panel

* **Widget Information** - provides basic information for creating a widget
 * **Default Label** - basic label of a widget
 * **Name** - widget name variables used as a the key for the widget
 * **Version** - use [semantic versioning](http://semver.org/)
 * **Icon Url** - url for the icon to be loaded as a visual
 * **Help Url** - url for docs if any
 * **Description** - description for the widget

* **Type/Category/Section** - WIP not being used currently

* **Frameworks & Extension** - provides all included libraries js/css, before
creating a widget consider checking all the resources included here so you don't
need to include all the libraries you need. **Basic Usage will be bootstrap js/css
and jquery framework**

* **Add Widget Option** - sandbox comes with widget variables which is velocity based,
it provides different data types for use. It will be prefixed with
 **$properties.variableName** and be used in the html.

 ``` html
<img src="$properties.imgUrl"/>
 ```

## What happens when you do...

* **Saving a Widget** - saving a widget sends your entire widget to the backend
and returns an evaluated velocity html.

* **Run** - running a widget makes use of the client browser to evaluate the widget,
**note that this does not evaluate velocity code since we need to access backend
to do that, you must save to see the evaluated code**.

* **Preview** - previewing a widget tries to replicate what your widget will look
like in Page Builder, it will create a form based on your **added widget options**. You
can **test values** and it will evaluate the widget velocity.

## Best practices on widget creation.

##### Coding standard please follow the following

* [Google Coding Standard](http://google-styleguide.googlecode.com/svn/trunk/htmlcssguide.xml#ID_and_class_naming)

These standards should be follow across all widget creations, they will be used
as a way to validate if a widget will pass.

##### Widget standard creation

##### The Widget HTML/VELOCITY Guide

```html
<!--

Author: Victor S. Barba
Email : victor.barba@torocommerce.com

## DO NOTE CHANGE, SAVE, UPDATE OR DELETE THIS WIDGET

-->

<!--
## CSS Includes Below
## If possible use style.css unless you need to provide external resources css
## for your project. As long as we don't ahve the frameworks and extensions working,
## you are allowed to add externall css resources but please be guided that
## most of the css you need are already included in the extensions.
-->

<!--
## Velocity Variables Below
-->

<!--
## Velocity Html Content Below
## This widget is from http://themeforest.net/item/garbini-bootstrap-ecommerce-template/full_screen_preview/7494288
-->

<div class="row product-parent">
    <ul class="products">
        <li class="col-sm-3">
            <div class="product">
                <div class="thumbnail">
                    <a href="product.html">
                        <img src="http://htmldemo.themico7.com/garbini/img/images/product-1.jpg" alt=""/>
                    </a>
                    <a href="" class="add-to-cart" title="Add to Cart">
                        <span class="fa-stack fa-2x">
                            <i class="fa fa-circle fa-stack-2x"></i>
                            <i class="fa fa-shopping-cart fa-stack-1x fa-inverse"></i>
                        </span>
                    </a>
                </div>
                <hr>
                <div class="title">
                    <h3>Reshape What?</h3>
                    <p>by Kirsten Dunst</p>
                </div>
                <span class="price">$18</span>
            </div><!-- End Product -->
        </li><!-- End col-sm-3 -->
    </ul><!-- End products -->
</div><!-- End product-parent -->

<!--
## Scripts Below
##  Make use if script.js instead please unless you need to include external resources
##  Put external resources below if needed but NOTE that this will be temporary
##  Until we handle external resources on frameworks and extension if possible avoid
-->

<!--
##  Adding scripts in here
-->
```


* General Guide **BEST PRACTICES (IMPORTANT READ AND FOLLOW!!!)**
 * [Necolas Idiomatic CSS](https://github.com/necolas/idiomatic-css)
 * [Mdo Code Guide](http://mdo.github.io/code-guide/)
* **Always add a prefix class specific for a widget**

##### The Widget CSS Guide

```css

/* README
 * .product-parent is a parent class wrapper for adding specificity
 * on your widget. You will be adding a similar logic when creating
 * your widget.
 *
 * ================================================================
 * DELETE THIS COMMENT WHEN YOU DONT NEED IT ANYMORE
 */

/* PRODUCTS
==================================================================*/

/* This is a sample parent class wrapper for the widget */
.product-parent {}

.product-parent a {
    color: #fd638f;
}

.product-parent hr {
    border-top: 1px solid #fd638f;
}

.product-parent ul.products {
  padding: 0;
  list-style-type: none;
}

```

##### The Javascript Guide

```javascript

No content yet!!

```




