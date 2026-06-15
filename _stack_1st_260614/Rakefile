# -*- coding: utf-8 -*-
require "colorize"
require 'command_line/global'

task :default do
  system "rake -T"
end

desc "make md from org"
task :mk_md do # any name on task_name
  file_name = ARGV[1] || 'readme.org'
  head_name = File.basename(file_name, ".*")

  # your code goes
  comm = "pandoc #{head_name}.org -f org -t markdown-yaml_metadata_block-pandoc_title_block-raw_attribute -o #{head_name}.md"
  puts comm
  system comm
  exit
end
