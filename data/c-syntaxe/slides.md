!SLIDE subsection ================

# syntaxe



!SLIDE smallcode topmargin ===========================

    @NgModule({
      declarations: [ AppComponent,
                     HighlightDirective,
                     TitleComponent ],
      imports:      [ BrowserModule,
                     ContactModule ],
      exports:      [ AppComponent ],

      bootstrap:    [ AppComponent ],
      providers:    [ UserService ],
      entryComponents : []
    })
    export class AppModule { }


!SLIDE smallcode topmargin ===========================

      declarations: [ AppComponent,
                     HighlightDirective,
                     TitleComponent ],
<br>
## contenu du module
### components, directives, pipes
### _privé par défaut_

!SLIDE smallcode topmargin ===========================

      imports:      [ BrowserModule,
                     ContactModule ],
<br>
## ce dont a besoin le module
### autres modules fournissant des déclarations<br>pour ses templates

!NOTES ---------------------------
- plus besoin d'importer FORM_DIRECTIVES dans chaque template


!SLIDE smallcode topmargin ===========================

      exports:      [ AppComponent ],
<br>
## ce que publie le module
### certaines de ses déclarations,
### ou d'autres modules


!SLIDE smallcode topmargin ===========================

      bootstrap:    [ AppComponent ],
<br>
## démarrage
### composant principal de l'appli



!SLIDE smallcode topmargin ===========================

      providers:    [ UserService ],
<br>
## services globaux
### publie des services à la racine





!SLIDE subsection ================

# types de modules


!SLIDE smallcode ===========================

## root AppModule

    platformBrowserDynamic()
        .bootstrapModule(AppModule);


!SLIDE smallcode ===========================

## Feature Module
### = partie de l'application

!SLIDE smallcode ===========================

## Widget Module
## (_aka_ Shared Module ?)
### components / directives / pipes

!SLIDE smallcode ===========================

## Service Module
## (_aka_ Core Module ?)
### providers globaux




