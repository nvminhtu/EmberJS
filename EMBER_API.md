# EMBERJS API
### BEST PRACTICES in EMBERJS
* [Ember Style GUIDE](https://github.com/DockYard/styleguides/blob/master/engineering/ember.md#general)

### CLASSES using in TEMPLATE
* [METHOD CONCAT](https://emberjs.com/api/classes/Ember.Templates.helpers.html#method_concat)
> Concatenates the given arguments into a string.
{{some-component name=(concat firstName " " lastName)}}
{{component (concat 'header-' startup.tag)}}

* [LINK-TO HELPER](https://guides.emberjs.com/v2.9.0/templates/links/) - It's Default Helper of EmberJS
A link in {{#link-to "index"}}Block Expression Form{{/link-to}}

* [Talk Promises](http://bantic.github.io/talks-promises/#/12)

* [RSVP JS](https://github.com/nvminhtu/rsvp.js)

* [RSVP JS in EMBERJS](https://www.emberjs.com/api/classes/RSVP.html)

* [this.get('ajax').request in emberjs](https://github.com/ember-cli/ember-ajax) - Using get Ajax in Ember JS, được cài mặc định trong ember-ajax (đã tích hợp trong ember-cli).

* [Ember Servces](https://guides.emberjs.com/v2.12.0/applications/services/) - An Ember.Service is an Ember object that lives for the duration of the application, and can be made available in different parts of your application.

* [Ember JS for Beginners](https://viblo.asia/thaont/posts/wznVGLdjGZOe) - Nice summary for Emberjs to beginners.

### Các ghi chú
* ember destroy (sử dụng cái này để xóa component, route,...).
* khi khởi tạo 1 component không muốn chạy POD (vì trong source đã setup PODs: true) => thì khi tạo mới:
ember g component demo-comp --pod (ta sẽ tạo ra Component ko theo dạng POD)
