# Generative AI World Cup

## Getting Started

1. Install venv ``python -m venv venv`
2. Activate venv `source venv/bin/activate`
3. Install pip-tools `python -m pip install pip-tools`
4. Re-activate venv (to activate pip-tools path) `source venv/bin/activate`
5. Install dependencies `pip-sync requirements.txt dev-requirements.txt`

## Development

### Add dependency

1. To add new packages, add them on `requirements.in` or `dev_requirements.in`
2. Activate venv `source venv/bin/activate`
3. Compile requirements by running `pip-compile requirements.in` or `pip-compile dev-requirements.in`
4. Then install by running `pip-sync requirements.txt dev-requirements.txt` (run both files at the same time!)

### Update dependencies

1. Activate venv `source venv/bin/activate`
2. Update all dependencies by `pip-compile --upgrade requirements.in` or specific dependency by `pip-compile --upgrade-package transformers requirements.in`
3. Then install by running `pip-sync requirements.txt dev-requirements.txt`
