# Materialize css tabs with angular routing

[Materialize css] is awesome. It has tabs but it lacks the functionality of loading remote data on click of tab. [Angular Routing] is good framework for single page application. In case if you want to use angular routing with Materailize css tabs, then with current tabs you can't do it. So I have tweaked existing tabs little bit and created new angularTabs. 

Also it won't disturb existing tabs (default materialize css tabs), so you can use them in case you have static content.

### Prerequisite

To use angular tabs in materialize css, you will need
  - [Materialize css], both css and js
  - [jQuery]
  - [Angular JS]
  - [Angular Routing JS]
  
### How to Use
To use this download the angularTabs.js from the repository and include in your web page after materialize.js or materiliaze.min.js.

Now along with **tab** class to your **ul**, add **angularTabs** class as shown in below code. With angular routing, you will be using ng-view, so you don't need to have seperate content divs for each tab. Just place one div with ng-view. Code for sample 4 tabs should be as follow.

        <div class="row">
            <div class="col s12">
                <ul class="tabs angularTabs">
                    <li class="tab col s3"><a class="active" href="#">Tab1</a></li>
                    <li class="tab col s3"><a href="#tab2">Tab2</a></li>
                    <li class="tab col s3"><a href="#tab3">Tab3</a></li>
                    <li class="tab col s3"><a href="#tab4">Tab4</a></li>
                </ul>
            </div>
            <div class="col s12">
                <div ng-view>
                </div>
            </div>
        </div>

That's it. Now whenever you click on any tab, the location will change to href of the tab and the remote content will be loaded for that tab in ng-view with the help of routing functionality.


License
----

MIT


   [Materialize css]: <http://materializecss.com/>
   [Angular Routing]: <https://docs.angularjs.org/api/ngRoute>
   [Angular Routing JS]: <https://github.com/angular/bower-angular-route>
   [Angular JS]: <https://angularjs.org/>
   [jQuery]: <https://jquery.com/download/>
   

