!SLIDE subsection ================

# lazy loading



!SLIDE smallercode top ===========================

## eager

    imports:      [ ContactModule ],




!SLIDE smallercode top ===========================

## lazy

    export const routing: ModuleWithProviders
        = RouterModule.forRoot([

      { path: '', redirectTo: 'contact', pathMatch: 'full' },

      { path: 'contact',
        component: ContactComponent }

      { path: 'crisis',
        loadChildren: 'app/crisis/crisis.module#CrisisModule' }

    ]);


!SLIDE smallercode top ===========================

## lazy + preloading

    export const routing: ModuleWithProviders
        = RouterModule.forRoot([

      { path: '', redirectTo: 'contact', pathMatch: 'full' },

      { path: 'contact',
        component: ContactComponent }

      { path: 'crisis',
        loadChildren: 'app/crisis/crisis.module#CrisisModule' }

    ], {preloadingStrategy: PreloadAllModules});



!SLIDE subsection ================

# démo

