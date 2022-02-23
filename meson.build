project(
  'dwm',
  'c',
  version: '6.3',
  license: [ 'MIT' ],
)

add_global_arguments('-DVERSION="1.0.0"', language: 'c')

cc = meson.get_compiler('c')

math = cc.find_library('m', required: false)
ft2 = dependency('freetype2')
xft = dependency('xft')
fontconfig = dependency('fontconfig')
webkit = dependency('webkit2gtk-4.0')

src = [
    'dwm.c',    
    'drw.c',
    'util.c'
]

executable('dwm',
    src,
    dependencies: [
        xft,
        math,
        ft2,
        fontconfig,
        webkit,
    ],
    install: true,
    install_dir: '/usr/bin'
)
