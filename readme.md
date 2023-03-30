# saving and working requirements for projects
each project should have pip_requirements.txt and conda_requirements.txt for us to work more efficiently here is how:<br />
using conda:<br />
save requirements.txt: conda list -e > conda_requirements.txt<br />
create conda env: conda create --name --file conda_requirements.txt<br />

using pip:<br />
save requirements: pip list --format=freeze > pip_requirements.txt<br />
install rquirements : pip install -r pip_requirements.txt<br />

Windows <br /><br />

FOR /F "delims=~" %f in (requirements.txt) DO conda install --yes "%f" || pip install "%f"<br />

Bash<br />

while read requirement; do conda install --yes $requirement; done < requirements.txt<br />
