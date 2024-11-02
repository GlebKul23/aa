<img width="894" alt="Снимок экрана 2024-11-02 в 11 17 39" src="https://github.com/user-attachments/assets/c82b0ffc-75cb-4230-b6b4-223cba1bdc9e">
cut -d: -f1 passwd.txt | sort

cut - это утилита, которая используется для извлечения определенных полей

-d - это параметр, показывающий разделитель

-f1 - это параметр, показывающий, какой столбец будет считан

| - это оператор, указывающий на то, куда будут переданы данные из cut

sort - утилита, сортирующая данные
<img width="1160" alt="Снимок экрана 2024-11-02 в 11 15 23" src="https://github.com/user-attachments/assets/985e7de3-6682-4145-8f7e-52fc577e908f">
<img width="758" alt="Снимок экрана 2024-11-02 в 11 16 57" src="https://github.com/user-attachments/assets/5d0a67fa-c2f4-4a6e-9663-fa998dc015e9">

Файл:

<img width="234" alt="Снимок экрана 2024-11-02 в 11 18 16" src="https://github.com/user-attachments/assets/31df0c03-460d-4a7d-bc7e-449defa1e951">

<img width="937" alt="Снимок экрана 2024-11-02 в 11 21 53" src="https://github.com/user-attachments/assets/4a3457c0-6fcf-4543-a640-7e93e26fb02f">

cat /etc/protocols | tail +8| sort | head -5

head - утилита, считывающая первые 10 строк в базавой настройке

tail - утилита обратная по смыслу head

tail +8 нужно чтобы исключить строки с объяснениями

<img width="565" alt="Снимок экрана 2024-11-02 в 11 24 01" src="https://github.com/user-attachments/assets/08be35c7-41d2-476c-bccc-9f0e3134e1f3">
<img width="898" alt="Снимок экрана 2024-11-02 в 11 23 34" src="https://github.com/user-attachments/assets/d8348467-39a8-48fa-8fb8-b65d5b1f7042">

Файл:
<img width="940" alt="Снимок экрана 2024-11-02 в 11 25 10" src="https://github.com/user-attachments/assets/e45b72f9-2054-421b-9841-0f3c2d800e7e">

<img width="934" alt="Снимок экрана 2024-11-02 в 11 27 56" src="https://github.com/user-attachments/assets/256c4dae-287b-41ca-828f-a0f4742a338b">

```C
#include <stdio.h>
#include <stdlib.h>
#include <string.h>
#include <readline/readline.h>

int main()
{
	char *a = readline("Введите текст: ");
	for (int i = 0; i < strlen(a) + 2; i++)
	{
		if (i == 0 || i == strlen(a) + 1)
			printf("+");
		else
			printf("-");
	}
	printf("\n");
	printf("|%s|\n", a);
	for (int i = 0; i < strlen(a) + 2; i++)
	{
		if (i == 0 || i == strlen(a) + 1)
			printf("+");
		else
			printf("-");
	}
	printf("\n");
	free(a);
	return 0;
}
```
<img width="442" alt="Снимок экрана 2024-11-02 в 11 31 39" src="https://github.com/user-attachments/assets/f23190fe-05af-4d10-b113-103a5d8a2adf">
<img width="679" alt="Снимок экрана 2024-11-02 в 11 32 07" src="https://github.com/user-attachments/assets/2b400ba7-423a-4057-81bf-b517032d6641">

<img width="919" alt="Снимок экрана 2024-11-02 в 11 33 42" src="https://github.com/user-attachments/assets/d4b52003-979b-4a31-bcf6-24f001e512e3">


```C
#!/bin/bash

file="$1"

id=$(grep -o -E '\b[a-zA-Z]*\b' "$file" | sort -u)
```
<img width="790" alt="Снимок экрана 2024-11-02 в 11 36 18" src="https://github.com/user-attachments/assets/8c6ac93a-017a-42a9-b210-a86b33d92eac">

<img width="902" alt="Снимок экрана 2024-11-02 в 11 37 00" src="https://github.com/user-attachments/assets/e8eee4a2-6079-46d7-a6e1-aa5ac18b99b0">

<img width="923" alt="Снимок экрана 2024-11-02 в 11 38 37" src="https://github.com/user-attachments/assets/59653ab8-09d0-4520-bea4-16631747e477">

```C
#!/bin/bash

file=$1

chmod 755 "./$file"

sudo cp "$file" /usr/local/bin/
```
<img width="275" alt="Снимок экрана 2024-11-02 в 11 40 02" src="https://github.com/user-attachments/assets/a49dec40-aaf7-44c3-8394-f987c82c4bc1">


<img width="473" alt="Снимок экрана 2024-11-02 в 11 40 24" src="https://github.com/user-attachments/assets/39fa8473-5aff-4a43-8bd0-30caab320a39">

<img width="875" alt="Снимок экрана 2024-11-02 в 11 42 07" src="https://github.com/user-attachments/assets/336a7412-f1c0-4cfc-9974-bd4973688b57">

```C
#include <fstream>
using namespace std;
int main() {
    ifstream in("banner.c");
    string line;
    getline(in, line);
    if (line[0] == '/') {
        if (line[1] == '/' || line[1] == '*')
            printf("Success\n");
        else {
            printf("Not success\n");
        }
    }
    else {
        printf("Not success\n");
    }
}
```
<img width="266" alt="Снимок экрана 2024-11-02 в 11 43 06" src="https://github.com/user-attachments/assets/5b5ed2d3-1b54-4820-8863-a21027dddba6">
<img width="491" alt="Снимок экрана 2024-11-02 в 11 43 30" src="https://github.com/user-attachments/assets/3a85fd0d-aa77-44e0-a527-829e324c40cc">

<img width="916" alt="Снимок экрана 2024-11-02 в 11 44 20" src="https://github.com/user-attachments/assets/58d54499-3cb0-4306-a2fa-5bfae14ac3fd">

```C
#include <iostream>
#include <filesystem>
#include <unordered_map>
#include <vector>
#include <fstream>
using namespace std;
namespace fs = filesystem;

string compute_hash(const fs::path& filePath) {
    ifstream file(filePath, ios::binary);
    string hash(istreambuf_iterator<char>(file), {});
    return hash;
}

int main(int argc, char* argv[]) {
    if (argc != 2) {
        cerr << "Использование: " << argv[0] << " <путь>" << endl;
        return 1;
    }

    fs::path dirPath(argv[1]);
    if (!fs::exists(dirPath) || !fs::is_directory(dirPath)) {
        cerr << "Указанный путь не является директорией." << endl;
        return 1;
    }
    unordered_map<string, vector<fs::path>> fileHashes;
    for (const auto& entry : fs::recursive_directory_iterator(dirPath)) {
        if (fs::is_regular_file(entry)) {
            string fileHash = compute_hash(entry);
            fileHashes[fileHash].push_back(entry);
        }
    }
    for (const auto& [hash, paths] : fileHashes) {
        if (paths.size() > 1) {
            cout << "Найдены дубликаты файлов с хэшем: " << hash << endl;
            for (const auto& path : paths) {
                cout << "    " << path << endl;
            }
            cout << endl;
        }
    }

    return 0;
}
```

Вывод:

//В файлах in и out перед запуском программы содержимое сделали одинаковым

<img width="467" alt="Снимок экрана 2024-11-02 в 11 45 29" src="https://github.com/user-attachments/assets/f30976d9-7090-4fb9-bfb0-d3d05feac79f">
<img width="692" alt="Снимок экрана 2024-11-02 в 11 45 49" src="https://github.com/user-attachments/assets/acc3f283-137e-40a6-9855-dd0d32daede7">

<img width="936" alt="Снимок экрана 2024-11-02 в 11 46 36" src="https://github.com/user-attachments/assets/1b052366-46d7-4a2a-a17f-b62604075c61">

```C
#!/bin/bash

files=( $(find . -type f -name "*.$1") )

tar -cvf "archive.tar" "${files[@]}"

echo "Архив создан"
```

Пример ввода и вывода:

<img width="243" alt="Снимок экрана 2024-11-02 в 11 48 01" src="https://github.com/user-attachments/assets/266f928e-ba80-4f31-8e5f-d5f8e8c841ea">
<img width="457" alt="Снимок экрана 2024-11-02 в 11 48 17" src="https://github.com/user-attachments/assets/1c380bf7-56ee-49d4-91af-c26551bd45d3">

Пример архива:

<img width="763" alt="Снимок экрана 2024-11-02 в 11 48 45" src="https://github.com/user-attachments/assets/a8be0ef6-27c9-4964-8010-1e2baa7bb5cb">

<img width="929" alt="Снимок экрана 2024-11-02 в 11 49 52" src="https://github.com/user-attachments/assets/b836922d-620b-465f-9fd2-8a3e45ba862d">

```C
#include <fstream>
#include <iostream>
using namespace std;
int main() {
    ifstream in("in.txt");
    ofstream out("out.txt");
    string line;
    string line2;
    while (getline(in, line))
    {
        int count = 0;
        line2 = "";
        for (int i = 0; i < size(line); i++) {
            if (count == 4) {
                line2 += '\t';
                count = 0;
            }
            if (line[i] == ' ') {
                count++;
            }
            else {
                if (count == 0)
                    line2 += line[i];
                else
                {
                    for (int j = 0; j < count; j++)
                        line2 += ' ';
                }
                count = 0;
            }
        }
        out << line2 << "\n";
    }
}
```

Запуск:

<img width="256" alt="Снимок экрана 2024-11-02 в 11 50 53" src="https://github.com/user-attachments/assets/e0f4bfac-c9c5-4654-90d9-5478309eddd2">


in.txt:

<img width="178" alt="Снимок экрана 2024-11-02 в 11 51 27" src="https://github.com/user-attachments/assets/7643f200-c799-4834-a7ec-34a998a59201">

out.txt:

<img width="206" alt="Снимок экрана 2024-11-02 в 11 51 10" src="https://github.com/user-attachments/assets/21cf02cd-5130-4b9d-99f7-b9ea54373603">

<img width="920" alt="Снимок экрана 2024-11-02 в 11 52 57" src="https://github.com/user-attachments/assets/d5a22c64-46be-4190-b1bc-6c72d6bd4d21">

```C
#!/bin/bash

for file in "$1"/*; do
    if [[ -f "$file" && ! -s "$file" ]]; then
        echo "Пустой файл: $file"
    fi
done
```

Ввод и вывод:

<img width="366" alt="Снимок экрана 2024-11-02 в 11 53 56" src="https://github.com/user-attachments/assets/5fb8a1bf-f7eb-431b-ae2f-9c75e0281acb">
<img width="581" alt="Снимок экрана 2024-11-02 в 11 54 19" src="https://github.com/user-attachments/assets/4d2608d3-ae52-46d9-9615-9ac6ff18e5d8">

