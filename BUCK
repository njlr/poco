include_defs('//BUCKAROO_DEPS')

cxx_library(
  name = 'poco-json', 
  header_namespace = 'Poco/JSON',
  exported_headers = subdir_glob([
    ('JSON/include/Poco/JSON', '**/*.h'),
  ]),
  srcs = glob([
    'JSON/src/**/*.cpp',
  ]),
  compiler_flags = [
    '-std=c++14',
  ],
  visibility = [
    'PUBLIC',
  ],
  deps = BUCKAROO_DEPS,
)
