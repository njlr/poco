include_defs('//BUCKAROO_DEPS')

cxx_library(
  name = 'cpp-parser', 
  header_namespace = 'Poco/CppParser',
  exported_headers = subdir_glob([
    ('CppParser/include/Poco/CppParser', '**/*.h'),
  ]),
  srcs = glob([
    'CppParser/src/**/*.cpp',
  ]),
  compiler_flags = [
    '-std=c++14',
  ],
  visibility = [
    'PUBLIC',
  ],
  deps = BUCKAROO_DEPS,
)
