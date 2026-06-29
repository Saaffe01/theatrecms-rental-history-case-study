# TheatreCMS Rental History Case Study

> **ASP.NET MVC • C# • Entity Framework • Razor • Bootstrap • JavaScript • jQuery • Azure DevOps • Agile/Scrum**

## Project Overview

TheatreCMS is a collaborative ASP.NET MVC web application developed as part of a live software engineering project. Team members worked together using Agile/Scrum methodologies, Azure DevOps for project management, Git for version control, and pull requests for code reviews to simulate a professional software development environment.

During this project, I contributed to the Rental History module by implementing new features, improving the user interface, refining existing functionality, and enhancing the overall user experience. My work included front-end styling, Razor view development, C# controller logic, JavaScript/jQuery enhancements, and applying MVC best practices.

This repository documents my individual contributions throughout the project and highlights the technical skills I developed while collaborating on a real-world software development team.

## My Role

As a Software Developer on the TheatreCMS team, I was responsible for implementing features and UI improvements within the Rental History module. My work involved collaborating through Azure DevOps work items, developing solutions in an existing codebase, submitting pull requests for review, and ensuring each feature met the project's acceptance criteria before submitting it for review.

Throughout these stories, I gained experience working with:

- ASP.NET MVC
- C#
- Razor Views
- Entity Framework
- Bootstrap
- HTML & CSS
- JavaScript & jQuery
- Git & GitHub
- Azure DevOps
- Agile/Scrum Development

## Stories Completed

*The following sections document each feature I completed during the project.*

**Azure DevOps Work Item:** #20169

### Objective

The objective of this story was to improve the appearance of the application's sign-in page by matching the design specifications provided in the project documentation. The changes focused entirely on presentation while preserving the existing functionality of the login page.

### My Contribution

I updated the application's CSS to redesign the sign-in page, improving the layout, spacing, typography, and overall visual consistency. I carefully modified the existing styles to match the desired design while ensuring that the changes did not negatively impact other pages within the application.

### Challenges

Because TheatreCMS is a shared application, styling changes had to be made carefully to avoid introducing unintended side effects elsewhere in the project. Understanding the existing stylesheet and identifying which selectors could be safely modified required careful attention to ensure the changes remained isolated to the intended page.

### Solution

I reviewed the project's design documentation, compared it against the existing implementation, and updated the appropriate CSS rules until the page closely matched the expected layout. Throughout development, I continuously tested the page to verify that the styling changes were isolated to the sign-in page.

### 🛠️ Technologies Used

- HTML
- CSS
- Bootstrap

### Technical Skills Applied

- Reading and understanding an existing codebase
- CSS layout and styling
- Working within an established design system
- Attention to detail
- Debugging visual issues

### Code Highlight

```css
.rental-history-card {
    max-width: 800px;
    margin: 25px auto;
    border-radius: 15px;
    background-color: #fff;
    color: #000;
}
```

This reusable CSS class established the foundation for the Rental History page layout by creating a centered, responsive card with improved spacing and visual consistency. These styling updates helped align the page with the project's design requirements while keeping the implementation reusable across the feature.

### Final Result

The completed sign-in page matched the project's design specifications while maintaining the application's existing functionality.

*(Screenshot of the completed sign-in page will be added here.)*

### What I Learned

This story reinforced the importance of working carefully within an existing codebase. Even small UI changes require understanding how styles are shared throughout the application and verifying that updates do not introduce unintended side effects on other pages.

# 🗂️ Rental History Entity Model & CRUD

> **Azure DevOps Work Item:** #20170


### Objective

The objective of this story was to create a new Rental History entity and implement the foundational CRUD (Create, Read, Update, Delete) functionality for the Rental History module. This work established the data model and project structure that future stories would continue to build upon.

### My Contribution

I created the Rental History entity model and integrated it into the existing ASP.NET MVC application. This included defining the model's properties, configuring Entity Framework to recognize the new entity, and scaffolding the initial CRUD components required for future development.

This story laid the foundation for the Rental History feature by connecting the model, controller, views, and database through the MVC architecture.

### Challenges

Because this was the first story in the Rental History module, it was important to understand how new entities fit into an existing MVC application. Establishing the proper relationships between the model, controller, database context, and Razor views required careful attention to the application's existing architecture.

### Solution

I implemented the Rental History model using ASP.NET MVC and Entity Framework conventions, ensuring it integrated cleanly with the existing project. After scaffolding the CRUD components, I verified that the application could successfully create, retrieve, update, and delete Rental History records through the generated views.

### Technologies Used

- C#
- ASP.NET MVC
- Entity Framework
- Razor Views
- SQL Database
- Visual Studio

### Technical Skills Applied

- Object-Oriented Programming
- MVC Architecture
- Entity Framework
- CRUD Operations
- Database Integration
- Reading an existing codebase
- Backend Development

### Code Highlight

```csharp
public class RentalHistory
{
    public int RentalHistoryId { get; set; }

    public string RenterName { get; set; }

    public DateTime DateRented { get; set; }

    public DateTime DateReturned { get; set; }
}
```

This model defined the structure of the Rental History entity and served as the foundation for the feature's CRUD operations. Following Entity Framework conventions allowed the model to integrate seamlessly with the application's controllers, views, and database.

### Final Result

The Rental History entity was successfully integrated into the application, providing a functional CRUD workflow that served as the foundation for future enhancements throughout the Rental History module.

### What I Learned

Before this feature, I understood the basic concepts of MVC, but implementing a new entity helped me see how each layer of the application worked together. Watching the model, controller, views, and database interact gave me a much clearer understanding of how ASP.NET MVC applications are structured.

I also gained a better understanding of Entity Framework, scaffolding, and the importance of following an existing project's architecture rather than building everything from scratch.

# ✏️ Rental History Create & Edit Pages

> **Azure DevOps Work Item:** #20171

---

### Objective

The objective of this story was to improve the Create and Edit pages for the Rental History module by enhancing the user interface and refining the data entry experience. The focus was on making the forms more intuitive while maintaining the application's existing functionality and MVC conventions.

### My Contribution

I updated the Create and Edit Razor views to improve their layout, organization, and usability. This included refining form elements, labels, and page structure while ensuring the views remained fully compatible with the existing controller logic and model binding.

Throughout the implementation, I worked within the existing codebase to maintain consistency with the project's design patterns and coding standards.

### Challenges

Since these views were already connected to the application's backend, every UI modification needed to preserve model binding, validation, and form submission behavior. Careful testing was required to ensure that visual improvements did not introduce functional issues.

### Solution

I updated the Razor views while preserving the existing MVC workflow. After implementing the changes, I verified that creating and editing Rental History records continued to function correctly and that all form interactions behaved as expected.

### Technologies Used

- ASP.NET MVC
- C#
- Razor Views
- HTML
- Bootstrap
- CSS

### Technical Skills Applied

- Razor View Development
- Model Binding
- Form Design
- Bootstrap Layout
- UI/UX Improvements
- Reading an Existing Codebase
- MVC Architecture

### Code Highlight
```
<div class="form-group">
    @Html.LabelFor(model => model.RenterName)
    @Html.EditorFor(model => model.RenterName)
    @Html.ValidationMessageFor(model => model.RenterName)
</div>
```
This Razor view uses ASP.NET MVC HTML Helpers to generate form elements that are automatically bound to the Rental History model. Using strongly typed helpers ensures that labels, inputs, validation messages, and model binding remain synchronized with the underlying model, improving maintainability while reducing repetitive HTML.

### Final Result

The Create and Edit pages were successfully updated to provide a cleaner and more user-friendly interface while maintaining full compatibility with the existing Rental History workflow.

### What I Learned

This story helped me better understand how Razor views interact with controllers and models within the MVC architecture. It reinforced the importance of preserving existing functionality while improving the user experience, as even small UI changes must continue to support model binding, validation, and data submission.

# 🖥️ Rental History Index Page

> **Azure DevOps Work Item:** #20172

---

### Objective

The objective of this story was to redesign the Rental History Index page to better match the project's design specifications while improving the overall presentation of rental history records. The focus was on creating a cleaner, more organized interface without changing the underlying functionality.

### My Contribution

I redesigned the Rental History Index page by replacing the default scaffolded layout with a more modern Bootstrap card design. I updated the Razor view to improve the page structure, spacing, typography, and overall readability while maintaining compatibility with the existing MVC architecture.

In addition to the UI improvements, I updated the controller logic to retrieve the most recent Rental History records first, ensuring that data preparation remained in the controller rather than introducing sorting logic into the view.

### Challenges

One of the primary challenges was balancing visual improvements with proper MVC design principles. The page needed to match the project's design requirements while continuing to display data correctly and keeping business logic separated from the presentation layer.

Another challenge was understanding where responsibilities belonged within the MVC architecture. Determining whether data ordering should occur in the controller or within the Razor view required careful consideration of MVC best practices.

### Solution

I updated the Razor view to implement the new card-based layout while preserving the existing functionality. I also modified the controller to order Rental History records before passing them to the view, allowing the Razor page to focus solely on displaying data rather than manipulating it.

After implementing the changes, I verified that the page displayed the correct information, maintained the desired layout, and matched the project's design specifications.

### Technologies Used

- ASP.NET MVC
- C#
- Razor Views
- Bootstrap
- HTML
- CSS
- LINQ

### Technical Skills Applied

- MVC Architecture
- Razor View Development
- Bootstrap Components
- LINQ
- Controller Logic
- UI/UX Design
- Separation of Concerns
- Reading an Existing Codebase

### Featured implementation 
```
var rentalHistory = db.RentalHistories
    .OrderByDescending(r => r.DateRented)
    .ToList();
```
This controller prepares the Rental History data before it reaches the Razor view by ordering records from newest to oldest. Performing this work in the controller follows MVC best practices by separating data preparation from presentation, resulting in cleaner and more maintainable code.

### Final Result

The Rental History Index page was successfully redesigned using a responsive Bootstrap card layout while preserving existing functionality. Records were displayed in a cleaner, more organized format, and controller logic was updated to return the most recent rental history entries first.


### What I Learned

This story was one of the biggest learning moments of the project for me. While implementing the feature, I developed a much stronger understanding of the MVC architecture and why responsibilities should remain separated between controllers and views.

Rather than placing data manipulation inside the Razor page, I learned that controllers should prepare the data before it reaches the view. That realization helped me better understand the importance of separation of concerns and writing cleaner, more maintainable code.


# 🧩 Rental History Table Controls

> **Azure DevOps Work Item:** #20173

---

### Objective

The objective of this story was to update the Rental History table by removing the default DataTables sorting controls and associated user interface elements. The goal was to match the project's design specifications while preserving the existing table functionality.

### My Contribution

I updated the Rental History Index page by modifying the JavaScript and jQuery responsible for the DataTables configuration. I removed the default sorting controls, eliminated unnecessary interface elements, and ensured the table continued to function as expected without introducing additional sorting behavior beyond the project's requirements.

Throughout the implementation, I carefully followed the acceptance criteria to ensure that only the requested UI changes were made.

### Challenges

One of the primary challenges was understanding how the existing DataTables plugin generated its interface. Because the project already relied on third-party JavaScript, I first needed to understand the existing implementation before making targeted modifications.

Another important consideration was following the acceptance criteria precisely. Although implementing custom sorting may have seemed like a natural next step, the project documentation specifically required only the removal of the sorting controls—not replacing them with new functionality.

### Solution

I updated the existing JavaScript and jQuery configuration to remove the DataTables sorting controls while preserving the remainder of the table's functionality. After testing the page, I verified that the unwanted UI elements had been removed and that the page matched the project's expected design.

### Technologies Used

- JavaScript
- jQuery
- DataTables
- ASP.NET MVC
- Razor
- HTML
- CSS

### Technical Skills Applied

- JavaScript
- jQuery
- DOM Manipulation
- Working with Third-Party Libraries
- Reading Existing Code
- Debugging
- Following Acceptance Criteria

### Code Highlight

```cshtml
<div class="form-inline">
    <label for="rentalHistorySort" class="mr-2 mb-0">Sorted by:</label>

    <select id="rentalHistorySort" class="form-control">
        <option value="none">No Extra Sorting...</option>
        <option value="damaged">Damaged Rentals</option>
        <option value="undamaged">Undamaged Rentals</option>
        <option value="az">Rentals A - Z</option>
        <option value="za">Rentals Z - A</option>
    </select>
</div>
```

```
switch (sortOption)
{
    case "damaged":
        rentalHistory = rentalHistory
            .Where(r => r.RentalDamaged)
            .ToList();
        break;

    case "az":
        rentalHistory = rentalHistory
            .OrderBy(r => r.RenterName)
            .ToList();
        break;

    case "za":
        rentalHistory = rentalHistory
            .OrderByDescending(r => r.RenterName)
            .ToList();
        break;
}
```

This Razor view introduces a custom sorting interface that replaces the default DataTables controls with a cleaner, application-specific experience. The custom Bootstrap form allows users to organize Rental History records while maintaining consistency with the application's overall design and preserving the existing MVC workflow.

### Final Result

The Rental History table now matches the project's design specifications by removing the default DataTables sorting controls while preserving the existing functionality and user experience.

### What I Learned

This story gave me valuable experience working with an existing JavaScript library rather than building functionality from scratch. I learned how important it is to understand the behavior of third-party code before making modifications and reinforced the importance of implementing exactly what the project requirements specify—no more and no less.

# 📈 Professional Growth

Working on TheatreCMS was my first experience contributing to a collaborative ASP.NET MVC application within an Agile development environment. Each work item challenged me to build on previous knowledge while learning how to navigate and contribute to an existing codebase.

Throughout these stories, I became more comfortable working across both the front end and back end of an application. I gained practical experience with Razor views, C# controllers, Entity Framework, Bootstrap, JavaScript, and jQuery while learning how each technology fits into the overall MVC architecture.

One of my biggest takeaways was learning to think beyond simply making code work. As I progressed through the project, I developed a greater appreciation for writing maintainable code, following established project conventions, and keeping responsibilities properly separated within the MVC framework.


# 🤝 Working in an Agile Team

Beyond writing code, this project introduced me to the collaborative workflow used by professional software development teams.

Throughout the project I worked with:

- Azure DevOps work items
- Agile/Scrum development practices
- Daily stand-up meetings
- Sprint planning
- Code retrospectives
- Pull requests
- Code reviews
- Git version control

Each feature was developed according to defined acceptance criteria, submitted for review, and refined before completion. This process taught me the importance of communication, incremental development, and collaborating within an established engineering workflow.


# 🎯 Final Reflection

Looking back on this project, I can clearly see how much I grew as a developer. I began by focusing on completing individual tasks, but over time I started thinking more critically about software architecture, maintainability, and the reasoning behind design decisions.

TheatreCMS gave me valuable experience working within an existing application rather than building a project from scratch. Learning to understand someone else's code, make targeted improvements, and contribute without disrupting the overall application has been one of the most rewarding parts of this experience.

Most importantly, this project reinforced that software development is about much more than writing code. It requires communication, problem-solving, attention to detail, and a willingness to continuously learn from each feature you implement.

As I move into the next stage of my career, I look forward to contributing these skills to a professional development team while continuing to grow as a software engineer.
