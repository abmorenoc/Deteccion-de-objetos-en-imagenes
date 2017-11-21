## Generando los tfrecord

Ahora se utilizara el archivo *generate_tfrecord.py* de [datitran's github](https://github.com/datitran/raccoon_dataset).
El unico cambio que se la hara sera el siguiente:

```python
# TO-DO replace this with label map
def class_text_to_int(row_label):
    if row_label == 'budlight':
        return 1
    elif row_label == 'corona':
        return 2
    elif row_label == 'indio':
        return 3
    elif row_label == 'miller':
        return 4
    else:
        None
```

Se tiene que correr el programa dos veces para obtener *test.record* y *train.record* de la siguiente manera:

```
python generate_tfrecord.py --csv_input=data/train_labels.csv --output_path=data/train.record

python generate_tfrecord.py --csv_input=data/test_labels.csv --output_path=data/test.record
```
