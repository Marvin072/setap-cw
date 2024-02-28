Usage
=====

.. _installation:

requirements
------------

 System should require the user to input a username, email address and password to register an account (1)
 System should allow the user to enter a login screen and input their username/email and password (2)
 System should validate the inputted username/email and password against the database of accounts (2)
 System should log in the user if their inputs pass validation, and reject the user if their inputs fail (2)
 System should include tick boxes for the user to select which parameters they want to be used by PC Generation. (3)
 System should expand input fields for any parameters ticked that the user can either drag if it’s a slider, input a number or select a word from a dropdown box (3)
 System should include tick boxes and input fields for Budget, Desired Processing power, Part specific values like: RAM size, read/write speed and type, Secondary Storage size, read/write speed and type, Case Dimensions, Motherboard Size/type, Energy Efficiency, Noise levels and Cooling Method (4)
 System should run an algorithm at the press of a “generate” button that uses the user parameters to generate many PC configurations (5)
 System should display all the generated PC configurations along with the values each config has for each selected parameter so users can see how generated configs slightly differ (5)
 System should allow users to click on one of the many PC configs to select them and display the config and its parts and stats (5)
 System should allow users to click on one of the parts of the PC and entire a maximised view, displaying an image of the product and its stats (6)
 System should allow the user to switch out certain parts from the configuration for other parts upon the press of a button (7)
 System should pop up with a list of parts that are of the same type as the one the user wants to replace as well as compatible with the rest of the parts. This pop-up should also have changeable user parameters like other parts of the system (7)
 System should replace the part selected for replacement with the one the user clicks on/selects and update the configuration’s stats and part list. This should also hide the pop-up (7)
 System should have a Job Template Generator section of the App that is similar to the vanilla PC Generator but can be skewed depending on an imputed Job the user wants the PC to be specialised for. This Generator should still have the other input parameters the vanilla Generator has (8)
 System should skew the PC Generator depending on the Job selected. For example Art professionals want the ability to store large files in storage and memory, therefore emphasise RAM and Secondary Storage sizes. (8)
 System should be able to save generated or customised PC configurations to the user’s account upon the click of a button. This will save and store the PC object onto the Accounts database (9)
 System should be able to retrieve and load PC configurations from the Accounts database if they have the privilege (9)
 System should have a page that displays all the user’s saved configs on their account (10)
 System should prompt the user to log in if they are not and try to open the saved configs page (10)
 System should allow the user to be able to click on any of the configs and load them (10)
 System should allow the user to share the config by changing the access type (restricted meaning only the author can view it or open meaning anyone with the link or the author can view it) and the system producing a link for the user to share (11)
 System should validate if a user has authorisation to retrieve configs from the database based on the config’s access type (11)
 System should have a help button in the UI that once pressed, loads a tutorial or help window explaining the functionality of the page the user is currently on (12)
 System should have different help pages depending on the page the user is currently on (12)
 System should display definitions of possibly confusing buzzwords when the user hovers over them or interacts with them with their mouse (13)


Creating recipes
----------------

To retrieve a list of random ingredients,
you can use the ``lumache.get_random_ingredients()`` function:

.. autofunction:: lumache.get_random_ingredients

The ``kind`` parameter should be either ``"meat"``, ``"fish"``,
or ``"veggies"``. Otherwise, :py:func:`lumache.get_random_ingredients`
will raise an exception.

.. autoexception:: lumache.InvalidKindError

For example:

>>> import lumache
>>> lumache.get_random_ingredients()
['shells', 'gorgonzola', 'parsley']

