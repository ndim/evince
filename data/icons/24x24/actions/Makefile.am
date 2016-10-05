themedir = $(pkgdatadir)/icons/hicolor
size = 24x24
context = actions

iconsdir = $(themedir)/$(size)/$(context)

icons_DATA = \
	stock_filters-invert.png	\
	view-page-continuous.png	\
	view-page-facing.png		\
	object-rotate-left.png		\
	object-rotate-right.png

noinst_DATA = 

INKSCAPE_OPTS = --without-gui
INKSCAPE_OPTS += --export-area-page
INKSCAPE_OPTS += --export-width 24 --export-height=24

# noinst_DATA += zoom.svg
icons_DATA  += $(srcdir)/zoom.png

# noinst_DATA += zoom-fit-page.svg
icons_DATA  += $(srcdir)/zoom-fit-page.png

# noinst_DATA += zoom-fit-width.svg
icons_DATA  += $(srcdir)/zoom-fit-width.png

# noinst_DATA += zoom-fit-height.svg
icons_DATA  += $(srcdir)/zoom-fit-height.png

if HAVE_INKSCAPE
$(srcdir)/%.png: $(srcdir)/../../22x22/actions/%.svg
	$(INKSCAPE) $(INKSCAPE_OPTS) --export-png=$@ $<
if HAVE_PNGCRUSH
	$(PNGCRUSH) -ow $@
endif
endif

EXTRA_DIST = \
	$(icons_DATA)	\
	$(noinst_DATA)

-include $(top_srcdir)/git.mk
