# BadNetsDefense

This repository goes over Backdoor attacks on neural networks. Implemented here is a BadNet model pruning defense for a class work.

The notebooks directory contains all the notebooks used to generate the GoodNet models with X={2%,4%,10%}. The models directory contains all the model weights for X={2%,4%,10%} saved in the format: B_primeX={2,4,10}.h5.

In order to run the file for evaluation, I created an eval.py from the following [link](https://github.com/csaw-hackml/CSAW-HackML-2020). The difference between the file in the link and my repo is that in line 7, I changed the path for where my model weights are saved. All you need to do is change between 2,4 and 10. For instance if you want to use model with X=4, then you will change from the following:

```python

clean_data_filename = str(sys.argv[1])
model_filename = "/models/B_primeX=2.h5"

```

to:
```python

clean_data_filename = str(sys.argv[1])
model_filename = "/models/B_primeX=4.h5" #change made here

```
I am not changing the clean_data_filename path since I do not directly have access to the data. In my notebooks, I accessed the data from the google drive link that was shared.