# Simple Time Clock

The Simple Time Clock application was originally created as an exercise in an interview process for a job which offer failed to come through.
But lest anything useful go to waste, I have decided to use it as a sample of my work. 

What I hope to convey through this example is both my approach to development, as evidenced both by the excellence in design, architecture,
and code to which I aspire as well as the paper trail revealed in the git logs. I am passionate about software quality from high level design
down through the nuts and bolts of implementation. I believe this codebase reveals some of that passion.

Enjoy!

Greg (18 December 2022)

## Interview Candidate Requirements
This project was created to specifically fulfill the requirements specified by the Interview Candidate Project instructions, which are reproduced below:

### Simple Time Clock Application
_Create an application that represents a simple time clock. You are free to use the programming languange if your choice.
The application must follow the requirements listed below._

1. Allow user to be identified using a unique ID assigned to each employee.
    1. Users that cannot be identified should not be able to use the application.
1. Allow users to start a work shift.
    1. Do not allow users to start multiple shifts simultaneously.
1. Allow users to end a work shift.
    1. Do not allow users to start a shift during an active shift.
1. Allow users to start/end a break, but only during an active shift. o Do not allow employees to end a shift if a break is active.
1. Allow users to start/end a lunch, but only during an active shift. o Do not allow employees to end a shift if a lunch is active.
1. All shift data performed by users should be recorded and made available upon returning to the application.
1. (Optional) Allow new users to register themselves in the application.
1. (Optional) Allow for two types of users in the application; administrators and non-
administrators.
1. (Optional) Allow administrators to perform any function at any time regardless of the rules
stated previously.
    - [GW] Need greater clarification on this rule. What is expected behavior in each case?
1. (Optional) Allow administrators to view a summary report section that summarizes all the
employee’s shift activity.
    1. (Optional) Allow administrators to filter the report data.

## Analysis

Even without the optional requirements, this is a tall set of requirements to implement over a relatively short time - 3 days, in this case. So rather than trying to do too much too quickly, I designed and built a high quality, maintainable and extensible MVP focused only on the non-optional requirements.

As it is, the result still could use a bit of polish:

## Next Steps
- add an application icon
- change user selection from current full page list of users to a more traditional login window (albeit without password)
    - allow user to register
- add support for admin users 
    - limit access user list screen to admin users <- user's will only see their own shift activity
- add filtering to employee work shift list
- optimize use of MutableLiveData<> objects. 
    - not sure all are necessary.

## Known Issues
- Date display on WorkShift fragment - be smarter about date inclusion, don't need it for every date/time.
