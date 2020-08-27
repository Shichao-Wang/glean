# Glean

This is the source code for paper [Dynamic Knowledge Graph based Multi-Event Forecasting](https://yue-ning.github.io/docs/KDD20-glean.pdf) appeared in KDD20 (research track)

[Songgaojun Deng](https://amy-deng.github.io/home/), [Huzefa Rangwala](https://cs.gmu.edu/~hrangwal/), [Yue Ning](https://yue-ning.github.io/)


## Data
We processed five country based datasets from the ICEWS data. Please find the datasets in this [Google Drive Link](https://drive.google.com/drive/folders/1qrF1e9I8pnVlCRjb-NPiidZCu5oA0NWL?usp=sharing). The dataset folder (e.g., `IND`) can be placed in the folder `data`. A brief introduction of the data file is as follows:
- `quadruple.txt` includes the structured event information ordered by time.
- `text.txt` event summary file, where each row corresponds to the event in `quadruple.txt`
- `stat.txt` includes the number of entities and event types.
- `entity2id.txt` entity string to index mapping
- `relation2id.txt` event type (i.e., relation) string to index mapping
- `quadruple_id.txt` events represented by the index.

## Prerequisites
The code has been successfully tested in the following environment.
- Python 3.7.7
- PyTorch 1.6.0
- dgl 0.5.0
- Sklearn 0.23.2
- Pandas 1.1.1

Example commands executed to build the environment (Note: we use Ubuntu with Cuda 9.2)
```sh
conda create --name glean python=3.7
conda install pytorch torchvision cudatoolkit=9.2 -c pytorch
pip install dgl-cu92
pip install tqdm
conda install scikit-learn
pip install pandas
```
