project('cristian', 'cpp',
        default_options: ['warning_level=3', 'cpp_std=c++17', 'werror=true'])

include_dir = include_directories(['include', get_option('asio_include_dir'), get_option('spdlog_include_dir'), get_option('cli11_include_dir')])
src = (['src/main.cpp'])
srcClient = (['src/client/main.cpp'])
srcServer = (['src/server/main.cpp'])
thread_dep = dependency('threads')

executable('cristian',
            sources: src, 
            include_directories: include_dir,
            dependencies: thread_dep)

executable('client',
            sources: srcClient, 
            include_directories: include_dir,
            dependencies: thread_dep)

executable('server',
            sources: srcServer, 
            include_directories: include_dir,
            dependencies: thread_dep)