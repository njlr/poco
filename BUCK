include_defs('//BUCKAROO_DEPS')

cxx_library(
  name = 'netssl-openssl',
  header_namespace = 'Poco/Net',
  exported_headers = subdir_glob([
    ('NetSSL_OpenSSL/include/Poco/Net', '**/*.h'),
  ]),
  srcs = glob([
    'NetSSL_OpenSSL/src/**/*.cpp',
  ]),
  compiler_flags = [
    '-std=c++14',
  ],
  visibility = [
    'PUBLIC',
  ],
  deps = BUCKAROO_DEPS,
)
