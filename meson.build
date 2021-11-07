project('unity', 'c',
  version: '2.5.4',
  license: 'MIT',
  meson_version: '>=0.60.0',
)

incdir = include_directories('.')
lib = static_library(meson.project_name(),
  'unity.c',
  c_args: ['-DUNITY_OUTPUT_COLOR'],
  implicit_include_directories: false,
)
unity_dep = declare_dependency(link_with: lib, include_directories: incdir)
meson.override_dependency('unity', unity_dep)
