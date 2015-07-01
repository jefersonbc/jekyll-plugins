## i18n_filter is a Liquid filter to use I18n localization.

This plugin was forked from https://github.com/gacha/gacha.id.lv/blob/master/_plugins/i18n_filter.rb.

The reason for that was the Jekyll Server fail each time a regeneration happens. After a regeneretion, for some reason, the Jekkyl Server ignores the LOCALE informed by the plugin and says that the :en locale is not valid.

Inside the 'localize' method, I forced the I18n.locale to be the LOCALE informed by the plugin (I18n.locale = LOCALE). That way after each regeneration the plugin informs the locale that must be used.
