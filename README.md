Creating a GitHub Book Repository (non-archive book)

Go to the template repository: https://github.com/openstax/template-osbooks

Above the file list, click “Use this template”.


In the Owner drop-down menu, select openstax.

Name the Repository:
osbooks-book-name, if repo contains only one collection, or

osbooks-book-name-bundle, if repo contains more than one collection

Note: Repository names can be changed at a later time. Description can be left blank.

Set repository visibility to Private.

Leave “Include all branches” unchecked (this template repository only has one branch).

Click Create repository from template.

Once the content repo is created, navigate to the META-INF folder.
Open the books.xml file.
Inside the <book/> tag, fill out the following information: 
slug: (determined by CM)
This can be changed at a later time
collection-id: col##### (determined by CM)
href: "../collections/<slug>.collection.xml" (use same slug from above)

Example:

<container xmlns="https://openstax.org/namespaces/book-container" version="1">
    <book slug="college-algebra" collection-id="col11759" href="../collections/college-algebra.collection.xml" />
    <book slug="precalculus" collection-id="col11667" href="../collections/precalculus.collection.xml" />
    <book slug="precalculus-coreq" collection-id="col32026" href="../collections/precalculus-coreq.collection.xml" />
</container>

Navigate to the COLLECTIONS folder.
Open the collection.xml file (this is a template file that must be edited) - full file name is chosen-book-slug.collection.xml
Inside the <md:uuid> tag, use a random number/letter generator to generate a UUID with 32 characters for this collection. 
Inside the <md:title> tag, input the book title.
Inside the <md:slug> tag, input the same slug used in step 8. 
Inside the <md:license> tag, input the desired license.
Inside the <md:language> tag, specify the language of this collection.
en for English
pl for Polish
sp for Spanish

Example:

<col:metadata>
    <md:uuid>00000000-0000-0000-0000-000000000000</md:uuid>
    <md:title>test book</md:title>
    <md:slug>book-slug1</md:slug>
    <md:language>book-slug1</md:language>
    <md:license url="http://creativecommons.org/licenses/by/4.0/">Creative Commons Attribution License 4.0</md:license>
  </col:metadata>


 Navigate to the LICENSE file. 
Copy/Paste the contents of one of the following into the LICENSE folder:
CC-BY 4.0
CC-BY-NC-SA 4.0
CC-SA 4.0

(Optional) Update READ.ME file with any information you wish.

 Create issue on CE board to review repository
Issue Title: review new repository for osbook-new-book-name
Include link to new repository
Include finalization date (when repo is needed by)
