open terminal window
# Install Software
$sudo npm install -g <#software#>
# check <#software veresion#> 
$run #software#> -v
# Open workspace
$cd capterra/feed-products
# Parse file contents
#sed -s capterra.yaml
# convert YAML to JSON- Install Ruby and add to .bashrc code:
alias yaml2json="ruby -capterra.yaml -rjson -e 'puts JSON.pretty_generate(YAML.load(ARGF))'"
# install jq to parse json file
$ sudo apt-get install jq
# Parse json file
$cat capterra.json | jq ‘.github’
$cat softwareadvice.json| jq
# Create Test cases  while reading file
Case1: File Not Found
Case2: File is empty
# Execute  TestCases
