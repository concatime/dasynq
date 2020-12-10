project('dasynq', 'cpp',
  default_options: [
    'b_ndebug=if-release',
    'buildtype=debugoptimized',
    'c_std=c++11',
    'warning_level=3',
  # 'werror=true',
  ],
  license: 'Apache-2.0',
  version: '1.1.7-development',
)

dasynq_ver = meson.project_version().split('-')[0]

dasynq_inc = [include_directories('include')]

dasynq_dep = declare_dependency(
  include_directories: dasynq_inc,
  version: dasynq_ver,
)

if meson.is_subproject()
    subdir_done()
endif

install_subdir('include',
  install_dir: 'include',
  strip_directory: true,
)

subdir('examples')

pkg = import('pkgconfig')
pkg.generate(
  description: 'Thread-safe cross-platform event loop library in C++',
  name: meson.project_name(),
  version: dasynq_ver,
)
