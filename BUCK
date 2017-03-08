include_defs('//BUCKAROO_DEPS')

cxx_library(
  name = 'poco-net', 
  header_namespace = 'Poco/Net',
  exported_headers = subdir_glob([
    ('Net/include/Poco/Net', '**/*.h'),
  ]),
  srcs = glob([
    'Net/src/**/*.cpp',
  ]),
  compiler_flags = [
    '-std=c++14',
  ],
  visibility = [
    'PUBLIC',
  ],
  deps = BUCKAROO_DEPS,
)
