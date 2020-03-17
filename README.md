Travoris Bradford, Aleyah Rowell, Kelvin-Clyde McGuire 
Unit 8- Unit 9 group milestones 
Group Project - README
===

# The Ultimate Grocery List

## Table of Contents
1. [Overview](#Overview)
2. [Product Spec](#Product-Spec)
3. [Wireframes](#Wireframes)
4. [Schema](#Schema)

## Overview
### Description
[This grocery list application will have a grocery list screen, and also have a update and remove item screen on the grocery list screen.The features will also  pertain to making this the best downloadable grocery app.  You can also be able to manage your list and be able to add-on/remove items to your disposal.]

### App Evaluation
[Evaluation of your app across the following attributes]
- **Category:Shopping**
- **Mobile:The application is a shopping app for your personal groecery needs.**
- **Story:User will be able to create an account log-in,User can be able to customize list by adding/removing items at their disposal.**
- **Market: Anyone that loves to keep tabs on what items to get/need so you won't be able to forget what is important. **
- **Habit:Users can personalize their list to the best option available for them as they shop.**
- **Scope:Most grocery list apps are very dull this app brings creativity.**

## Product Spec

### 1. User Stories (Required and Optional)

**Required Must-have Stories**

* [User will be able to create an account log-in.]
* [User can be able to customize list by adding/removing items at their disposal.]

**Optional Nice-to-have Stories**

* [Have an example list that the users can refer to.]
* ``
* ...

### 2. Screen Archetypes

* [Grocery list screen]
* [Add/remove items to your disposal as you shop and find items you need.]
* [When the user presses "+" sign, they will be able to customize by adding or removing from the list.]

### 3. Navigation

**Tab Navigation** (Tab to Screen)

* [Grocery list:Add item tab]
* [Update/delete items tab]


**Flow Navigation** (Screen to Screen)

* [Grocery list:Add item screen]
   * [once added it will pop up the item that you will be shopping for on screen.]
   
* [Update/delete items on list.]
   * [Once item has been added/deleted you will be able to save list.]
   

## Wireframes
[Add picture of your hand sketched wireframes in this section![]
]
<img src="https://i.imgur.com/tO2go0t.jpg" width=600>
<img src=" ![](https://i.imgur.com/DnP8l52.jpg)" width=600>

### [BONUS] Digital Wireframes & Mockups
<img src="https://i.imgur.com/tO2go0t.jpg" width=600>
<img src=" ![](https://i.imgur.com/DnP8l52.jpg)" width=600>

### [BONUS] Interactive Prototype

## Unit 9 Section
## Schema
[This section will be completed in Unit 9]
### Models


| Property    | Type     |           Description               |
| --------    | -------- | -----------                         |
| ItemsId     |  String  |The names of the items that are added|
| UpdateButton|  String  |User can update the list items|
| RemoveButton|  String  |User can remove list items|
| PlusSign    |  String  |Users can plus sign to add items to list|
 
 
### Networking
### Networking
•	Home Screen (Grocery List)
-	(Read/GET) Load items that were previously saved by the user
-	//This function will load items by reading every line of the data file
private void loadItems(){
    try {
        items = new ArrayList<>(FileUtils.readLines(getDataFile(), Charset.defaultCharset()));
    } catch (IOException e) {
        Log.e("MainActivity","Error reading items", e);
        items = new ArrayList<>();
    }
}

-	(Create/ITEMS) Add a new item to the grocery list

btnAdd.setOnClickListener(new View.OnClickListener(){
    @Override
    public void onClick(View v){
        String todoItem = etItem.getText().toString();
        //Add item to the model
        items.add(todoItem);
        //Notify adapter that an item is inserted
        itemsAdapter.notifyItemInserted( position = items.size() - 1);
        etItem.setText("");
        Toast.makeText(getApplicationContext(), text = "Item was added", Toast.LENGTH_SHORT).show();
        saveItems();
    }
});

-	(Update/ITEMS) Edit an existing item on the grocery list

-	 (Delete) Delete an item from the grocery list

ItemsAdapter.OnLongClickListener onLongClickListener = new ItemsAdapter.OnLongClickListener(){
    @Override
    public void onItemLongClicked(int position) {
        //Delete the item from the model
        items.remove(position);
        //Notify the adapter
        itemsAdapter.notifyItemRemoved(position);
        Toast.makeText(getApplicationContext(), text = "Item was removed", Toast.LENGTH_SHORT).show();
        saveItems();
    }
};

   
## Sprints
[x]- Finalize unit 9 HackMD document

[]- Analyze how we are going to code our project

[]- Analyze what additional features we can add to the application

[]- Analyze how we can make the app easy for the user navigate
