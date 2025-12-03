require 'og_tasks'

spec = Gem::Specification.find_by_name 'og_tasks'
Dir.glob("#{spec.gem_dir}/lib/**/*.rake").each { |r| load r }
