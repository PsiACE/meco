project('meco', 'c',
  version : '0.1.0',
  meson_version: '>= 0.50.0',
  default_options : ['warning_level=3'])


config_h = configuration_data()
config_h.set_quoted('PACKAGE_VERSION', meson.project_version())
configure_file(
  output: 'meco-config.h',
  configuration: config_h,
)
add_project_arguments([
  '-I' + meson.build_root(),
], language: 'c')

subdir('include')
subdir('src')

run_target(
  'format',
  command: ['scripts/format.sh']
)

run_target(
  'release',
  command: ['scripts/release.sh', meson.project_name(), meson.project_version()]
)

run_target(
  'run',
  command: ['scripts/run.sh']
)