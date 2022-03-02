# todolist-again

## MONGODB

### 設定環境

```
sudo su -
touch /etc/profile.d/custom_env.sh
vi /etc/profile.d/custom_env.sh
export MONGODB_URI="mongodb+srv://[DB 帳號]:[DB 密碼]@cluster0.4fvs5.mongodb.net/todo-list?retryWrites=true&w=majority"
```
打開 powershell admin 模式
```
wsl --shutdown
```
檢查
```
env | grep MONGODB_URI
```

沒有設定成功的話會跳錯誤，忘記存下訊息，但大致上是說 process.env.MONGODB_URI 應該是 string 而非 undefined

### mongoose

安裝最新版的可以消滅下列的錯誤訊息

```
(node:1399) Warning: Accessing non-existent property 'count' of module exports inside circular dependency
(Use `node --trace-warnings ...` to show where the warning was created)
(node:1399) Warning: Accessing non-existent property 'findOne' of module exports inside circular dependency
(node:1399) Warning: Accessing non-existent property 'remove' of module exports inside circular dependency
(node:1399) Warning: Accessing non-existent property 'updateOne' of module exports inside circular dependency
```

## handlebars

會出現 found 1 high severity vulnerability  
但課程用沒差

