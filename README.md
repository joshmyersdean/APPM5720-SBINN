# Tutorial for APPM 5720: Data Driven Modeling
Authors: Josh Myers-Dean, Leonardo Orozco, and Wenhao Wang

This code supplements [Systems biology informed deep learning for inferring parameters and hidden dynamics](https://journals.plos.org/ploscompbiol/article/file?id=10.1371/journal.pcbi.1007575&type=printable) by Yazdani et al. and is adapted from [this code](https://github.com/alirezayazdani1/SBINNs).

### SBINN for Cell Apoptosis
- Open up `sbinn.ipynb` and click on the `Open in Colab` button in order to gain access to a GPU.
- Enable GPU runtime in colab
- Run all code as is to ensure it works correctly.

The authors train their model for 1.5 million epochs, this is not feasible to train during a tutorial. Instead we will only train for 5000 epochs (~4.5 minutes) or 10,000 epochs (~9 minutes). Regardless of the number of epochs, the results will not be that great due to the discrepency in amount of epochs. So for this tutorial we will go in with the mindset that the results will not be great, but instead study how the width and depth of the neural network affect the results.

You will find two comments in the larger code block. 
1. Change the number of layers and/or the number of neurons per layer and see how that affects the results. We can observe how good our solution is by the plot (that will be saved) at the end of the notebook. Compare your plots with eachother to see if you notice a difference in solution quality.
2. If time allows, try changing the number of epochs to see if there is a considerable difference in your solution. We recommend increasing the number of epochs by a minimum of 1000.

While your experiments are running, check out the next section of this tutorial.

### SINDy for Cell Apoptosis

For this part of the tutorial we can examine how well SINDy can perform compared to the neural network based approach. The biggest benefit of SINDy is that we do not have to wait almost a day for it to train. So while the neural network in part 1 of this tutorial is training, let's play around with SINDy parameters and see how well we can do!

Instructions
1. Connect to a non-GPU runtime
2. Run the first cell
3. Restart colab runtime 
4. Run cells 2 through last for default params, do not run cell 1 again
5. Try changing the sparsity threshold (`thrs`)
6. Try changing the polynomial degree order or experiment with other basis functions
7. Vary the amount of noise present in the training data
