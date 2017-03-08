include_defs('//BUCKAROO_DEPS')

cxx_library(
  name = 'poco-cpp-unit', 
  header_namespace = 'CppUnit',
  exported_headers = subdir_glob([
    ('CppUnit/include/CppUnit', '**/*.h'),
  ]),
  srcs = glob([
    'CppUnit/src/**/*.cpp',
  ]),
  compiler_flags = [
    '-std=c++14',
  ],
  visibility = [
    'PUBLIC',
  ],
  deps = BUCKAROO_DEPS,
)
