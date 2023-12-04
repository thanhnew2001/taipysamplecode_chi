<|{all_users}|table|columns={user_columns}|width='100%'|on_action={on_user_table_click}|style=user_style|>
<|Add User|button|on_action={open_add_user_dialog}|>
<|Refresh Users|button|on_action={refresh_user_list}|>

<|{show_dialog_add_user}|dialog|title=Add new user|
<|{new_user_name}|input|placeholder='Enter user name'|
<|{new_user_role}|selector|lov={get_all_roles()}|>
<|Add|button|on_action={add_user}|>
<|Cancel|button|on_action={close_add_user_dialog}|>
|>

<|{show_user_details}|pane|

# User Details <|Delete|button|on_action=delete_selected_user|> <|Disable|button|on_action=disable_selected_user|>

<|layout|columns=1 1|
<|part|class_name=card|
## Name
<|{selected_user.name}|>
|>

<|part|class_name=card|
## Role
<|{selected_user.role}|>
|>

<|part|class_name=card|
## ID
<|{selected_user.id}|>
|>

<|part|class_name=card|
## Creation Date
<|{selected_user.creation_date.strftime("%b %d %y %H:%M:%S")}|>
|>

<|part|class_name=card|
## Status
<|{get_status(selected_user)}|>
|>

----
|>
