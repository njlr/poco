linux_sources = glob([
  'Foundation/src/SyslogChannel.cpp',
  'Foundation/src/**/*_POSIX.cpp',
  'Foundation/src/**/*_UNIX.cpp',
])

macos_sources = glob([
  'Foundation/src/SyslogChannel.cpp',
  'Foundation/src/**/*_POSIX.cpp',
])

windows_sources = glob([
  'Foundation/src/EventLogChannel.cpp',
  'Foundation/src/WindowsConsoleChannel.cpp',
  'Foundation/src/**/*_WIN32.cpp',
  'Foundation/src/**/*_WIN32U.cpp',
  'Foundation/src/**/*_WINCE.cpp',
  'Foundation/src/**/WindowsC*.cpp',
])

other_sources = glob([
  'Foundation/src/**/OpcomChannel.cpp',
  'Foundation/src/**/*_Android.cpp',
  'Foundation/src/**/*_VMS.cpp',
  'Foundation/src/**/*_VX.cpp',
  'Foundation/src/**/*_HPUX.cpp',
  'Foundation/src/**/*_DEC.cpp',
  'Foundation/src/**/*_SUN.cpp',
])

macos_compiler_flags = [
  '-D__TOS_MACOS__',
  '-DARCHFLAGS=-arch x86_64',
  '-DPOCO_TARGET_OSARCH=x86_64',
  '-DUSE_STATIC_LIBRARIES=0',
]

linux_linker_flags = [
  '-lpthread',
]

cxx_library(
  name = 'foundation',
  header_namespace = 'Poco',
  exported_headers = subdir_glob([
    ('Foundation/include/Poco', '**/*.h'),
  ]),
  srcs = glob([
    'Foundation/src/**/*.cpp',
  ],
  excludes = windows_sources + macos_sources + linux_sources + other_sources),
  platform_srcs = [
    ('default', macos_sources),
    ('^macos.*', macos_sources),
    ('^linux.*', linux_sources),
    ('^windows.*', windows_sources),
  ],
  compiler_flags = [
    '-std=c++11', 
  ],
  platform_compiler_flags = [
    ('default', macos_compiler_flags),
    ('^macos.*', macos_compiler_flags),
  ],
  exported_platform_linker_flags = [
    ('default', []),
    ('^linux.*', linux_linker_flags), 
  ],
  visibility = [
    'PUBLIC',
  ],
)
