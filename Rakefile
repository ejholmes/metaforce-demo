require 'metaforce'
require 'metaforce/dsl'
include Metaforce::DSL::Metadata

Savon.log = false
HTTPI.log = false

desc "Deploy 'codepkg' to the target organization"
task :deploy do
  login :username => ENV["SFDC_USERNAME"], :password => ENV["SFDC_PASSWORD"], :security_token => ENV["SFDC_SECURITY_TOKEN"] do
    puts "Deploying 'codepkg' to the organization..."
    deploy File.dirname(__FILE__) do |result|
      puts "'codepkg' deployed successfully"
    end
  end
end

desc "Retrieve files from the target organization"
task :retrieve do
  login :username => ENV["SFDC_USERNAME"], :password => ENV["SFDC_PASSWORD"], :security_token => ENV["SFDC_SECURITY_TOKEN"] do
    puts "Retrieving content from the organization..."
    retrieve File.expand_path("../codepkg/package.xml", __FILE__), :to => "retrieved" do |result|
      puts "Retrieve successfull. Code unziped to 'retrieved'"
    end
  end
end
