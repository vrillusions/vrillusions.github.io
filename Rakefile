# this taken from https://github.com/davidensinger/davidensinger.github.io/blob/source/Rakefile
desc "Start dev server"
task :run_server do
  puts "Starting dev server"
  pids = [
    spawn("bundle exec jekyll server --watch")
  ]

  trap "INT" do
    Process.kill "INT", *pids
    exit 1
  end

  loop do
    sleep 1
  end
end
