# h4l_agent_test

This is a tutorial on using agentic workflows to do high eneryg physics anaylsis on CMS open data.
This tutorial is designed for the USCMS meeting
step0: install Claude or Codex. Here are the Claude instructions

```
curl -fsSL https://claude.ai/install.sh | bash
```

You will have to pay for Claude if you don't have it. Claude Pro ($20/month) is sufficient. 

Also you will need Pixi
```
curl -fsSL https://pixi.sh/install.sh | sh
```

step1: download the data
```
curl -L -o https://www.dropbox.com/scl/fi/tj2j72ub3smel2wg8arei/data.tgz?rlkey=rx0ol2uvz36dhegqcgyi4cvzc&dl=1
tar xzvf data.tgz
```

step2: setup the environment, 
```
git clone git@github.com:violatingcp/h4l_agent_test.git
git clone git@github.com:violatingcp/jfc.git -b jfc_lite
cd jfc
pixi run scaffold analyses/h4l_analysis --type measurement
cd analyses/my_analysis
pixi install
```

step3: setup the prompts and configure Claude
```
cp -r ../../../data .
cp -r ../../../h4l_agent_test/h4l_ntuplize.py
cp -r ../../../h4l_agent_test/docs .
cp -r ../../../h4l_agent_test/.claude .
cp    ../../../h4l_agent_test/prompt.md .
~~~

step4: And we are off
```
cat prompt.md | claude
~~~

step4 (alt): And we are off
```
cat prompt.md | codex
~~~

