# Universal-Dependencies

For this assignment, I annotated 20 sentences in English and Swedish, and trained a dependency parser using MaChAmp on the Swedish Talbanken treebank.

The model was trained for 20 epochs on the MLTGPU server and the training took over 3 hours.  There was a steady improvement in score after every epoch, which shows the model was learning well from the Swedish training data.

The parser performed significantly well on Swedish (99 %) which could be because it was trained on Swedish data. The mistakes i noticed were differences in obj instead of iobj, tagging words like igår as NOUN instead of ADV.

The parser also performed well for English as well (92 %) taking the fact into consideration that English was never seen during training. Some errors I noticed were month names being tagged as NOUN instead of PROPN, and 's being tagged as PROPN or AUX instead of PART.Since Swedish and English have similar word order (both SVO languages), this could explain why the model transfers reasonably well across the two languages despite being trained only on Swedish.

