namespace :site do
  desc "Runs Jekyll server, and compiles/watch SASS files"
  task :run do
    sh "sass --watch _sass/style.scss:stylesheets/style.css & jekyll --auto --server"
  end
end