default prefix -> /hostname:8888/

UPORABNIK
POST /user/register
POST /user/login

OBJAVE
POST /posts/
GET  /posts/
GET  /posts/{postId}

UPRAVLJANJE komentarjev
POST /comments/
GET  /comments/?postID=...
GET  /comments/commentId
DELETE /comments/commentId
POST /comments/like

SPOROČILNI SISTEM
POST /messaging/?userIdFrom=...,userIdTo=...
GET /messaging/?userId=...
