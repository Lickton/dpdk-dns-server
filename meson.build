project(
    'dpdkns',
    'cpp',
    default_options: [
        'default_library=static', 
        'warning_level=3',
        'cpp_std=c++20'
    ],
)

incdir = include_directories('include')

source = files(
    'src/application.cc',
    'src/logger.cc',
    'src/main.cc',
    'src/message.cc',
    'src/query.cc',
    'src/resolver.cc',
    'src/response.cc',
    'src/server.cc',
)

dpdk_dep = dependency('libdpdk')

executable(
    'dpdkns',
    source,
    include_directories: incdir,
    dependencies: dpdk_dep,
)