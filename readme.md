# saving and working requirements for projects
using conda: 
save requirements.txt: conda list -e > requirements.txt 
create conda env: conda create --name --file requirements.txt

using pip:
save requirements: pip list --format=freeze > requirements.txt+ 
install rquirements : pip install -r requirements
