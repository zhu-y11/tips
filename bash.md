# Kill all the processes within a GPU
`kill -9 $(nvidia-smi -i ${GPUID} | sed -n 's/|\s*[0-9]*\s*\([0-9]*\)\s*.*/\1/p' | sort | uniq | sed '/^$/d')`

# Use B as a proxy to between A and C 
In A, do
`scp -oProxyCommand="ssh -W %h:%p B" thefile C:destination`
