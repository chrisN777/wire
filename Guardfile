
guard :rspec do
  watch(%r{^spec/.+_spec\.rb$}) { "spec" }
  watch(%r{^lib/(.+)\.rb$})     { |m| "spec/lib/#{m[1]}_spec.rb" }
  watch('spec/spec_helper.rb')  { "spec" }

end

guard :rubocop, all_on_start: false, cli: ['--config', '.rubocop.yml']  do
  #watch(%r{.+\.rb$})
  watch(%r{^lib/(.+)\.rb$}) 
  watch(%r{(?:.+/)?\.rubocop\.yml$}) { |m| File.dirname(m[0]) }
end
