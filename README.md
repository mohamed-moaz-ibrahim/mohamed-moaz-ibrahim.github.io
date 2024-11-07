all steps to create a same resume could be found in this [repo](https://github.com/sproogen/modern-resume-theme?tab=readme-ov-file)

this is resume using Github Pages.

[check my resume website](https://mohamed-moaz-ibrahim.github.io)

# Usage

_config.yml this file contains all the content for your resume.

### Content
The main content for you resume will all come under the content property in the _config.yml file. This can be quite complex and a good understanding on YAML will be helpful here.

Content will contain an array of sections, there are currently 2 types of layouts for content sections, text and list.

text is a basic layout that contains markdown content.
list is a the standard layout that is used for things like Education and Experience.

Below is a the full list of content options.

```
content:
  - title: Section Name
    layout: list (options: list, text)
    content:
      - layout: left (options: left, right, top, top-right, top-middle)(default: left)
        title: Name of item (eg. Company or Project name)
        sub_title: Sub title (eg. Qualification or Job title)(optional)
        caption: Item caption (eg. Employment or course dates)(optional)
        link: Web link (eg. https://sproogen.github.io/modern-resume-theme)(optional)
        link_text: Text for link (optional: without this link will show URL as link text)
        additional_links: (optional)
          - title: Link name
            icon: Font Awesome brand icon name (eg. fab fa-twitter) (https://fontawesome.com/icons?d=gallery&s=brands&m=free)
            url: Link url (eg. https://google.com)
        quote: >
          Short overview or quote for the item
        description: | # this will include new lines to allow paragraphs
          Main content area for the list item.
  - title: Section Name
    layout: text (options: list, text)
    content: | # this will include new lines to allow paragraphs
      This is where you can write a little more about yourself. You could title this section **Interests** and include some of your other interests.

      Or you could title it **Skills** and write a bit more about things that make you more desirable, like *leadership* or *teamwork*
```

Note: The description or content areas (fields starting with | #) use markdown, this means that you have the ability to format the section in many different ways and add things such as images, code & syntax highlighting and tables. You can find a good Markdown cheatsheet here

### Additional links
If you would like to add more than the predefined social links in the config file, then you can use the additional_links field to add as many additional links with urls and font awesome icons as you wish.

### Dark Mode
Dark mode is configured via _config.yml
> darkmode: true (options: true, false, never)

When dark mode is true the site will show the dark theme for everyone.

When dark mode is false the site will not show the dark theme, but it will still respect the users device preferences.

When dark mode is never the site will never be shown in the dark theme.

assets/main.scss
Add any css changes or additions you want to make here after the line @import 'modern-resume-theme';

# Running locally
Before you start make sure you have Ruby and the gems for Jekyll installed locally. You can find out how to do that here.

```
bundle install
bundle exec jekyll serve
Open your browser to http://localhost:4000
```

Any changes you make will automatically build and you will be able to see these by refreshing your browser.

Note: You will need to re-run bundle exec jekyll serve to see changes made in _config.yml.
