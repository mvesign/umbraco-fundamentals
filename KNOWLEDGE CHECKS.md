# Umbraco Fundamentals

Course contains several knowledge checks exercises. Below are the questions presented in these knowledge checks.

## Exercise 1: Document Types and Content

1. *What do document types do?*
   - Define what kind of content the editors will be able to fill in on the corresponding page.
   - Allow you to define the content structure.

2. *Is it possible to make content without using any Document Types?*
   - False.

## Exercise 2: Creating our View

1. *What is the correct way of executing code/getting dynamic values in a template?*
   - `@Model.`

2. *How would you render a "CompanyName" property on a template with a generic page model (ie. a model that is not strongly typed)?*
   - `@Model.Value("companyName")`

3. *What does a layout template need to function properly?*
   - A call to the `RenderBody` method.

## Exercise 3: Building a top navigation in Razor

1. *Which of these options is the best for building a top-level navigation?*
   - `@foreach (var child in Model.Root().Children())`

2. *What does the method .AncestorOrSelf(int level) do?*
   - Finds the Ancestor of the specific content item, and if an ancestor is not found or inaccessible, returns itself. The parameter limits the level of content that the method will traverse to find the Ancestor.

## Exercise 4: Creating a new section

1. *How do you build a feature in Umbraco?*
   1. Create the document types.
   2. Create a content structure.
   3. Build up the templates/HTML.
   4. Add dynamic values/code to the templates.

## Exercise 5: Media Section

1. *What approach (approaches) should be considered bad practice when it comes to adding images to your content? (Pick one or more)*
   - Hard-coding a URL to an image uploaded to the Media section.
   - Hard-coding a URL to an external image in a template.

2. *How can you render a link to an image provided via a media picker (let's assume the media picker property alias is Image)?*
   - `@Model.Image.Url()`

## Exercise 6: Image Cropper

1. *How can you crop and/or resize images in your template? (Pick one or more)*
   - Dynamically generate a crop by adding a querystring like `?width=200` to the image url in the template.
   - Define crops directly on the Image media type, then in your template, use the `.GetCropUrl()` method and choose the specific crop by name/alias.

## Exercise 7: Shared templates, document type compositions and partial views

1. *You can have a template that has three levels of template inheritance. Example:*
```plaintext
master.cshtml
    _BasicNav.html (master template: _layout)
        _ContentPage.cshtml (master template: _basicNav)
            ContactUs.cshtml (master template: _contentPage)
```
   - True.

2. *What are partial views good for? (Pick one or more)*
   - Splitting your templates into smaller, more readable chunks.
   - Storing reusable bits of HTML and Razor you can plug into other templates.

## Exercise 8: Block Grid Editor

1. *There is a default limit set on the amount of blocks you can have in a Block Grid Editor.*
   - False.

2. *How do you render a BlockGrid property on a template?*
   - `@await Html.GetBlockGridHtmlAsync(Model, "myGrid")`

## Exercise 9: Block List Editor

1. *It is possible to reuse the same Element Types you used in the Block Grid Editor, in the Block List Editor.*
   - True.

2. *How can you modify a specific block label to display a filled-in content property from said block?*
   - `{=propertyName}`

## Exercise 10: Getting started with a multi-lingual website

1. *There's a limit of 12 languages you can choose to translate your content to.*
   - False.

2. *It's possible to have a property that is not available across multiple languages on a document type that is set to vary by culture.*
   - True.