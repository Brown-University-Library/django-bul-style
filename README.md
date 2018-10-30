Brown University Library Theme (Django)
===============

Theme for Brown University Library Django Projects

Installation and configuration
------
 * Either checkout and run ```python setup.py install``` or install directly from Github with pip:

   ```
   pip install git+https://github.com/Brown-University-Library/django-bulstyle.git#egg=bulstyle
   ```

 * In settings.py :

  * Add `bulstyle` to your `INSTALLED_APPS`

    ```python
    INSTALLED_APPS = (
       # other packages
      'bulstyle',
    )
    ```
  
  * Add `bulstyle/css/bulstyle.css` to you BOOTSRAP3 settings
  
    ```python
    BOOTSTRAP3 = {
      # other settings
      'css_url': os.path.join('',STATIC_URL,'bulstyle/css/bulstyle.css'),
    }
    ```

* In your project `base.html` template

  ```django
      {% extends 'bulstyle/base.html' %}
  ```


Include Blacklight themes
-------------------------
  * Follow the above instructions except  replace `bulstyle.css` 
  with `bulstyle-blacklight.css`

    ```python
    BOOTSTRAP3 = {
      # other settings
      'css_url': os.path.join('',STATIC_URL,'bulstyle/css/bulstyle-blacklight.css'),
    }
    ```

Optional Settings
-----------------
  The following setting will change the main container class for all divs.

  ```python
  BULSTYLE = {
    'container_class': 'container', #default
  }
  ```

  With this setting you could potentially change to a fluid layout using 
  ```python
  BULSTYLE = {
    'container_class': 'container-fluid',
  }
  ```

Legacy Theme
-------------------------
  This is a precompiled theme that is not generated by the scss files included.
  Also has some styles used in the Brown Digital Repository
  * Follow the above instructions except  replace `bulstyle.css` 
  with `project.css`

    ```python
    BOOTSTRAP3 = {
      # other settings
      'css_url': os.path.join('',STATIC_URL,'bulstyle/css/project.css'),
    }
    ```



License
=======

[bulstyle] [BULSTYLE] by [Brown University Library] [BUL]
is licensed under a [Creative Commons Attribution-ShareAlike 3.0 Unported License] [CC BY-SA 3.0]

[BULSTYLE]: https://github.com/Brown-University-Library/etd_app
[BUL]: http://library.brown.edu/its/software/
[CC BY-SA 3.0]: http://creativecommons.org/licenses/by-sa/3.0/

Human readable summary:

    You are free:
    - to Share — to copy, distribute and transmit the work
    - to Remix — to adapt the work
    - to make commercial use of the work

    Under the following conditions:
    - Attribution — You must attribute the work to:
      Brown University Library - http://library.brown.edu/its/software/
    - Share Alike — If you alter, transform, or build upon this work,
      you may distribute the resulting work only under the same
      or similar license to this one.

