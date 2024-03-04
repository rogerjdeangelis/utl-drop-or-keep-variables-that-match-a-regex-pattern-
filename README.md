# utl-drop-or-keep-variables-that-match-a-regex-pattern-
Drop or keep variables that match a regex pattern
    %let pgm=utl-drop-or-keep-variables-that-match-a-regex-pattern;                                                                
                                                                                                                                   
    Drop or keep variables that match a regex pattern                                                                              
                                                                                                                                   
    github                                                                                                                         
    https://tinyurl.com/5n6pcrbh                                                                                                   
    https://github.com/rogerjdeangelis/utl-drop-or-keep-variables-that-match-a-regex-pattern-                                      
                                                                                                                                   
    macros                                                                                                                         
    https://tinyurl.com/y9nfugth                                                                                                   
    https://github.com/rogerjdeangelis/utl-macros-used-in-many-of-rogerjdeangelis-repositories                                     
                                                                                                                                   
    /**************************************************************************************************************************/   
    /*                                                                                                                        */   
    /*                INPUT                                                                                                   */   
    /*                                                                                                                        */   
    /* NAME       SEX    AGE    HEIGHT    WEIGHT         DROP VARS THAT                       HEIGHT AND WEIGHT               */   
    /*                                                   END WITH 'EIGHT'                     ARE DROPPED                     */   
    /* Alfred      M      14     69.0      112.5                                                                              */   
    /* Alice       F      13     56.5       84.0         data want_drop / view=want_drop;      NAME       SEX    AGE          */   
    /* Barbara     F      13     65.3       98.0                                                                              */   
    /* Carol       F      14     62.8      102.5           set sashelp.class(drop=             Alfred      M      14          */   
    /* Henry       M      14     63.5      102.5                %utl_varlist(                  Alice       F      13          */   
    /*                                                              sashelp.class              Barbara     F      13          */   
    /*                                                             ,prx=/EIGHT$/i));           Carol       F      14          */   
    /*                                                                                         Henry       M      14          */   
    /*                                                   run;quit;                                                            */   
    /*                                                                                                                        */   
    /*                                                                                                                        */   
    /*                                                   KEEP VARS THAT                       HEIGHT AND WEIGHT               */   
    /*                                                   END WITH EIGHT                       ARE KRPT                        */   
    /*                                                                                                                        */   
    /*                                                   data want_keep / view=want_keep;       HEIGHT    WEIGHT              */   
    /*                                                                                                                        */   
    /*                                                     set sashelp.class(keep=               69.0      112.5              */   
    /*                                                           %utl_varlist(                   56.5       84.0              */   
    /*                                                              sashelp.class                65.3       98.0              */   
    /*                                                             ,prx=/EIGHT$/i));             62.8      102.5              */   
    /*                                                                                           63.5      102.5              */   
    /*                                                   run;quit;                                                            */   
    /*                                                                                                                        */   
    /**************************************************************************************************************************/   
                                                                                                                                   
    /*              _                                                                                                              
      ___ _ __   __| |                                                                                                             
     / _ \ `_ \ / _` |                                                                                                             
    |  __/ | | | (_| |                                                                                                             
     \___|_| |_|\__,_|                                                                                                             
                                                                                                                                   
    */                                                                                                                             
                                                                                                                                   
