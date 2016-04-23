task :get_up do
  puts 'getting up'
end

task :default => :get_up

task :clean_teeth => :get_up do
  puts 'going to bathroom'
end

task :choose_clothes_color, [:color] => :clean_teeth do |task, args|
  puts "#{args[:color]} color chosen"
end

task :run_positive do
  sh 'cucumber -t @positive'
end

task :run_all do
  sh 'cucumber -t @positive,@negative -f junit -o reports/ -f html -o reports/report.html'
end