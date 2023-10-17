# API 文档（粗略版

## 模块

```

user登录

user{
	id:string,
	name:string,
	avator,
	follow: id[]
	fans: id[],
	articles : articles[],
	collection : asrticles[]
}


article {
	id,
	title,
	content: string,
	time,
	class,
	discuss,
	stars : 点赞数
}


discuss{
	user,
	time,
	content,
	target
}

```

## 内容

根据学科 语文 数学 英语 科学

首页：根据点赞数/最新





## API 

```

登录注册，如果数据库不存在用户则先注册再返回
GET /login 
params {
	id: string,
	password: stirng
}
res {
	user
}

根据类别获取文章列表
GET /get_articles
params {
	class
}
res {
	data: articles[]
}

发布文章
POST /post_article
params {
	writer,
	article
	time
	class
}
res {
  ok
}

点赞
GET /star
params {
	articleId
}
res {
	ok
}

关注
GET /follow
params{
	userId
	targetId
}
res {
	ok
}

收藏
GET /collect
params {
	userId,
	articleId
}

根据文章id或文章名字返回整个文章
GET /get_article 
params {
	articleId / title
}
res {
	article
}




```





##  推荐

根据用户的收藏点赞，得到他喜欢的tag，根据这个tag推送

tag在后端限定



分类

tag对用户不可见，用于分类推荐





## 后台管理

审核分类

删除垃圾文章



管理员用户

























