Recent Tracks Last.fm Plugin jQuery
=====================================

![Screenshot](http://c2.staticflickr.com/2/1687/23981960244_16781b0216_z.jpg)

How to use
----------

   Include the latest version jQuery Framework, then .js into the page:
     
##Example


    #JS
    <script src="http://ajax.googleapis.com/ajax/libs/jquery/1.12.0/jquery.min.js"></script> 
    <script src="http://cdnjs.cloudflare.com/ajax/libs/handlebars.js/1.0.0-rc.3/handlebars.min.js"></script>
    <script src="js/last.fm.js"></script>

    lastfm.init({        

       template: $('#tracks-template').html(),

       container: $('.container'),

       username: 'thinkphp',

       count: 10,       

       apikey: '<your api key here>'
    })


    #HTML

    <h1 id="recent-header"></h1>
    <div class="container">
            <img class="loading" src="img/preloader.gif" alt="Loading" title="Loading">
    </div>

    <script id="tracks-template" type="text/x-handlebars-template">
            {{#each this}}
                <div class="lastfm cf">
                    <div class="cover">
                        <a href="{{link}}" title="{{song}}">
                            <img src="images/vinyl.png" class="highlight">
                        </a>
                        {{#if image}}
                        <img alt="{{album}}" src="{{image}}">
                        {{else}}
                        <img alt="{{album}}" src="images/noartwork.png">
                        {{/if}}
                    </div>
                    <div class="info">
                        <p class="song">{{song}}</p>
                        <p class="artist">{{artist}}</p>
                        <p class="album">{{album}}</p>
                    </div>
                </div>
            {{/each}}
    </script>
