# SocialNews dataset for Aspect-based Sentiment Classification of Long Documents

This dataset consists of news articles related to social issues derived from the [PerSenT dataset (Bastan et al., 2020)](https://github.com/StonyBrookNLP/PerSenT/tree/main). We identify six implicit aspects, namely crime-justice, digital-online, economic issues, health, human rights, and work. Three independent annotators are asked to assess the sentiment towards these aspects and we use the majority vote as the ground truth sentiment. The Kappa inter-annotator agreement is 93.14%.

## Data Fields
- `id`: document id  
- `mode`: this dataset has 3 splits: train, dev, and test  
- `text`: a string containing the text of the article  
- `paragraphs`: a list of strings containing paragraphs of the article  
- `sentences`: a list of strings containing sentences of the article  
- `entity`: The entity that the author is expressing opinion about  
- `Aspect{crime_justice_system,...,work_occupation}`: label for each aspect in the article  

**Note**: Labels are one of  
- {aspect} is not in the article (-1)  
- {aspect} is in the article and aspect sentiment is mixed positive negative (3)  
- {aspect} is in the article and aspect sentiment is positive (2)  
- {aspect} is in the article and aspect sentiment is neutral (1)  
- {aspect} is in the article and aspect sentiment is negative (0)  

## Dataset Statistics
| Dataset | Justice+| Justice-| Online+| Online-| Economic+| Economic-| Health+| Health-|Rights+|Rights-|Work+|Work-|
|---------|--------------|--------------|-------------|-------------|---------------|---------------|-------------|-------------|-------------|------------|-----------|-----------|
| Train   | 83           | 530          | 353         | 134         | 200           | 40            | 94          | 68          | 127         | 97         | 968       | 137       |
| Dev     | 10           | 83           | 56          | 17          | 30            | 9             | 12          | 15          | 21          | 40         | 152       | 29        |
| Test    | 12           | 97           | 48          | 29          | 37            | 11            | 16          | 14          | 31          | 38         | 137       | 24        |

<sub>+: positive, -: negative</sub>

## Citation

If you find this work useful, please cite as following:

```
@inproceedings{
  
}
```

If we submit the paper to a conference or journal, we will update the BibTeX.
