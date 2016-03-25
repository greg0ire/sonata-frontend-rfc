
# The Admin List View

`.sonata-admin-list`

The list component MUST have a `data-list-mode` attribute with its value set to the lowercased list mode identifier.

It MUST have a modifier: `sonata-admin-list--mode-{mode}` where mode is the value of the `data-list-mode` attribute.

```html
<div class="sonata-admin-list sonata-admin-list--mode-list" data-list-mode="list">
    <table>...</table>
</div>
```

## Elements

### List item
A list item represents an individual object/entity of the ListMapper object.

It MUST have the class `sonata-admin-list__item`.

It MUST have a `data-object-id` attribute, whose value is set to the result of calling `Admin::id($object)`.

```html
<div class="sonata-admin-list sonata-admin-list--mode-list" data-list-mode="list">
    <table>
        <tbody>
            <tr class="sonata-admin-list__item" data-object-id="42"></tr>
        </tbody>
    </table>
</div>
```

### List item field
A list item field element MUST be a descendant of a `sonata-admin-list__item` element.

It represents a field of the the object represented by it's parent list item element.

It MUST have the class `sonata-admin-list__item__field`.

It MUST have a `data-field-type` attribute set to the value of the type property of the FieldDescription object.

It SHOULD have a type modifier `sonata-admin-list__item__field--type-{type}` where `{type}` is the value of its `data-field-type` attribute.

If the field can be edited inline, it MUST have an editable modifier: `sonata-admin-list__item__field--is-editable`.

For example:
```html
<div class="sonata-admin-list sonata-admin-list--mode-list">
    <table>
        <tbody>
            <tr class="sonata-admin-list__item" data-object-id="42">
                <td>
                    <div class="
                        sonata-admin-list__item__field
                        sonata-admin-list__item__field--type-batch
                      "
                      data-field-type="batch"
                    >
                      Batch selection checkbox
                    </div>
                </td>
                <td>
                    <div class="
                        sonata-admin-list__item__field
                        sonata-admin-list__item__field--type-boolean
                        sonata-admin-list__item__field--is-editable
                      "
                      data-field-type="boolean"
                    >
                      An editable boolean field
                    </div>
                </td>
                <td>
                    <div class="
                        sonata-admin-list__item__field
                        sonata-admin-list__item__field--type-actions
                      "
                      data-field-type="actions"
                    >
                      The item action buttons (show/edit/delete/...)
                    </div>
                </td>
            </tr>
        </tbody>
    </table>
</div>
```
