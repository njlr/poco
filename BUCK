include_defs('//BUCKAROO_DEPS')

cxx_library(
  name = 'poco-xml', 
  header_namespace = 'Poco',
  exported_headers = subdir_glob([
    ('XML/include/Poco', '**/*.h'),
  ]),
  srcs = glob([
    'XML/src/**/*.cpp',
  ]),
  compiler_flags = [
    '-std=c++14',
  ],
  platform_compiler_flags = [
    ('default', ['-DHAVE_MEMMOVE']),
    ('^macos.*', ['-DHAVE_MEMMOVE']),
  ],
  visibility = [
    'PUBLIC',
  ],
  deps = BUCKAROO_DEPS,
)
