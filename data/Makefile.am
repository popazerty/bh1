SUBDIRS = countries fonts defaults extensions keymaps skin_default   

dist_pkgdata_DATA = \
	defaultsatlists.xml \
	defaultwizard.xml \
	dreampackagewizard.xml \
	encoding.conf \
	keymap.xml \
	menu.xml \
	prev.png \
	radio.mvi \
      radio-hd.mvi \
	rcpositions.xml \
	setup.xml \
	skin_default.xml \
	skin.xml \
	startwizard.xml \
	tutorialwizard.xml \
	unicable.xml

if HAVE_TEXTLCD
dist_pkgdata_DATA += skin_text.xml
else
if HAVE_COLORLCD
dist_pkgdata_DATA += skin_display96.xml
else
dist_pkgdata_DATA += skin_display.xml
endif
endif

skin_display.xml: $(srcdir)/skin_display_default.xml
	test -f $(srcdir)/skin_display_$(BOXTYPE).xml && cp $(srcdir)/skin_display_$(BOXTYPE).xml skin_display.xml || cp $(srcdir)/skin_display_default.xml skin_display.xml
