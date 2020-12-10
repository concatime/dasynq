executable('chatserver', 'chatserver/chatserver.cc',
  dependencies: [dasynq_dep],
)

thread_dep = dependency('threads')
executable('chatserver_mt', 'chatserver/chatserver_mt.cc',
  dependencies: [dasynq_dep, thread_dep],
)
