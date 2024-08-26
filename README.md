# Popup web component

Popup web component for Cradle CMS.

1. Add the file in the `components` folder.
2. Include in layout file `theme.liquid` or in a specific template such as `page.liquid` with `{% component 'popup' %}`. 
3. Add a button that opens the popup `<button id="<button-id>">Contact</button>`.
4. Add the `<pop-up>` element with attributes and content.

## The attributes and content

### Connect with button
Set target for the button with replacing `<button-id>`. 

### Attributes
* Width - popupwidth : Add a number in px , if removed the default is 400px.
* Background - popupbg : Sets the background color for the whole popup but in practise only for the header, if removed dafault is white.
* Content background : Sets the background color for the content/main part.

### Content
There is two content slots: header and main, fill with the desired content. With Cradle CMS it is possible to build a form and include the html with `{% form '<form-handle>' %}{% endform %}`

```
<pop-up target="<button-id>" popupwidth="<set width in px, default is 400px>" popupbg="background color for the popup header, default is white" mainbg="background color for the main content, default is white" >
    <div slot="header">
      <!-- replace with content for header -->
    </div>
    <div slot="main">
      <!-- replace with content for main body of popup -->
    </div>
</pop-up>
```
