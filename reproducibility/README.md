```bash
export PROJECT_NAME=xlanalysis5k

docker build -t ${PROJECT_NAME}_image -f reproducibility/dockerfile .


docker run --rm --ipc=host --gpus all -v ${PWD}:/workspace -it ${PROJECT_NAME}_image bash

# inside the container


# Download the dataset, instructions are included in the main readme file.

unzip 'Bible bitexts.zip'

python src/Data\ Generation/generate_features.py --path_to_matthew "Bible bitexts/book_of_matthew" --path_to_john "Bible bitexts/book_of_john" --download_dir ./results.csv --path_to_lang_df "Bible experimental vars/bible_all_features_LANGUAGE"
```

