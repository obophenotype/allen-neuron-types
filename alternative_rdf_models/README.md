# Aim:

Convert ttl files to a model more compliant with patterns in CL using Robot templates (Conventient for now - may switch to DOSDP).

# Strategy:

Use ipython notebook to mung ttl files into tsv files to be consumed by Robot.


### TTL to JSON:

```
robot convert --input fu.ttl -f json --output fu.json
```

### Building with ROBOT templates - example:

```sh
robot -p "HGNC: https://cbiit.cancer.gov/#HGNC_" template  --input /repos/obo-relations/ro.owl  --template robot_pattern_test.tsv --output robot_pattern_test.owl
```

Note - using ro.owl as an input allows use of quoted names to refer to object properties.  I have not succeeded in getting curies for OPs to work.

### Processing with Jupyter notebook

See [Allen\_neuron_hack.py] & notes within.



