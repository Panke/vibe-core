project('vibe-core', 'd')

srcs = [
'./source/vibe/internal/hashmap.d',
'./source/vibe/internal/traits.d',
'./source/vibe/internal/allocator.d',
'./source/vibe/internal/array.d',
'./source/vibe/internal/async.d',
'./source/vibe/internal/list.d',
'./source/vibe/internal/interfaceproxy.d',
'./source/vibe/internal/typetuple.d',
'./source/vibe/internal/freelistref.d',
'./source/vibe/internal/string.d',
'./source/vibe/appmain.d',
'./source/vibe/core/args.d',
'./source/vibe/core/process.d',
'./source/vibe/core/internal/release.d',
'./source/vibe/core/file.d',
'./source/vibe/core/stream.d',
'./source/vibe/core/concurrency.d',
'./source/vibe/core/log.d',
'./source/vibe/core/parallelism.d',
'./source/vibe/core/path.d',
'./source/vibe/core/connectionpool.d',
'./source/vibe/core/core.d',
'./source/vibe/core/task.d',
'./source/vibe/core/net.d',
'./source/vibe/core/channel.d',
'./source/vibe/core/taskpool.d',
'./source/vibe/core/sync.d'
]

eventcore_dep = dependency('eventcore')
allocator_dep = dependency('stdx-allocator', fallback: ['stdx-allocator', 'allocator_dep'])

vibe_core_dep = declare_dependency(
    compile_args: '-i',
    include_directories: 'source',
    version: '1.9.4',
    dependencies: [eventcore_dep, allocator_dep]
)

echo_server = executable(
    'echo-server',
    'examples/echo-server/source/app.d',
    dependencies: [eventcore_dep, vibe_core_dep, allocator_dep]
)