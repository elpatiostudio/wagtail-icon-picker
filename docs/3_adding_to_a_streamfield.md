# Adding to a StreamField

To add the icon chooser to a StreamField, import and use the `IcofontPickerBlock`.

```python
from wagtail.models import Page
from wagtail.fields import StreamField
from wagtail_icon_picker.blocks import IcofontPickerBlock


class MyStreamFieldPage(Page):
    body = StreamField([
        ('icon', IcofontPickerBlock(default="icofont-tree")),
    ])

    content_panels = Page.content_panels + [
        StreamFieldPanel('body'),
    ]
```
