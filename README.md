# I've left here for launching wordpress on play-docker  

## Copy and Paste  [here](https://zenn.dev/kazurof/articles/a2de4a9fcf5dc1)
### Copy  
```Ctrl + Insert```
### Paste  
```Shift + Insert```  

## Launch on play-docker  
1. ```docker images```  
2. ```docker run -it -p 8000:80 nginx```  

## Create a custom docker image  
1. Create a directory and move into it.  
```mkdir ~/mynginx && cd ~/mynginx```  
2. Create a Dockerfile in the newly created directory with the following  
content.
```
FROM nginx
COPY index.html /usr/share/nginx/html
```  
3.  Create index.html in the same directory with your favorite content  
```html
<h1>Hello, world</h1>
```  
4. Build the Docker image.  
```docker build -t citrus1998/mynginx .```
5. Check if your image has been created successfully.  
``` docker images ```  
6. Run your custom docker image.  
``` docker run -p 8000:80 citrus1998/mynginx ```  

