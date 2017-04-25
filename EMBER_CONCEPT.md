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
