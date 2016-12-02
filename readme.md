## Prepare
0. Make sure you have `python` environment, and `pip` command
1. Install all requirements by (you may need `sudo`)

        pip install -r requirements.txt

2. Fill up configuration file `support-files/config.json`

  - directory: the path to store all of your codeforces source code
  - api_problems: the codeforces api to retrieval all problem information
  - java: path of java template
  - py: path of python template
  - cpp: path of cpp template

## Use

Assume root folder is `tools/`
### Update problem set

- `support-files/update_problems.py`

    Retrieval codeforces problem set and store in tiny json db (`tinydb`).

### Solve a problem    

- Under root folder `./sol`

    Pick a unsolved problem. Script will create folder and download sample case. Be careful if sample cases has tricky string, like `<\br>`, I can't guarantee that the parser will work.
    
- Under the problem folder `./run {name}.cpp`

    Compile and run test case. The `run` script only support `cpp`.
    
- Under root folder `./finish {name}`

    Remove the folder `{name}` and move the source code to your source code folder.
    
GL & HF.