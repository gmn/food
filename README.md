Food Diary Calculator
====

A simple food diary calculator written as a shell script in PHP. 

It supports a basic set of commands to remember foods you've eaten.
So that you don't have to enter them again.  This calculator is only concerned
with the macronutrients: Fat, Carbohydrates, Protein and Calories.  You 
can see a tally of your calories for each day, produce a .csv output,
and a few other useful things.

Note: for proper function, it is recommended that your installation of PHP 
have its curl and sqlite extensions enabled.  Debian packages for these are:
php5-curl and php5-sqlite respectively.


Installation:

Edit the top three fields to set the path where you want the database 
file and your home directory.  You may need to edit the path to your php
executable.  On first run it will create a database automatically.


Command Summary:

/usr/bin/food  -  A food diary calculator script. 
Keeps list of everything you've eaten. Prints macronutrient tallies.

OPTIONS:                

-f [match]              List known foods. Optionally limit results by %match%

new [date][notes]       Start a new day. If no date given, today's date is used

add|-a [name of food]   Add a food to list of foods 

list [date][-v]         List the foods you had today (or on a certain date)
-l   [date][-v]           

-d [name of food]       Delete a food from stored foods.

-r <food>               Replace/Edit a food's attributes

eat <food> [mult][day]  Adds a food to list of eaten for today. If food info 
						is not stored, you will be prompted to enter it. 
						Multipier is by portion or by Oz. So if you drink
						8 ounces of orange juice, you enter 8.

days [-v|-c]            List totals for every day. -v is verbose,-c outputs .CSV

-e [day]                Edit items eaten for specified day (today if none given)

find <food>             Lookup info for a food on the web.

-m [day]                Change how much you've eaten of a food. [day] lists
						foods for specified day.

-n [day][-a]            edit day's note. optionally can select different day 
						-a ammends existing note, instead of overwriting it.

when|-w <string>        search for a food and show what days you've eaten it
						on, and how much.                   

