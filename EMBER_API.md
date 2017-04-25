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

* [this.get('ajax').request in emberjs](https://github.com/ember-cli/ember-ajax) - Using get Ajax in Ember JS, được cài mặc định trong ember-ajax (đã tích hợp trong ember-cli).

### Các ghi chú
* ember destroy (sử dụng cái này để xóa component, route,...).
* khi khởi tạo 1 component không muốn chạy POD (vì trong source đã setup PODs: true) => thì khi tạo mới:
ember g component demo-comp --pod (ta sẽ tạo ra Component ko theo dạng POD)
