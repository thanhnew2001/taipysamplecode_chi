<|{all_projects}|table|columns={project_columns}|width='100%'|on_action={on_project_table_click}|style=project_style|>
<|Create Project|button|on_action={open_create_project_dialog}|>
<|Refresh Projects|button|on_action={refresh_project_list}|>

<|{show_dialog_create_project}|dialog|title=Create new project|
<|{project_name}|input|placeholder='Enter project name'|
<|Create|button|on_action={create_project}|>
<|Cancel|button|on_action={close_create_project_dialog}|>
|>

<|{show_project_details}|pane|

# Project Details <|Delete|button|on_action=delete_selected_project|> <|Archive|button|on_action=archive_selected_project|>

<|layout|columns=1 1|
<|part|class_name=card|
## Project Name
<|{selected_project.name}|>
|>

<|part|class_name=card|
## Project Manager
<|{selected_project.manager}|>
|>

<|part|class_name=card|
## ID
<|{selected_project.id}|>
|>

<|part|class_name=card|
## Start Date
<|{selected_project.start_date.strftime("%b %d %y")}|>
|>

<|part|class_name=card|
## Status
<|{get_project_status(selected_project)}|>
|>

----
|>
