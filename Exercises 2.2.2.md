1. By referring to Figure 2.11, write out the analogous steps for visiting the
URL /users/1/edit.


браузер запрашивает(URL /users/1/edit) -> Rails router сопоставляет запрос (edit) -> Controller(user_controller.rb) ищет конкретного пользователя -> получает его запись из бд -> контроллер подготавливает данные -> отправляет их во view -> рендерится представление edit.html.erb -> HTML ответ отправляется в браузер.

2. Find the line in the scaffolding code that retrieves the user from the database in the previous exercise. Hint: It’s in a special location called set_- user.

users_controller.rb ->

def set_user  
  @user = User.find(params[:id])  
end


3. What is the name of the view file for the user edit page?

edit.html.erb

app/views/users/edit.html.erb