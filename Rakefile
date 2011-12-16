require 'rubygems'
require 'rake'

require 'jeweler'
Jeweler::Tasks.new do |gem|
  # gem is a Gem::Specification... see http://docs.rubygems.org/read/chapter/20 for more options
  gem.name = "ms-testdata"
  gem.homepage = "http://github.com/jtprince/ms-testdata"
  gem.license = "MIT"
  gem.summary = %Q{A repository of test data used by the mspire libraries}
  gem.description = %Q{The data used to test the mspire libraries is often large and unwieldly.  To better 
support multiple libraries, multiple developers, and the inevitable overlap of one
library test data with that of another, the mspire test data has been extracted
into this project.}
  gem.email = "jtprince@gmail.com"
  gem.authors = ["John T. Prince", "Simon Chiang"]
  gem.rubyforge_project = "mspire"
end
Jeweler::RubygemsDotOrgTasks.new

require 'rake/testtask'
Rake::TestTask.new(:spec) do |spec|
  spec.libs << 'lib' << 'spec'
  spec.pattern = 'spec/**/*_spec.rb'
  spec.verbose = true
end

require 'rcov/rcovtask'
Rcov::RcovTask.new do |spec|
  spec.libs << 'spec'
  spec.pattern = 'spec/**/*_spec.rb'
  spec.verbose = true
end

task :default => :spec

require 'rdoc/task'
Rake::RDocTask.new do |rdoc|
  version = File.exist?('VERSION') ? File.read('VERSION') : ""

  rdoc.rdoc_dir = 'rdoc'
  rdoc.title = "ms-testdata #{version}"
  rdoc.rdoc_files.include('README*')
  rdoc.rdoc_files.include('lib/**/*.rb')
end
