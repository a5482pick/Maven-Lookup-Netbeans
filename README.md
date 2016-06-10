**_Selection, Lookups and Maven with Netbeans._**

Two independent window components are created in Netbeans.  &nbsp; 'HistoryTopComponent' is able to listen for String submissions in 'TextTopComponent' using 'Lookups.'  &nbsp; The Lookup mechanism means HistoryTopComponent need know nothing about how TextTopComponent generates String instances: &nbsp; HistoryTopComponent is able to locate the instances irrespective of who or what generated them. &nbsp; String instances are submitted from TextTopComponent (using method associateLookup of class TopComponent) to its own Lookup using a) the click of a button, and also b) by clicking in turn inside each of the two text boxes. &nbsp; The crucial method in HistoryTopComponent is _Utilities.actionGlobalContext()_. &nbsp; This method, used in conjunction with a listener, observes the Lookup of whatever component currently has focus i.e. it watches the Lookup of TextTopComponent when TextTopComponent is in use.

_Summary of use:_

If two text-area boxes are not visible upon start-up, select 'History' from 'Window' after the application has loaded.

To pass new text to the 'History' window's text box, submit with the button. &nbsp; If instead you click the text boxes in each of the two windows alternately, an incrementing number is submitted to the HistoryTopComponent text box from TextTopComponent.

(The example https://platform.netbeans.org/tutorials/nbm-maven-quickstart.html was used as a starting point.)

_To run directly from the command line:_

From within directory _MavenPlatformWordApp/application/_ &nbsp; use this phase/goal combination:

$ mvn install

$ mvn nbm:run-platform


