namespace :greeting do

desc 'outputs hello to the terminal'
  task :hello do
    puts "hello from Rake!"
  end

  desc "outputs hola to terminal in spanish"
  task :hola do
    puts "hola de Rake!"
  end
end

namespace :db do

  desc "invokes the :environment and migrates database"
  task :migrate => :environment do
    Student.create_table
  end

  desc "fills the table with dummy data"
  task :seed do
    require_relative "./db/seeds.rb"
  end

  desc "environment to connect files, top level"
  task :environment do
    require_relative "./config/environment"
  end

end
