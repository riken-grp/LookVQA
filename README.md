# Gaze-grounded VQA Dataset
This repository includes the Gaze-grounded Visual Question Answering dataset (GazeVQA) introduced by the following paper: Shun Inadumi, Seiya Kawano, Akishige Yuguchi, Yasutomo Kawanishi, Koichiro Yoshino. "A Gaze-grounded Visual Question Answering Dataset for Clarifying Ambiguous Japanese Questions". In Proc. of LREC-COLING 2024.

## License
[Creative Commons Attribution 4.0 License](https://creativecommons.org/licenses/by/4.0/legalcode)

## Dataset Format
GazeVQA provides annotated 17,276 question/answer pairs for the [Gazefollow](https://gazefollow.csail.mit.edu/index.html) and [COCO](https://cocodataset.org/) Dataset.

## QA format
```
[
    {
        "image_id": identification of the COCO image,
        "qa_id": identification of the QA sample,
        "question": question,
        "answer": answer (Note that test-set QAs have ten answers),
        "c_question": clarified question (Only test-set have)
    }, ...
]
```

## QA Attributes format
```
Copyright (c) 2015, COCO Consortium.
{
    "qa_id":{
        "gf_path": identification of the Gazefollow image and gaze annotation,
        "bboxes": bounding box annotation of gaze targets from COCO
        [
            [x1, y1, w, h], # obj1
            [x1, y1, w, h], # obj2
            ...
        ],
        "objects": object label annotation of gaze targets from COCO
        [obj1, obj2, ...]
    }, ...
}
```

# Citation
You can cite it as follows:
```
@inproceedings{inadumi-etal-2024-gaze,
  author    = "Shun Inadumi and
               Seiya Kawano and
               Akishige Yuguchi and
               Yasutomo Kawanishi and
               Koichiro Yoshino",
  title     = "A Gaze-grounded Visual Question Answering Dataset for Clarifying Ambiguous Japanese Questions",
  booktitle = "Proceedings of the 2024 Joint International Conference on Computational Linguistics, Language Resources and Evaluation",
  year      = "2024"
}
```


If you have any questions about the paper and repository, feel free to contact Shun Inadumi (inazumi.shun.in6[at]naist.ac.jp) or open an issue.
