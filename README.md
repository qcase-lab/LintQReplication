Install Conda, Docker
- Docker (tested with versions: 24.0.2, build cb74dfc and 20.10.23, build7155243).
- Conda (tested with versions: 24.3.0 and 22.9.0).
Run in powershell: conda env create -f virtualenv/conda/environment.yml
Activate virtual environment: conda activate LintQEnv
Build docker image: python automation_scripts/create_docker_image_locally.py
Run to verify installation: docker run -v "$(pwd)/data:/home/codeql/project/data" -it --rm lintq codeql pack ls /usr/local/codeql-home/
Verify output:
- Found mattepalte/qiskit@0.0.1
- Found mattepalte/qlint@0.0.1
- Found mattepalte/qlint-tests@0.0.0
