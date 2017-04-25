# EMBERJS CONCEPT
* [Ember Services](https://guides.emberjs.com/v2.12.0/applications/services/) - An Ember.Service is an Ember object that lives for the duration of the application, and can be made available in different parts of your application.

* [Ember JS for Beginners](https://viblo.asia/thaont/posts/wznVGLdjGZOe) - Nice summary for Emberjs to beginners.

* [Talk Promises](http://bantic.github.io/talks-promises/#/12)

* [RSVP JS](https://github.com/nvminhtu/rsvp.js)

* [RSVP JS in EMBERJS](https://www.emberjs.com/api/classes/RSVP.html)

## EMBERJS OBJECT MODEL

### 1. OBJECT MODEL
* Plain Javascript objects lack the ability to be dependent on other properties changes => Ember Model solve it.
* Most objects in Ember, including routes, Ember Data models, services and components extend Ember.Object.
* Use `object.id = "value"` but rather `object.set('id', "value")`

### 2. ROUTING
* Ember is URL-driven
* Where to add? `router.js`
* Use: `this.route('item', { path: '/items/:item_id' });`
* Setup Route
`export default Ember.Route.extend({
  model(params) {
    return {
      id: params.item_id,
      text: "This is item " + params.item_id
    }
  }
});`

### 3. Data Down, Actions Up
*
`export default Ember.Route.extend({
  actions: {
    remove(item) {
      item.remove().then(() => {
        this.transitionTo('index');
      });
    }
  }
  ...
});`

### 4. Models
* A model can be fetched with the Ember.$.getJSON() utility:
`export default Ember.Route.extend({
  model() {
    return Ember.$.getJSON('/items.json');
  }
});`
* Return Value => ? (answer: No) => It return Promises
* Or Ember Data
`export default Ember.Route.extend({
  model(params) {
    return this.store.findRecord('item', params.item_id);
  }
});`

### 5. Services
* Ember’s Injection API
* An Ember.Service is a long-lived object (singleton) used to provide services to other Ember objects

### 6.Components
* Components consist of two parts: a Javascript component file (that defines behavior) and its accompanying Handlebars template.
`// app/components/item-display.js

export default Ember.Component.extend({
  isModelTwo: Ember.computed('model.id', function() {
    return this.get('model.id') == 2;
  })
});`

`{{!-- app/templates/components/item-display.hbs  --}}<h1>{{ model.text }}</h1>{{#if isModelTwo}} <p><strong>OMG MODEL TWO!</strong></p>{{/if}}`
* Component can include other components.


### Reference
* [EmberJS Object Model](https://emberigniter.com/5-essential-ember-concepts/)
