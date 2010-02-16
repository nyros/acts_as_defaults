class << ActiveRecord::Base

  def default_find_option(option_name, value)
    @default_find_options ||= {} 
    @default_find_options[option_name] = value
  end
 
alias_method :orig_find, :find
  def find(args)
     options = args
    @default_find_options ||= {}
    orig_find(options,@default_find_options)
  end
end
