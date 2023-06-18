<!--- START SELFDOC --->
## SelfDoc
_Auto-generated code documentation to make the repository easier to navigate and contribute to._

_Last Updated: 2023-06-18_

The `example_selector` directory is for selecting examples to include in prompts. It contains implementation files for three classes: `LengthBasedExampleSelector`, `SemanticSimilarityExampleSelector`, and `MaxMarginalRelevanceExampleSelector`. It also includes an abstract base class `BaseExampleSelector` and implementation files for `NGramOverlapExampleSelector` and `SemanticSimilarityExampleSelector` classes. These classes use different algorithms to select and order examples based on length, ngram overlap score, and semantic similarity.

### Files
#### __init__.py
This file exports three classes for selecting examples to include in prompts: `LengthBasedExampleSelector`, `SemanticSimilarityExampleSelector`, and `MaxMarginalRelevanceExampleSelector`. These classes are imported from the `length_based.py` and `semantic_similarity.py` files and can be accessed through this module.

#### base.py
This file defines an abstract base class `BaseExampleSelector` which serves as an interface for selecting examples to include in prompts. It contains two abstract methods: `add_example` which adds a new example to the store for a key, and `select_examples` which selects which examples to use based on the inputs.

#### length_based.py
This file contains the implementation of a class named `LengthBasedExampleSelector` which selects examples based on their length. It uses a prompt template to format the examples and measures the length of the examples using a function that counts the number of words in the text. Additionally, it contains a function `select_examples` that selects examples based on the length of the input.

#### ngram_overlap.py
This file contains the implementation of NGramOverlapExampleSelector class, which selects and orders examples based on their ngram overlap score. It includes a function to compute the ngram overlap score of a source and example as a sentence_bleu score, and a class that inherits from BaseExampleSelector and BaseModel. The class has a list of examples, a prompt template, and a threshold at which the algorithm stops. The selected examples are sorted in descending order of their ngram overlap score and exclude any examples with a score less than or equal to the threshold.

#### semantic_similarity.py
This file contains the implementation of an example selector that selects examples based on Semantic Similarity. It defines a class `SemanticSimilarityExampleSelector` that uses a `VectorStore` to store information about examples and has methods to add new examples to the `VectorStore` and select examples based on their similarity to a given input. Additionally, it contains a subclass `MaxMarginalRelevanceExampleSelector` that selects examples based on semantic similarity using Max Marginal Relevance algorithm and returns a list of selected examples.

<!--- END SELFDOC --->