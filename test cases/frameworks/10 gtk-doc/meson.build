project('gtkdoctest', 'c', version : '1.0.0')

gtkdoc = find_program('gtkdoc-scan', required: false)
if not gtkdoc.found()
  error('MESON_SKIP_TEST gtkdoc not found.')
endif

gnome = import('gnome')

assert(gnome.gtkdoc_html_dir('foobar') == 'share/gtk-doc/html/foobar', 'Gtkdoc install dir is incorrect.')

inc = include_directories('include')

subdir('include')

# We have to disable this test until this bug fix has landed to
# distros https://bugzilla.gnome.org/show_bug.cgi?id=753145
error('MESON_SKIP_TEST can not enable gtk-doc test until upstream fixes have landed.')

subdir('doc')
