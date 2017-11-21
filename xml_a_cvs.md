## Creando los cvs

Una vez marcadas todas las imagenes se procede a crear los archivos cvs para el conjunto de __train__ y __test__. Se utilizo el codigo *xml_to_cvs.py* de [datitran's github](https://github.com/datitran/raccoon_dataset).

Al archivo xml_a_cvs.py se le cambio:
```python
def main():
    image_path = os.path.join(os.getcwd(), 'annotations')
    xml_df = xml_to_csv(image_path)
    xml_df.to_csv('raccoon_labels.csv', index=None)
    print('Successfully converted xml to csv.')
```

A esto:

```python
def main():
    for directory in ['train','test']:
        image_path = os.path.join(os.getcwd(), 'images/{}'.format(directory))
        xml_df = xml_to_csv(image_path)
        xml_df.to_csv('data/{}_labels.csv'.format(directory), index=None)
        print('Successfully converted xml to csv.')
```

Una vez que se corre el programa te deberia generar los archivos:
```
test_labels.csv
train_labels.csv
```
