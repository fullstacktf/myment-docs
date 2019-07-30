# Database structure

The Myment Travel web app has an internal structure that needs to be understood in order to make a clear, logical and concise front-end.

In order to do so. First we have to see this image:

![database tables](https://live.staticflickr.com/65535/48411784097_5da13b2f0d_k.jpg)

I have to clarify that the photo has some errors, but the true info is down bellow and without errors. (Later propably, I'll remove this photo)

At this very moment and in this first version, you can see four (4) tables that are inter-connected (the tables are the ones that are enclosed in squares). Within each table (**sign_up for example**), there are certain columns (**username for example**), that will in turn and later contain values (**thanos2019 for example**).

#### 1. sign_up
   * id
   * first_name
   * last_name
   * username
   * password
   * email
   * createdAT
   * updatedAT
   (this last two columns are necessary for sequelize to work, and they have to be on each table also)

#### 2. ranking
   * id
   * points
   * createdAT
   * updatedAT

#### 3. profile
   * id
   * profile_photo
   * profile_info
   * createdAT
   * updatedAT

#### 4. add_moments
   * id
   * name
   * country
   * state
   * city
   * category
   * description
   * item_lodging
   * item_leisure
   * item_food
   * item_lodging_name
   * item_leisure_name
   * item_food_name
   * item_lodging_tags
   * item_leisure_tags
   * item_food_tags
   * createdAT
   * updatedAT
   (here, I will try to make it more simple, don't worry, I'm on it)

Under the tables, you can see that there are certain explanations in which I would like to inquire.

First, you can see that the **add_moments** table has an arrow that goes down. Right there, you can see that the **moments contain categories**, and that in turn **those categories contain items**, and that **those items contain a name or tags**.

Following this logic: **category > item > name, tags**

## Why?

**The explanation lies here, on the values saved or taken when you are making an itinerary:**

![database tables](https://live.staticflickr.com/65535/48411695867_6bc219651c_b.jpg)

First you can see... (I'll finish this)

![database tables](https://live.staticflickr.com/65535/48411695922_a1c35262ee_b.jpg)

And then... (I'll finish this)

![database tables](https://live.staticflickr.com/65535/48411695817_50639283b9_b.jpg)

1. MariaDB as a database management system.
   * Inside the MariaDB database you can see the myment database.
   * You can access to the database writing 

2. We will use Sequelize as an ORM.
3. This is the 1.01 version of the database structure:


First, when we will generate an itinerary, we can choose between three (3) options.

The first is to generate a free contain categories, wich will contain items, wich will contain name and tags.