The code (V1) is for: 
===========================================================================
W. Wang, J. Shen, L. Shao, and F. Porikli, 
[Correspondence driven saliency transfer](https://www.researchgate.net/publication/306435619_Correspondence_Driven_Saliency_Transfer) 
IEEE Trans. on Image Processing,25(11):5025- 5034, 2016       
===========================================================================

This is a re-implementation of the method proposed in above paper. 
Importantly, it was written for clarity of understanding, 
and is totally unoptimized.
For realistic timing and results to compare against, 
please refer to the material included in the original publication. 

The code is free to use for research purposes. 
If you use this software for research purposes,
you should cite above paper in any resulting publication.

The code has been tested on Window and Linux platforms with matlab.

The PR-curve, F-measure, and MAE on various datasets are stored in 'results.xlsx'.

The results on DUT, ECCSD, MSRA1000, MSRA5000 and PASCAL datasets are stored in 'rseults.rar'.

===========================================================================
How to run a simple demo:
===========================================================================
0a. if possible, compile '*.cpp' files in 'subCode'; 
1a. run 'createDataset.m' for establishing test/train dataset and pre-computing
GIST feature for all the images;
2a. run 'precomputeMatching.m' for precomputing batch-/pixel-level matching;
3a. run 'SaliencyTransfer.m'. 

===========================================================================
How to run our code on public datasets,  such as 'MSRA5000' or 'ECSSD', or use
your own dataset:
===========================================================================
1b. store the dataset as form of 'subDUT', containing two fields:'Annotations'
and 'Imgs';
2b. change the parameter 'database' in 'createDataset.m','precomputeMatching.m'
and 'SaliencyTransfer.m'  as the name of the new dataset;
3b. change the parameter 'setting.para.nTest' to set the number of test images
(usually set as 30% of the number of the images of the new dataset);
4b. then do 0a-3a.

===========================================================================
Note:
===========================================================================
We offer a tiny dataset 'subDUT', this is only used for demonstrating how
to run our demo. You need to download other datasets and perform 1b-4b, if 
you want to test our code on some public dataset.

===========================================================================
Contact Information
===========================================================================

Email:
    wenguanwang@bit.edu.cn
	shenjianbing@bit.edu.cn
------------------------------------------------------------------------------------------------
