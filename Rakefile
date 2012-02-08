require 'metaforce'
require 'metaforce/dsl'
include Metaforce::DSL::Metadata

Savon.log = false
HTTPI.log = false

# Get SFDC credentials for :deploy and :retrieve
task :credentials do
  print "username: "
  @username = STDIN.gets.chomp
  print "password: "
  @password = STDIN.gets.chomp
  print "security token: "
  @security_token = STDIN.gets.chomp
end


desc "Deploy 'codepkg' to the target organization"
task :deploy => :credentials do
  login :username => @username, :password => @password, :security_token => @security_token do
    puts "Deploying 'codepkg' to the organization..."
    deploy File.dirname(__FILE__) do
      puts "'codepkg' deployed successfully"
    end
  end
end

desc "Retrieve files from the target organization"
task :retrieve => :credentials do
  login :username => @username, :password => @password, :security_token => @security_token do
    puts "Retrieving content from the organization..."
    retrieve File.expand_path("../codepkg/package.xml", __FILE__), :to => "retrieved" do
      puts "Retrieve successfull. Code unziped to 'retrieved'"
    end
  end
end
