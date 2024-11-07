# Usage

_config.yml this file contains all the content for your resume.

Additional links
If you would like to add more than the predefined social links in the config file, then you can use the additional_links field to add as many additional links with urls and font awesome icons as you wish.

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
