
desc "Run the default task"
task :default => [:clean, :build]

desc "Cleanup all the generated junk"
task :clean do
  sh "JEKYLL_ENV='production' bundle exec jekyll clean"
end

desc "Build the site in production mode"
task :build do
  sh "JEKYLL_ENV='production' bundle exec jekyll build"
end

desc "Show the current theme and location on disk"
task :show_theme do
  sh "THEME=`cat _config.yml | grep theme`; bundle show `echo ${THEME##*:}`"
end

desc "Publish the site to S3"
task :publish do
  sh "s3_website push"
end


