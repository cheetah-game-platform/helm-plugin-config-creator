## Утилита для создания ConfigurationMap

Принимает два аргумента - путь до каталога с конфигурацией и путь до каталога для сохранения созданных ConfigurationMap.

Каталог для конфигурации имеет следующию структуру:

```
service-1
    room // если в каталоге сервиса есть каталоги 
         // - то для каждого каталога первого уровня будет создана ConfigMap с binaryData от tgz архивом каталога
        some-directory
             config-3.yaml
        config-1.yaml
        config-2.yaml
service-2
    config-1.yaml // для каждого файла в каталоге сервиса на первом уровне будет создана ConfigMap с текстовым 
                  // содержанием файла
    config-2.yaml
service-3
```
