include_defs('//BUCKAROO_DEPS')

cxx_library(
  name = '7zip',
  header_namespace = '',
  exported_headers = subdir_glob([
    ('SevenZip/src', '**/*.h'),
  ]),
  srcs = glob([
    'SevenZip/src/**/*.c',
  ]),
  compiler_flags = [
    '-D_7ZIP_ST',
  ],
)

cxx_library(
  name = 'seven-zip',
  header_namespace = 'Poco/SevenZip',
  exported_headers = subdir_glob([
    ('SevenZip/include/Poco/SevenZip', '**/*.h'),
  ]),
  srcs = glob([
    'SevenZip/src/**/*.cpp',
  ]),
  compiler_flags = [
    '-std=c++14',
  ],
  visibility = [
    'PUBLIC',
  ],
  deps = BUCKAROO_DEPS + [
    ':7zip',
  ],
)
