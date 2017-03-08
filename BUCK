include_defs('//BUCKAROO_DEPS')

cxx_library(
  name = 'poco-data', 
  header_namespace = 'Poco/Data',
  exported_headers = subdir_glob([
    ('Data/include/Poco/Data', '**/*.h'),
  ]),
  srcs = glob([
    'Data/src/**/*.cpp',
  ]),
  compiler_flags = [
    '-std=c++14',
  ],
  visibility = [
    'PUBLIC',
  ],
  deps = BUCKAROO_DEPS,
)
