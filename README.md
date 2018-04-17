# LibraryApp
This Application is to simulate a Library System. In order to challenge and improve upon my Course Registration Application,
I decided to attempt a GUI implementation of a Library System. While it shares similarities to the Course Registration App,
the Library Application improves on many of the poor-programming techniques used in the past. The core object models of the Library 
App are more well designed, minimizing dependency and improving cohesion. While the design for the GUI components is better than the 
Course Registration App, there are still many improvements that can be made most notably in libraryapp.gui.StudentMenu. One change that 
I believe vastly improved my QoL is writing completely separate Listeners within libraryapp.gui.utilities. Many JComponents used
the exact same listener so it made more sense to write a separate class that can be reused multiple times and changed from a single file. 
Having attempted to create full-fledged GUI applications multiple times, it is much faster to implement and less intimidating to approach.
This project pushed me to learn a lot more about correclty using git, designing classes more effeciently, and working with Swing/multithreads.

## Current Struggles
The main issue that continues to be a problem is running into ConcurrentModificationErrors of Lists and adding JComponents
to existing JPanels deep within a JFrame. Often times, the conccurent error is the result of poor design and is resolved with an iterator.
While I learned a lot from the Course Registration App, it still did not prepare me for everything that I might have needed in this 
Library Application. As a result, my planning and design was sub-optimal. I imagine future attempts will go by even faster and will have 
better designs as I reflect on how this project developed. I overcame my previous concurrentModificationError with this issue by learning about Swing's threads and its importance to update
UI components from the Event Dispatch Thread. However, one issue that continues to bother me is being able to add JComponents to a JPanel
deep within a JFrame. My initial thoughts are to use validate, revalidate, invalidate, and SwingUtilities.updateComponentTreeUI to accomplish
this task. 

Features this includes(April 17, 2018):
- User Login/Registration
- Checkout/Return Books
- Search for Books by Author/ISBN/Title
- Supports Multiple Copies of Same Book
- View/Pay Overdue Book Penalties
- State of all objects are maintained in CSV files
  - Data can outlive changes to UI

Future Implementation:
- Librarian Menus
