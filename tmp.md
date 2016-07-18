# SCSS
**WARNING** These notes are taken directly from the tutorial at [codecademy](https://www.codecademy.com/en/courses/learn-sass)

## Variables
    $variable-name-color: #fff;

    background-color: $variable-name-color;

## Nesting
block in a block
    .class1-parent {
        this: that;
        .child {
          this2: that2;
        }
    }
    //compiles to
    .class1-parent {
      this: that;
    }
    .class1-parent .child {
      this2: that2;
    }

An example of nested properties would be:
    .parent {
       font : {
        family: Roboto, sans-serif;
        size: 12px;
        decoration: none;
       }
    }

##  Data Types
- Numbers
-	Strings
-	Booleans
-	null
-	Lists
-	Maps

## Lists
Can use a space or comma separated list
    one two three or one, two, three

## Maps
Uses key : value pairs such as
    (key1: value, key2: value);

## Mix-ins
-	Let you make groups of declarations that you want to re-use through out a site
-	uses hyphens and underscores interchangeably


1.    Mixins can take multiple arguments.
2.    Sass allows you to explicitly define each argument in your @include statement.
3.    When values are explicitly specified you can send them out of order.
4.    If a mixin definition has a combination of arguments with and without a default value, you should define the ones with no default value first.
5.     Mixins can be nested.



      .notecard {
        .front, .back {
        width: 100%;
        height: 100%;
        position: absolute;

        @include backface_visibility;
        }
      }

      // Is equivalent to:

      .notecard .front, .notecard .back {
        width: 100%;
        height: 100%;
        position: absolute;

        backface-visibility: hidden;
        -webkit-backface-visibility: hidden;
        -moz-backface-visibility: hidden;
        -ms-backface-visibility: hidden;
        -o-backface-visibility: hidden;
      }

Mix-ins should only be used with arguments such as:

    @mixin backface-visibility($visibility) { //Add an argument
     backface-visibility: $visibility;
     -webkit-backface-visibility: $visibility;
     -moz-backface-visibility: $visibility;
     -ms-backface-visibility: $visibility;
     -o-backface-visibility: $visibility;
    }

    .className {
      @include backface-visibility(hidden);
    }

Default values are declared like:

    @mixin backface-visibility($visibility: hidden)

    // When it is called later on, it will default to the value passed
    @include backface-visibility(); //hidden will be used
