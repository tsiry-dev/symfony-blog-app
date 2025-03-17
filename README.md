# symfony-blog-app
Blogg en symfony



------------CREATION DE L'ENTITÉ articles-----------------
   -id
   -title
   -slug
   -content
   -featuredText
   featuredImage ->relation->Media->ManyToOne
   -createdAt
   -updatedAt

------------CREATION DE L'ENTITÉ Media-----------------
    -id
    -name
    -altText
    -filename

------------CREATION DE L'ENTITÉ Category-----------------
   -id
   -name
   -slug
   -createdAt
   -updatedAt
->RELATION MANY TO MANY (avec la table articles => article->relation->manyToMany)

Une category peut avoir plusieurs articles
Une article peut avoir plusieurs categories
Introduit la relation article dans la creation de la table category




------------CREATION DE L'ENTITÉ Comment-----------------
    -id
    -content
    -createdAt
   ->RELATION ONE TO MANY (avec la table articles => article->relation->oneToMany)


------------CREATION DE L'ENTITÉ Option ()-----------------
    -id
    -label
    -name
    -value
    -type

------------CREATION DE L'ENTITÉ Page ()-----------------
    -id
    -title
    -slug
    -content
    -createdAt
    -updatedAt

------------CREATION DE L'ENTITÉ Menu ()-----------------
    -id
    -name
    -menuOrder (int)
    -subMenus->relation->Menus->ManyToMany
    -isVisible (bool)
    -article->relation->Articles->ManyToOne
    -category->relation->Categories->ManyToOne
    -page->relation->Page->ManyToOne
    -link
    -createdAt
    -updatedAt




-----------------------------------------------CREATION DU CONTROLLER-------------------------------------------
-----> ArticlesController.php
-----> CategorYController.php
-----> CommentController.php
----->PageController.php