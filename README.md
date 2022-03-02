# I've left here for launching wordpress on play-docker  

## Copy and Paste  [here](https://zenn.dev/kazurof/articles/a2de4a9fcf5dc1)
### Copy  
```Ctrl + Insert```
### Paste  
```Shift + Insert```  

## Launch on play-docker  
1. ```docker images```  
2. ```docker run -it -p 8000:80 nginx```  

## Wordpress on Docker  
1. ```docker run --name my_mysql -e MYSQL_ROOT_PASSWORD=pass -d mysql:5.7```
2. ```docker run -e WORDPRESS_DB_PASSWORD=pass --link my_mysql:mysql -d -p 8080:80 wordpress```  
