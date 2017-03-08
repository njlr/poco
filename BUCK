include_defs('//BUCKAROO_DEPS')

windows_sources = glob([
  'Util/src/WinService.cpp.cpp',
  'Util/src/WinRegistryConfiguration.cpp',
])

cxx_library(
  name = 'poco-util', 
  header_namespace = 'Poco/Util',
  exported_headers = subdir_glob([
    ('Util/include/Poco/Util', '**/*.h'),
  ]),
  srcs = glob([
    'Util/src/**/*.cpp',
  ], excludes = windows_sources),
  platform_srcs = [
    ('^windows.*', windows_sources),
  ],
  compiler_flags = [
    '-std=c++14',
  ],
  visibility = [
    'PUBLIC',
  ],
  deps = BUCKAROO_DEPS,
)
