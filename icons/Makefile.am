
iconsdir=$(datadir)/icons/hicolor
appicons16dir=$(iconsdir)/16x16/apps
appicons22dir=$(iconsdir)/22x22/apps
appicons24dir=$(iconsdir)/24x24/apps
appicons32dir=$(iconsdir)/32x32/apps
appicons48dir=$(iconsdir)/48x48/apps
appiconsscalabledir=$(iconsdir)/scalable/apps
mimeicons16dir=$(iconsdir)/16x16/mimetypes
mimeicons22dir=$(iconsdir)/22x22/mimetypes
mimeicons24dir=$(iconsdir)/24x24/mimetypes
mimeicons32dir=$(iconsdir)/32x32/mimetypes
mimeiconsscalabledir=$(iconsdir)/scalable/mimetypes
pixmapsdir=$(datadir)/pixmaps
uiiconsdir=$(datadir)/poedit/icons

appicons16_DATA = appicon/16x16/apps/poedit.png
appicons22_DATA = appicon/22x22/apps/poedit.png
appicons24_DATA = appicon/24x24/apps/poedit.png
appicons32_DATA = appicon/32x32/apps/poedit.png
appicons48_DATA = appicon/48x48/apps/poedit.png
appiconsscalable_DATA = appicon/scalable/apps/poedit.svg

mimeicons16_DATA = mime-gnome/16x16/mimetypes/poedit-translation-generic.png
mimeicons22_DATA = mime-gnome/22x22/mimetypes/poedit-translation-generic.png
mimeicons24_DATA = mime-gnome/24x24/mimetypes/poedit-translation-generic.png
mimeicons32_DATA = mime-gnome/32x32/mimetypes/poedit-translation-generic.png
mimeiconsscalable_DATA = mime-gnome/scalable/mimetypes/poedit-translation-generic.svg

pixmaps_DATA = appicon/48x48/apps/poedit.png


uiicons_DATA = \
		appicon/128x128/apps/poedit.png \
		ui/toolbar-24/document-open.png \
		ui/toolbar-24/document-save.png \
		ui/toolbar-24/document-properties.png \
		ui/toolbar-24/document-new.png \
		ui/toolbar-24/edit-delete.png \
		ui/toolbar-24/poedit-comment.png \
		ui/toolbar-24/poedit-fuzzy.png \
		ui/toolbar-24/poedit-update.png \
		ui/toolbar-24/poedit-validate.png \
		ui/poedit-status-automatic.png \
		ui/poedit-status-cat-mid.png \
		ui/poedit-status-cat-no.png \
		ui/poedit-status-cat-ok.png \
		ui/poedit-status-comment-modif.png \
		ui/poedit-status-comment.png \
		ui/poedit-status-modified.png \
		ui/poedit-status-nothing.png \
		ui/window-close.png


MIMETYPES = \
		text-x-gettext-translation \
		gnome-mime-text-x-gettext-translation


install-data-hook:
	for type in $(MIMETYPES) ; do \
		rm -f $(DESTDIR)$(iconsdir)$$size/mimetypes/*/$$type.*; \
		$(LN_S) -f poedit-translation-generic.png $(DESTDIR)$(mimeicons16dir)/$$type.png; \
		$(LN_S) -f poedit-translation-generic.png $(DESTDIR)$(mimeicons22dir)/$$type.png; \
		$(LN_S) -f poedit-translation-generic.png $(DESTDIR)$(mimeicons24dir)/$$type.png; \
		$(LN_S) -f poedit-translation-generic.png $(DESTDIR)$(mimeicons32dir)/$$type.png; \
		$(LN_S) -f poedit-translation-generic.svg $(DESTDIR)$(mimeiconsscalabledir)/$$type.svg; \
	done
