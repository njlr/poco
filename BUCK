include_defs('//BUCKAROO_DEPS')

cxx_library(
  name = 'crypto', 
  header_namespace = 'Poco/Crypto',
  exported_headers = subdir_glob([
    ('Crypto/include/Poco/Crypto', '**/*.h'),
  ]),
  srcs = glob([
    'Crypto/src/**/*.cpp',
  ]),
  compiler_flags = [
    '-std=c++14',
  ],
  visibility = [
    'PUBLIC',
  ],
  deps = BUCKAROO_DEPS,
)
