project('CPR', 'cpp')
src = ['cpr/auth.cpp',
'cpr/cookies.cpp',
'cpr/cprtypes.cpp',
'cpr/digest.cpp',
'cpr/error.cpp',
'cpr/multipart.cpp',
'cpr/parameters.cpp',
'cpr/payload.cpp',
'cpr/proxies.cpp',
'cpr/session.cpp',
'cpr/ssl_options.cpp',
'cpr/timeout.cpp',
'cpr/util.cpp']
inc = [include_directories('include')]
if meson.is_cross_build() and target_machine.cpu_family() == 'arm'
    inc += include_directories(meson.get_cross_property('root') + '/usr/include/arm-linux-gnueabihf')
endif

libcurl = dependency('libcurl')
lib = static_library('cpr', src, dependencies : libcurl, include_directories : inc)
cpr_dep = declare_dependency(include_directories : inc, link_with : lib)
