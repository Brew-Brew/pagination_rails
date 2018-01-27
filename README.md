# Pagination with kaminari

## 컨트롤러
```ruby
@posts= Post.page params[:page]
```
## 뷰
```ruby
<%@posts.each do |post|%>
    <%=post.title%><br>
<%end%>

<%= paginate @posts %>
```
# rails g kaminari:config 명령어로 페이지네이션 갯수 정할수있음
+ 기본 25개
+ # config.window = 4 양옆 숫자

# locales/en.yml
+ prev next 를 이전 다음과 같이 바꿀수있음
```
en:
  views:
    pagination:
      first: "처음"
      last: "마지막"
      previous: "이전"
      next: "다음"
      truncate: "~~~" 
```