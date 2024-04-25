import os

path = 'C:\\windows\\help'

for dirpath, dirnames, filenames in os.walk(path):    # обход каталога
    print('*' * 27)
    print(dirpath, dirnames, filenames)
    file_sise = os.path.getsize(path)             #размер файла
    print(file_sise)

    dir_name = os.path.dirname(path)             #директория файла
    print(dir_name)



    for file in filenames:
        full_name_path = os.path.join(dirpath, file)    # формирование полного пути к файлам
        print(full_name_path)
        print()
        full_name_path = dirpath + '\\' + file
        print(os.path.getmtime(full_name_path))       # отображение времени





