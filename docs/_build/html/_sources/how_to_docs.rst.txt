How to Make Documents
=====================

Making documents for the project is actually very simple. All you'll need to know if how to run a couple of commands!
Let's get started! For simplicity, we're going to break this up into X steps:

**1. Write the Document Content.**

This is where the majority of your time will be spent! Since sphinx is heavily automated, it will render your content
into html without you having to do anything but typing a command. The only caviat is that the file you write your content
in *has* to be in the .rst format (test.rst, is a valid file). Additionally, you need to add a title to the page. To do this
add a bit of text at the top of the page and put a collection of underscores underneath, like this:


| Test
| \=\=\=\=


Sphinx has its own markdown system which means that your text will be rendered based on specific key symbols that you input. 
This is kinda similar to having a text editor that has a programming language built in!

Here are some examples of how to do basic formatting with Sphinx's markdown solution:
    
    *test* = \*test\*
    

    **test** = \*\*test\*\*


    - test = \- test
    - test = \- test
    - test = \- test 

For more information on the various things you can do with formatting, check `here <http://docutils.sourceforge.net/docs/user/rst/quickref.html>`_

When you're finished typing up your document, go ahead and add it to the *raw_documents* folder. This is needed because
sphinx looks in that specific folder when convert .rst files into html documents.

**2. Add the Document to the Homepage.**

*If you're editing an existing file, you can skip this step as it should already be added to the Homepage*

With your document written and added into the *raw_documents* folder, we need to make sure that it is attached to the
home page and navigation bar. This is necassary to keep our documentation consistent and accesible. To do this, go
ahead and open up the *homepage.rst* file found inside of the *raw_documents* folder. To add your new document, simply 
write the name of your file (without the extension) 

**3. Render the new Documentation.**

Once the document is found in the *homepage.rst* file, you can go ahead and generate the html! To do this, simply run the
following command:

    *make html*

A bunch of output should occur to let you know what is being generated. Once you have done this, open the html file that you
generated (it will be found in the *_build* folder) and check that it looks the way you expected. When you're satisfied, 
commit the changes in make a pull request so other members of the group can review it and upload it to the hosting service.
