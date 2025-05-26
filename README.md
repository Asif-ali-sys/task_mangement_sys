# Task Management Application

This is a full-stack Task Management Application with Angular for the frontend and ASP.NET Core Web API for the backend. It allows users to create, view, update, and delete tasks, as well as filter and sort them based on status or priority.

---

# Technologies Used

- Frontend: Angular 19
- Backend: ASP.NET Core Web API (.NET 8 or higher)
- Database: SQL Server 20.0v
- Styling: Bootstrap, Angular Material
- Tools: Postman, Swagger, GitHub, Visual Studio 2022

---

# Instructions for Running the App

# Prerequisites

- Node.js and Angular CLI
- .NET 8 SDK or higher
- SQL Server
- Visual Studio or Visual Studio Code

---

# Backend Setup (ASP.NET Core)

1. Open the solution in Visual Studio.
2. Update the `appsettings.json` file with your SQL Server connection string.
3. Run the following commands in the Package Manager Console:

4. Run the project. Swagger should open at `https://localhost:<port>/swagger`.

---

# Frontend Setup (Angular)

1. Navigate to the Angular project directory:
```bash
cd TaskManagementApp-Frontend
2.npm install
3.ng serve
4.Open http://localhost:4200 in your browser.

# Test Report – Task Management App
Test Case ID	Test Description	Component	Test Type	Input	Expected Result	Status
TC_001	Load all tasks successfully	TaskController / API	Integration	-	List of tasks is returned	✅ Passed
TC_002	Add a new task with valid input	TaskController / API	Unit	Title, Desc, Priority, Status	Task added successfully	✅ Passed
TC_003	Edit an existing task	TaskController / API	Unit	Task ID + updated data	Task updated in DB	✅ Passed
TC_004	Delete task with confirmation	TaskController / API	Unit	Task ID	Task deleted from DB	✅ Passed
TC_005	Validate required fields in form	TaskFormComponent	Unit	Empty title/status	Validation error shown	✅ Passed
TC_006	Validate max length for title (100)	TaskFormComponent	Unit	Title > 100 chars	Validation error shown	✅ Passed
TC_007	Validate max length for description (500)	TaskFormComponent	Unit	Description > 500 chars	Validation error shown	✅ Passed
TC_008	Open task form in add mode	TaskManagerList	UI	Click "Add Task"	Empty modal opens	✅ Passed
TC_009	Open task form in edit mode	TaskManagerList	UI	Click "Edit"	Modal opens with task data	✅ Passed
TC_010	Search by title or description	TaskManagerList	UI	Enter search keyword	Filtered results displayed	✅ Passed
TC_011	Sort tasks by priority	TaskManagerList	UI	Select Priority dropdown	Sorted by priority	✅ Passed
TC_012	Sort tasks by status	TaskManagerList	UI	Select Status dropdown	Sorted by status	✅ Passed
TC_013	Sort tasks by created date	TaskManagerList	UI	Sort column	Sorted by created date	✅ Passed
TC_014	Display confirmation before delete	TaskManagerList	UI	Click Delete	Confirmation dialog appears	✅ Passed
TC_015	Show success alert on task addition	TaskFormComponent	UI	Submit valid task	Success message shown	✅ Passed
TC_016	Handle API failure gracefully	TaskController	Integration	Simulated API failure	Error message displayed	✅ Passed
TC_017	Jquery Datatable integration	TaskManagerList	UI	Load list	Table supports pagination/filter/sort	✅ Passed
TC_018	Form emits submit event correctly	TaskFormComponent	Unit	Valid form data	Parent receives event	✅ Passed
TC_019	Status and Priority filter combined	TaskManagerList	UI	Select both filters	Correct filtered tasks shown	✅ Passed
TC_020	CreatedAt auto-filled	TaskFormComponent	Unit	Open add task modal	Current date pre-filled

