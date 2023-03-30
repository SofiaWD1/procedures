# saving and working requirements for projects
each project should have pip_requirements.txt and conda_requirements.txt for us to work more efficiently here is how:<br />
using conda:<br />
save requirements.txt: conda list -e > conda_requirements.txt<br />
create conda env: conda create --name --file conda_requirements.txt<br />

using pip:<br />
save requirements: pip list --format=freeze > pip_requirements.txt<br />
install rquirements : pip install -r pip_requirements.txt<br />


## To install from  conda_requirements to conda env 
create conda env using : conda create --name <env name> <br />
install pip for conda using : conda install pip <br />
Windows <br />

FOR /F "delims=~" %f in (conda_requirements.txt) DO conda install --yes "%f" || conda install -c conda_forge --yes "%f"<br />

Bash<br />

while read requirement; do conda install --yes $requirement; done < conda_requirements.txt<br /> <br />
### create env yml:<br />
conda env export --name my-env --from-history --file environment.yml <br />
create conda env using yml: conda env create --file environment.yml <br />
 for more info: <br />
 https://carpentries-incubator.github.io/introduction-to-conda-for-data-scientists/04-sharing-environments/index.html
