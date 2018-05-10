# Kill all the processes within a GPU
`kill -9 $(nvidia-smi -i ${GPUID} | sed -n 's/|\s*[0-9]*\s*\([0-9]*\)\s*.*/\1/p' | sort | uniq | sed '/^$/d')`
