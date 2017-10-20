# chef-custom-generator

Please note, my version of the custome Chef generator is far-far away from even BETA. 

1) Add the following configuration to the ~/.chef/config.rb file. Mind the path and $USER variable!

```
cookbook_path [ '~/chef-repo/cookbooks/']
if File.basename($PROGRAM_NAME).eql?('chef') && ARGV[0].eql?('generate')
  chefdk.generator.license = "all_rights"
  chefdk.generator.copyright_holder = "Your Name"
  chefdk.generator_cookbook = "/home/$USER/cookbooks/chef-custom-generator"
  chefdk.generator.email = "you@example.com"
  chefdk.generator_cookbook = "~/chef-repo/generator/chef-custom-generator"
end
```
