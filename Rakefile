begin
  require 'bones'
  Bones.setup
rescue LoadError
  begin
    load 'tasks/setup.rb'
  rescue LoadError
    raise RuntimeError, '### please install the "bones" gem ###'
  end
end

ensure_in_path 'lib'
require 'rackamole'

task :default => 'spec:run'

PROJ.name            = 'rackamole'
PROJ.authors         = 'Fernand Galiana'
PROJ.email           = 'fernand.galiana@gmail.com'
PROJ.url             = 'http://www.rackamole.com'
PROJ.version         = Rackamole::VERSION
PROJ.spec.opts       << '--color'
PROJ.ruby_opts       = %w[-W0]
PROJ.readme          = 'README.rdoc'
PROJ.rcov.opts       = ["--sort", "coverage", "-T", '-x mongo']

# Dependencies
depend_on "logging"      , ">= 1.2.2"
depend_on "hitimes"      , ">= 1.0.3"
depend_on "mongo"        , ">= 1.0.1"
depend_on "bson"         , ">= 1.0.1"
depend_on "bson_ext"     , ">= 1.0.1"
depend_on "chronic"      , ">= 0.2.3"
depend_on "twitter4r"    , ">= 0.3.0"
depend_on "erubis"       , ">= 2.6.0"
depend_on "mail"         , ">= 2.1.3"
depend_on "ruby-growl"   , ">= 2.0"
