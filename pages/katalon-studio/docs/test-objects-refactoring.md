---
title: "Test Objects Refactoring" 
sidebar: katalon_studio_docs_sidebar
permalink: katalon-studio/docs/test-objects-refactoring.html 
---
> Starting from **Katalon Studio version 7.0.0**, test object refactoring is available.

Test object refactoring is an ability to view and manage the unused test objects, which helps you have an insight on which objects are useful. Hence, you can actively organize and keep them up-to-date. For a significant and long-term project, this feature is critical to keeping your object repository neat and clean.

An unused Test Object is any Web, Web Service, Mobile, Windows test object that you haven't referred to in any Test Case, Test Listener, or Keyword.

Go to **Tools > Test Object > Show unused Test Objects** to retrieve all unused test objects in that project.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/test-object-refactor/option.png" width="486" height="141">

The **Unused Test Objects Report** displays a list of test objects that you haven't used yet.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/test-object-refactor/a.png" width="745" height="254">

> Make sure you enable **Link with selected part** to view the selected unused test objects on Test Explorer.\
<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/test-object-refactor/link-selected.png" width="471" height="87">

You can view and maintain its details by double-clicking the object to display its **test object view**.  Alternatively, you can remove the outdated and obsolete ones to keep only those objects you have used.

* Remove all unused objects: Click **Delete all** and confirm your action. Be cautious since there is no chance to restore the removed objects in Katalon Studio. You can back up those unused objects by using [Katashare](https://docs.katalon.com/katalon-studio/docs/import-export-test-artifact.html) for exporting and importing those objects in case you would like to have them back.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/test-object-refactor/list-unused-objects.png" width="442" height="192">

* Remove selected objects: If you want to remove just some of the objects in the list, right-click on that object, select **Delete** and confirm your action.

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/test-object-refactor/remove-one.png" width="636" height="552">

### Object References

You can see in which places a test object has been used by viewing its references. Right-click on the object, in the drop-down menu, select **Show References**. Katalon Studio searches for that object and returns its references. Double-click on a highlighted reference to go to the corresponding place in that project.

Example:

<img src="https://github.com/katalon-studio/docs-images/raw/master/katalon-studio/docs/test-object-refactor/object-reference.png" width="" height="">

> Unused objects have no references and appear in the **Unused Test Objects Report** mentioned above.
