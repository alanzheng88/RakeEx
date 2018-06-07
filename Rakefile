require 'rake'

task default: :build_all

task rebuild: ["clean:remove_binaries", :build_all]
task build_essentials_only: ["build:dep1", "build:dep2"]
task build_all: "build:all"
task package: [:build_all, "pack:all"]
task install: "install:all"
task deploy: [:package, :install]

namespace "clean" do
  desc "Remove binaries"
  task :remove_binaries do
    puts "Removing binaries"
  end
end

namespace "build" do
  task all: [:dep1, :dep2, :dep3]

  desc "Build dependency 1"
  task :dep1 do
    puts "Finish building dependency 1"
  end

  desc "Build dependency 2"
  task :dep2 do
    puts "Finish building dependency 2"
  end

  desc "Build dependency 3"
  task :dep3 do
    puts "Finish building dependency 3"
  end
end

namespace "pack" do
  task all: :create

  desc "Create package"
  task :create do
    puts "Finish creating package"
  end
end

namespace "install" do
  task all: :run

  desc "Install package"
  task :run do
    puts "Finish installing package"
  end
end
