# todo
improved taskwarrior

Console on web
speed of console, availability of web

based on taskwarrior - super simple, everything optional commands

examples:
  `add call @victor due:tomorrow`
  -create person "victor"
  -create duedate
  create task "call @victor"
  automatic urgency
  automatic scheduling
  
  `add check foozle proj:github +zone`
    creates new project
    adds tag
    
  `add fix computer blocks:all`
  =>created task n
    creates new task which is at top of priority list
    blocks everything (although later things may be visible! (or maybe not))
    how to create subtasks?
      `add subtask(N) get power restored`
      `add subtask(N) reinstall OS`
      `add subtask(N) buy new monitor (old one exploded)`
    
  everything optional

tech stack
  postgres
    events table
  C# dotnet core
  nginx
  "commands received"
  upon significant change, reprocess everything
  every event is a change entered by the user
    so we can replay everything once the processor changes
    
Development methodology
  dogfood everything
  opensource

UI
  appears as a custom shell
  no globbing
  good autocomplete (people, duedates, project names)
  coloration of commands as you type
  if you type proj: the whole term will colorize to indicate it's recognized
  converse is also true
  nice ctl+backspace delete whole word
  CRUD viewer (a-la djando admin)
    linking tags, projects, tasks, etc.
  continuously display a reasonable summary
  commandline-control what is displayed
  some configurability but most can come later - first make a reasonable mvp
  what to do about a mobile app version? so painful  
  
features:
  reasonable time interpolations/guesses
  "blocks:"
  
make it much easier to do self-hosting on a VPS
