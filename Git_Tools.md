1) Найдите полный хеш и комментарий коммита, хеш которого начинается на aefea.  
```
git show aefea  
```
Хэш: aefead2207ef7e2aa5dc81a34aedf0cad4c32545  
Комментарий: Update CHANGELOG.md

2) Ответьте на вопросы.
- Какому тегу соответствует коммит 85024d3?  
```
git tag --contains 85024d3
v0.12.23
v0.12.24
v0.12.25
v0.12.26
v0.12.27
v0.12.28
v0.12.29
v0.12.30
v0.12.31
```
- Сколько родителей у коммита b8d720? Напишите их хеши.  
```
git show --pretty=raw b8d720 | grep parent
parent 56cd7859e05c36c06b56d013b55a252d0bb7e158
parent 9ea88f22fc6269854151c571162c5bcf958bee2b
```
- Перечислите хеши и комментарии всех коммитов, которые были сделаны между тегами v0.12.23 и v0.12.24.  
```
git log --oneline v0.12.23..v0.12.24
33ff1c03bb (tag: v0.12.24) v0.12.24
b14b74c493 [Website] vmc provider links
3f235065b9 Update CHANGELOG.md
6ae64e247b registry: Fix panic when server is unreachable
5c619ca1ba website: Remove links to the getting started guide's old location
06275647e2 Update CHANGELOG.md
d5f9411f51 command: Fix bug when using terraform login on Windows
4b6d06cc5d Update CHANGELOG.md
dd01a35078 Update CHANGELOG.md
225466bc3e Cleanup after v0.12.23 release
```
- Найдите коммит, в котором была создана функция func providerSource, её определение в коде выглядит так: func providerSource(...) (вместо троеточия перечислены аргументы).  
```
git log -S'func providerSource' -p
8c928e83589d90a031f811fae52a81be7153e82f
```
- Найдите все коммиты, в которых была изменена функция globalPluginDirs.  
```
git log -G'globalPluginDirs' -p
c0b17610965450a89598da491ce9b6b5cbd6393f
35a058fb3ddfae9cfee0b3893822c9a95b920f4c
22a2580e93170eac46621ab97decaec989d52edb
7c4aeac5f30aed09c5ef3198141b033eea9912be
```
- Кто автор функции synchronizedWriters?  
```
git log -G'func synchronizedWriters' -p
Martin Atkins
```
