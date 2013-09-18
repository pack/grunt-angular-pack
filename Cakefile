{exec} = require 'child_process'

task 'build', 'Build project from src/*.coffee to tasks/*.js', ->
  exec 'coffee --compile --output tasks/ src/', (err, stdout, stderr) ->
    throw err if err
    if stdout or stderr
      console.log stdout + stderr

task 'watch', 'Starts a watcher for the src/*.coffee files', ->
  exec 'coffee -w src/ -o tasks/', (err, stdout, stderr) ->
    throw err if err
    if stdout or stderr
      console.log stdout + stderr
