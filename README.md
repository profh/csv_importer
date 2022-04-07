CSV Importer
---

This is code taken from a previous 67-373 project where we were importing student records from a cvs file and generating a student object based on that record.  This can be generalized and applied to other projects, like TQG.

There is in the test directory a sample of the csv file for students as well as the test for the importer. The tests should make it a little more apparent how to utilize the importer service, but feel free to ask for assistance as needed.

The importer does rely on the "roo" gem (https://github.com/roo-rb/roo) and can now be used to import xlsx spreadsheets as well csv files.  

Key to modifying the service is to adjust private method `read_data`, which is what is used to map key attributes to the columns in the csv file.  The `add_student` method calls this, and then takes the data extracted to create a student object and push it into an array of student objects.