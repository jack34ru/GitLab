# Домашнее задание к занятию «GitLab» - Кузнецов Евгений Александрович

### Задание 1

**Что нужно сделать:**

1. Разверните GitLab локально, используя Vagrantfile и инструкцию, описанные в [этом репозитории](https://github.com/netology-code/sdvps-materials/tree/main/gitlab).   
2. Создайте новый проект и пустой репозиторий в нём.
3. Зарегистрируйте gitlab-runner для этого проекта и запустите его в режиме Docker. Раннер можно регистрировать и запускать на той же виртуальной машине, на которой запущен GitLab.

В качестве ответа в репозиторий шаблона с решением добавьте скриншоты с настройками раннера в проекте.

### Решение 1

Скриншот 1 к решению 1
![Screen 1](https://github.com/jack34ru/GitLab/blob/master/screens/Screenshot_99.png)
Скриншот 2 к решению 1
![Screen 2](https://github.com/jack34ru/GitLab/blob/master/screens/Screenshot_100.png)
Скриншот 3 к решению 1
![Screen 3](https://github.com/jack34ru/GitLab/blob/master/screens/Screenshot_101.png)
Скриншот 4 к решению 1
![Screen 4](https://github.com/jack34ru/GitLab/blob/master/screens/Screenshot_102.png)

### Задание 2

**Что нужно сделать:**

1. Запушьте [репозиторий](https://github.com/netology-code/sdvps-materials/tree/main/gitlab) на GitLab, изменив origin. Это изучалось на занятии по Git.
2. Создайте .gitlab-ci.yml, описав в нём все необходимые, на ваш взгляд, этапы.

В качестве ответа в шаблон с решением добавьте: 
   
 * файл gitlab-ci.yml для своего проекта или вставьте код в соответствующее поле в шаблоне; 
 * скриншоты с успешно собранными сборками.

 ### Решение 2

 Листинг кода файла gitlab-ci.yml к решению 2:
```
stages:
  - test
  - build

job_1_test:
  stage: test
  image: golang:1.17
  script: 
   - go test .
  tags:
    - hwgitlab

job_2_build:
  stage: build
  image: docker:latest
  script:
   - docker build .
  tags:
    - hwgitlab

```

Скриншот 1 к решению 2
![Screen 5](https://github.com/jack34ru/GitLab/blob/master/screens/Screenshot_103.png)
Скриншот 2 к решению 2
![Screen 6](https://github.com/jack34ru/GitLab/blob/master/screens/Screenshot_104.png)
Скриншот 3 к решению 2
![Screen 7](https://github.com/jack34ru/GitLab/blob/master/screens/Screenshot_105.png)
Скриншот 4 к решению 2
![Screen 4](https://github.com/jack34ru/GitLab/blob/master/screens/Screenshot_106.png)