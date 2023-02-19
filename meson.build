project(
    'ugetopt',
    ['c'],
    version: '2.38.99',
    default_options: ['c_std=gnu99', 'warning_level=3'],
    license: 'GPL-2.0-or-later',
)

cc = meson.get_compiler('c')

# warning: ISO C does not support %n$ operand number formats
if cc.has_argument('-Wpedantic')
    add_project_arguments('-Wno-pedantic', language: 'c')
endif

add_project_arguments(
    '-DPACKAGE_VERSION="' + meson.project_version() + '"', language: 'c'
)

executable(
    'ugetopt', ['getopt.c'],
    install: true,
)

install_man('getopt.1')
