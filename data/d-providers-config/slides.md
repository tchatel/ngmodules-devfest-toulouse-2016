!SLIDE subsection ================

# providers & config


!SLIDE ===========================

# DI
## type-based
## hierarchical


!SLIDE ===========================

## <span class="red">bootstrapped</span> module
# providers globaux
## _(application-scoped)_


!SLIDE ===========================

## ex : HttpModule


!SLIDE ===========================

# surchargeable
## dans le root AppModule


!SLIDE ===========================

## <span class="red">lazy</span> module
# providers locaux
## _(module-scoped)_


!SLIDE smallcode top ===========================

# ModuleWithProviders
### _(module configuré)_
<br>

    export interface ModuleWithProviders {
        ngModule: Type;
        providers?: any[];
    }


!SLIDE smallercode top ===========================

    export const routing: ModuleWithProviders
        = RouterModule.forRoot([
      { path: '', redirectTo: 'contact', pathMatch: 'full' },
      { path: 'contact', component: ContactComponent }
    ]);
<br>

    @NgModule({
      imports: [
        BrowserModule,
        ContactModule,
        routing
      ],
      declarations: [ AppComponent ],
      bootstrap:    [ AppComponent ]
    })
    export class AppModule { }


!SLIDE smallercode top ===========================

## convention

### `.forRoot()`  => import dans le root AppModule
### `.forChild()` => import dans un Feature Module

      static forRoot(config: UserServiceConfig):
             ModuleWithProviders {
        return {
          ngModule: CoreModule,
          providers: [
            {provide: UserServiceConfig, useValue: config }
          ]
        };
      }
