namespace :greeting do
  desc "outputs hello to terminal"
  task :hello do
    puts "hello from Rake!"
  end

  desc "outputs hola to terminal"
  task :hola do
    puts "hola de Rake!"
  end
end

namespace :db do
  desc "migrates changes to your database"
  task migrate: :environment do 
    Student.create_table
  end
  desc "seed the database with some dummy data"
  task seed: :environment do
    require_relative "./db/seeds"
  end
  
end

task :environment do
  require_relative "./config/environment"
end

desc "drop into pry console"
task console: :environment do
  Pry.start
end