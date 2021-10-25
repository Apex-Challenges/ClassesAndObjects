# Coding 101 Classes and Objects

# Setup

[Fork](https://docs.github.com/en/get-started/quickstart/fork-a-repo) this repository

Create a [new branch](https://docs.github.com/en/github/collaborating-with-pull-requests/proposing-changes-to-your-work-with-pull-requests/creating-and-deleting-branches-within-your-repository) - name it whatever you like, but note it down!

[Clone](https://docs.github.com/en/github/creating-cloning-and-archiving-repositories/cloning-a-repository-from-github/cloning-a-repository) to your local machine

On your local machine, `cd` into the directory created for your clone and switch to your new branch using the command:

`git checkout <branchname>`

## Implementing

Carry out all work in your local filesystem using VS Code, as you will 
need to send them back to Github.

1. Create a scratch org (or connect to an existing one)
1. Push the code to your scratch org - this will check that your code compiles

## Exercises

For each exercise, after you have created the class(es), it's a good idea to execute some anonymous Apex to create new class instances and invoke the methods, using a variety of values if appropriate.

### Rectangles

Create a class named `Rectangle` that encapsulates the height and width of a rectangle.
It should only be possible to construct a rectangle by supplying a height and width - no defaults are provided.

Add methods to :
1. Calculate and return the surface area of the rectangle
1. Determine if the rectangle is a square, returning true if it is, otherwise false

### Circles

Create a class named `Circle` that encapsulates the radius of a circle.
It should be possible to construct a circle by providing either it’s radius or a string representation of its diameter.

Add methods to calculate and return :  
1. The circumference of the circle
1. The surface area of the circle

Any constants used in the calculation should be class variables and use the final keyword to prevent modification. They should not be visible or usable outside of the `Circle` class

### Grid 

Create a class that tracks the position of a user in a 5x5 grid as x and y coordinates. The coordinates are index origin 0.
The default position is the top left, but the user can specify the position in the constructor. 

Create methods to move :

1. left 
1. right 
1. up 
1. down

Any attempts to move outside of the grid, or establish a starting position outside the grid, should result in the x and y coordinates being set to the closest position that remains inside the grid.

Create a method to output the grid to the debug log. Use the `-` character to represent empty space and the `*` character to represent the user’s current position. For example, if the user is currently at position 2,1 the following debug lines will be output:

```
   ----- 
   --*--
   -----
   -----
   -----
```

### Books

Create classes to model an author and the books that they have written. 

The `Author` class holds :
- First name
- Last name
- Email address
- Collections of books in Draft and Published states. The published collection is keyed by publish date. 

The `Book` class is an inner class of the `Author` class and holds :
- Title
- Number of pages
- Genre
- Status (Draft or Published) 
- Published date, which will not be defined if the book is in Draft.

1. Create a method on the `Book` class to allow it to be published. Invoking this method changes the state to Published and sets the published date to today’s date.
1. Create a method on the `Author` to publish a book based on its title. This should locate and remove the book from the draft collection
execute the publish method on the book add the book to the published collection, using it’s published date as the key

## Submitting Your Solution for Assessment

Please note that assessment is only available to BrightGen employees or by prior arrangement with Keir Bowden (aka Bob Buzzard). If you don't satisfy this criteria your pull request will not be reviewed.

Add `keirbowden` as a [collaborator](https://docs.github.com/en/github/setting-up-and-managing-your-github-user-account/managing-access-to-your-personal-repositories/inviting-collaborators-to-a-personal-repository) to your new repository

The commands below are if you are using Git from the command line - you can also use the VS Code built-in [source control functionality](https://code.visualstudio.com/docs/editor/versioncontrol).

Stage your new classes using the following command: 

`git add force-app/main/default/classes`

and then commit the changes :

`git commit`

and push these to the remote repository

`git push origin <branchname>`

Once you are happy with your solution, [open a pull request](https://docs.github.com/en/github/collaborating-with-pull-requests/proposing-changes-to-your-work-with-pull-requests/creating-a-pull-request)

Then wait!


