# DevTest

## Create an application that displays the result of the API https://thecatapi.com/ in a grid using React and Typescript. 
 
1. Use React and Typescript, and as the UI library, use Telerik Kendo UI for React. 
Implement data paging (server-side) with a filter triggered by a switch/toggle button to filter and display cats. 
Please include unit tests using Jest and/or Cypress if possible. 
As a bonus, add any functionality and/or library that you frequently use and find useful for demonstration purposes. 
The application should be visually appealing and user-friendly while adhering to standard front-end programming practices and coding conventions commonly used in front-end projects. (ideas : use a store like zustand, retries on failure, HTTP calls isolated from React components, a file for REST endpoints routes URLs, use react-query library, create a class for hosting endpoints calls like "CatService.ts"...)
 
2. Create a function in Typescript : Given an array of club members, determine which members should be billed based on the links between the members and identify the number and/or names of dependent children. 
 - Each member has a numeric Id and a numeric linkId, and members are linked together based on their linkId. 
 - A member with a non-null linkId is a child (and should not be billed), while a member without a linkId (null) is a parent (with or without children). 
 - If a member is linked to another member, the linked member should be billed (e.g., a child linked to a parent) if they don't have their own link to another member. - The algorithm should detect circular references (e.g., A linked to B linked to A, or A linked to B linked to C linked to A, or A linked to A, B linked to B...). (Members' array provided in the email as a .json format attachment). 
 
Please make both parts of the test available on GitHub and notify me with a link once it's available. For the second part, it can be a simple additional .ts or .js file, or accessible through a button click on the main application.
 
## Answer these questions:
 
1.	How would you, in the context of a SaaS application, allow the front-end/browser to obtain data from the server, such as a list of currencies or accounting accounts, without necessarily having access to all internal database fields?
2.	What are the advantages and possible drawbacks of using GUIDs as IDs (primary keys) in a database table, instead of using integers?
3.	What is the possible bug in the return of this method in this C# code, knowing that the method should return the current date if no close date is found? (C# code snippet provided): 
public static DateTime GetClosest(this DateTime dateTime, DateTime[] dates)
{
    long min = long.MaxValue;
    DateTime closestDate = new DateTime();
    foreach (DateTime date in dates)
    {
        var calc = Math.Abs(date.Ticks - dateTime.Ticks);
        if (calc < min)
        {
            min = calc;
            closestDate = date;
        }
    }
    return closestDate;
}
 
