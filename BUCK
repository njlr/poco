include_defs('//BUCKAROO_DEPS')

cxx_library(
  name = 'poco-zip', 
  header_namespace = 'Poco/Zip',
  exported_headers = subdir_glob([
    ('Zip/include/Poco/Zip', '**/*.h'),
  ]),
  srcs = glob([
    'Zip/src/**/*.cpp',
  ]),
  compiler_flags = [
    '-std=c++14',
  ],
  visibility = [
    'PUBLIC',
  ],
  deps = BUCKAROO_DEPS,
)
