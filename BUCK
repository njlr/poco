include_defs('//BUCKAROO_DEPS')

cxx_library(
  name = 'poco-mongodb', 
  header_namespace = 'Poco/MongoDB',
  exported_headers = subdir_glob([
    ('MongoDB/include/Poco/MongoDB', '**/*.h'),
  ]),
  srcs = glob([
    'MongoDB/src/**/*.cpp',
  ]),
  compiler_flags = [
    '-std=c++14',
  ],
  visibility = [
    'PUBLIC',
  ],
  deps = BUCKAROO_DEPS,
)
