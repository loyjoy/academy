# How to add email HTML templates in LoyJoy

## 1. What this solution will do for you

There are multiple points where you can configure email templates in LoyJoy.
This guide will explain how you can configure these to your liking.

## 2. What you need for this solution to work

Ideally, you would already have an HTML template that you want to enter.

If you do not have a template you can create a template in one of these ways:
- Manually create an HTML template
- Copy the HTML from one of your existing emails
- Create an HTML template using a tool such as Canva

## 3. Add the template to LoyJoy

You can add the template to by copying all of the html code to text area in
LoyJoy. To check that it's working, you can use the "Preview" button right
above the text area.

In the template, you can use the `${variable_name}` syntax to add variables
from LoyJoy to the email that will be sent out. In the preview, the
`${variable_name}` will be shown as-is, without exchanging the text.

## 4. Change images in the template

Since the email template is not created by LoyJoy, all images used have to be
hosted externally as well. Usually image assets should be hosted on your
website.

To change an image, you can either change the URL in the HTML template to point
to another image. Or you can replace the image you want to change on the
server.
