- マイグレーションが途中で止まってしまうエラーが発生。以下エラー文
```
rails aborted!
StandardError: An error has occurred, all later migrations canceled:

Index name 'index_graphs_on_user_id' on table 'graphs' already exists
/Users/user/Desktop/portfolio/weight_management/db/migrate/20210404180742_create_graphs.rb:3:in `change'
bin/rails:4:in `<main>'

Caused by:
ArgumentError: Index name 'index_graphs_on_user_id' on table 'graphs' already exists
/Users/user/Desktop/portfolio/weight_management/db/migrate/20210404180742_create_graphs.rb:3:in `change'
bin/rails:4:in `<main>'
Tasks: TOP => db:migrate
(See full trace by running task with --trace)
```

- やった事
```
$ rails db:migrate:reset
を実行したら成功した
```
- rails db:migrate:resetについて参考:https://blog.naichilab.com/entry/db_reset-vs-db_migrate_reset https://shonoooo.hatenablog.com/entry/2016/07/13/231338
```
# rails db:migrate:reset は db:seed は実行されないので
$ rails db:seed
を再実行した
```
