## i18n_filter is a Liquid filter to use I18n localization.

This plugin was forked from https://github.com/gacha/gacha.id.lv/blob/master/_plugins/i18n_filter.rb.

The reason for that was the Jekyll Server fail each time a regeneration happens. After a regeneretion, for some reason, the Jekkyl Server ignores the LOCALE informed by the plugin and says that the :en locale is not valid.

Inside the 'localize' method, I forced the I18n.locale to be the LOCALE informed by the plugin (I18n.locale = LOCALE). That way after each regeneration the plugin informs the locale that must be used.


#### Requirements

- i18n gem;
- '_plugins' folder inside the Jekyll root;
- a locale file inside '_locales' folder (get locales from here https://github.com/svenfuchs/rails-i18n/tree/master/rails/locale).


#### Install

- put the i18n_filter.rb inside the _plugins folder;
- put the locale inside the _locales folder;
- Use the I18n as is used in a Rails app.


#### Example

- {{ post.date | localize: "%d/%m/%Y" }}
- {{ post.date | localize: ":short" }}
- {{ post.date | localize: ":long" }}
