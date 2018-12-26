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
inc = include_directories('include')
libcurl = dependency('libcurl')
lib = static_library('cpr', src, dependencies : libcurl, include_directories : inc)
dep = declare_dependency(include_directories : inc, link_with : lib)
