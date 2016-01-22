[back to summary](https://github.com/ByJC/angular2-step-by-step)

# 1-step : Angular 2 - How to start ?  

First of All, Even if angular 2 is written in TypeScript, you don't have to use it to develop angular 2 applications. The Framework also work with ES5, ES6 and Dart.

## How to choose one ?

ES5 is the JavaScript you know and use in the current browser. It is what it is and does not require a build step to transform it into something that will run in today's browsers

ES6 is the next iteration of JavaScript, but it does not run in today's browsers. There are quite a few transpilers that will export ES5 for running in browsers (like [Babel](https://babeljs.io/) ). It is still an dynamic (read: untyped) language.

TypeScript provides an optional typing system while pulling in features from future versions of JavaScript (ES6 and ES7).

Dart is an experimental language created several years ago by google but I'm not so confident to talk about it.

I decided to choose TypeScript for this project because I think there are good things in it like Types, Annotations, a better documentation (for now) and because it seems that the learning curves from ES6 is quite good.

## Example of components for each languages

ES5 :
```js
var AppComponent = function () {

};

AppComponent.annotations = [
  new ng.Component({
    selector: 'my-app',
    template: '<h1>First Step with angular2-step-by-step</h1>'
  })
];
```


ES6 :
```js
(function(app) {
  app.AppComponent =
    ng.core.Component({
      selector: 'my-app',
      template: '<h1>First Step with angular2-step-by-step</h1>'
    })
    .Class({
      constructor: function() {}
    });
})(window.app || (window.app = {}));
```

TypeScript :
```js
@Component({
    selector: 'my-app',
    template: '<h1>First Step with angular2-step-by-step</h1>'
})
export class AppComponent { }
```

## Next Step

[Let's get started with Angular 2 TypeScript](https://github.com/ByJC/angular2-step-by-step/tree/2-step)
