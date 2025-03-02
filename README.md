## Домашнее задание

**Студента группы ИУ8-<21>**
**<Гацан Лев>**


1. Скачайте библиотеку *boost* с помощью утилиты **wget**. Адрес для скачивания `https://sourceforge.net/projects/boost/files/boost/1.69.0/boost_1_69_0.tar.gz`.
```sh
(Скачал последнюю версию)
$ wget https://sourceforge.net/projects/boost/files/boost/1.87.0/boost_1_87_0.tar.gz

--2025-03-02 20:07:31--  https://sourceforge.net/projects/boost/files/boost/1.87.0/boost_1_87_0.tar.gz
Resolving sourceforge.net (sourceforge.net)... 104.18.12.149
Connecting to sourceforge.net (sourceforge.net)|104.18.12.149|:443... connected.
WARNING: cannot verify sourceforge.net's certificate, issued by ‘CN=Kaspersky Anti-Virus Personal Root Certificate,O=AO Kaspersky Lab’:
  Self-signed certificate encountered.
HTTP request sent, awaiting response... 301 Moved Permanently
Location: https://sourceforge.net/projects/boost/files/boost/1.87.0/boost_1_87_0.tar.gz/ [following]
--2025-03-02 20:07:32--  https://sourceforge.net/projects/boost/files/boost/1.87.0/boost_1_87_0.tar.gz/
Reusing existing connection to sourceforge.net:443.
HTTP request sent, awaiting response... 301 Moved Permanently
Location: https://sourceforge.net/projects/boost/files/boost/1.87.0/boost_1_87_0.tar.gz/download [following]
--2025-03-02 20:07:32--  https://sourceforge.net/projects/boost/files/boost/1.87.0/boost_1_87_0.tar.gz/download
Reusing existing connection to sourceforge.net:443.
HTTP request sent, awaiting response... 302 Found
Location: https://downloads.sourceforge.net/project/boost/boost/1.87.0/boost_1_87_0.tar.gz?ts=gAAAAABnxJBWa1XskfH0aS4e0JuLrxCyjSKK_W0f2PHGt2ZWVQ2jG_vBXOZUTtmEfFhefdWwYlgFNyP9K0j_xHvHx2I-knIR7A%3D%3D&use_mirror=deac-riga&r= [following]
--2025-03-02 20:07:33--  https://downloads.sourceforge.net/project/boost/boost/1.87.0/boost_1_87_0.tar.gz?ts=gAAAAABnxJBWa1XskfH0aS4e0JuLrxCyjSKK_W0f2PHGt2ZWVQ2jG_vBXOZUTtmEfFhefdWwYlgFNyP9K0j_xHvHx2I-knIR7A%3D%3D&use_mirror=deac-riga&r=
Resolving downloads.sourceforge.net (downloads.sourceforge.net)... 104.18.13.149, 104.18.12.149, 2606:4700::6812:c95, ...
Connecting to downloads.sourceforge.net (downloads.sourceforge.net)|104.18.13.149|:443... connected.
WARNING: cannot verify downloads.sourceforge.net's certificate, issued by ‘CN=Kaspersky Anti-Virus Personal Root Certificate,O=AO Kaspersky Lab’:
  Self-signed certificate encountered.
HTTP request sent, awaiting response... 302 Found
Location: https://deac-riga.dl.sourceforge.net/project/boost/boost/1.87.0/boost_1_87_0.tar.gz?viasf=1 [following]
--2025-03-02 20:07:33--  https://deac-riga.dl.sourceforge.net/project/boost/boost/1.87.0/boost_1_87_0.tar.gz?viasf=1
Resolving deac-riga.dl.sourceforge.net (deac-riga.dl.sourceforge.net)... 89.111.52.100
Connecting to deac-riga.dl.sourceforge.net (deac-riga.dl.sourceforge.net)|89.111.52.100|:443... connected.
WARNING: cannot verify deac-riga.dl.sourceforge.net's certificate, issued by ‘CN=Kaspersky Anti-Virus Personal Root Certificate,O=AO Kaspersky Lab’:
  Self-signed certificate encountered.
HTTP request sent, awaiting response... 200 OK
Length: 154912292 (148M) [application/x-gzip]
Saving to: ‘boost_1_87_0.tar.gz’

boost_1_87_0.tar.gz           100%[=================================================>] 147.74M   579KB/s    in 5m 36s

2025-03-02 20:13:14 (450 KB/s) - ‘boost_1_87_0.tar.gz’ saved [154912292/154912292]
```
2. Разархивируйте скаченный файл в директорию `~/boost_1_69_0`
```sh
$ tar -xf boost_1_87_0.tar.gz -C ~/ 
```
3. Подсчитайте количество файлов в директории `~/boost_1_69_0` **не включая** вложенные директории.
```sh
$ find ~/boost_1_87_0 -maxdepth 1 -type f | wc -l

13
```
4. Подсчитайте количество файлов в директории `~/boost_1_69_0` **включая** вложенные директории.
```sh
$ find ~/boost_1_87_0 -type f | wc -l

79424
```
5. Подсчитайте количество заголовочных файлов, файлов с расширением `.cpp`, сколько остальных файлов (не заголовочных и не `.cpp`).
```sh
- Заголовочные файлы (.h; .hpp)
$ find ~/boost_1_87_0 -type f \( -name "*.h" -o -name "*.hpp" \) | wc -l

17856

- Файлы с расширением `.cpp`
$ find ~/boost_1_87_0 -type f -name "*.cpp" | wc -l

18233

- Остальные файлы
$ find ~/boost_1_87_0 -type f ! -name "*.h" ! -name "*.hpp" ! -name "*.cpp" | wc -l

43335
```
6. Найдите полный пусть до файла `any.hpp` внутри библиотеки *boost*.
```sh
$ find ~/boost_1_87_0 -name "any.hpp"

/root/boost_1_87_0/boost/any.hpp
/root/boost_1_87_0/boost/fusion/algorithm/query/any.hpp
/root/boost_1_87_0/boost/fusion/algorithm/query/detail/any.hpp
/root/boost_1_87_0/boost/fusion/include/any.hpp
/root/boost_1_87_0/boost/geometry/geometries/adapted/detail/any.hpp
/root/boost_1_87_0/boost/hana/any.hpp
/root/boost_1_87_0/boost/hana/fwd/any.hpp
/root/boost_1_87_0/boost/proto/detail/any.hpp
/root/boost_1_87_0/boost/spirit/home/support/algorithm/any.hpp
/root/boost_1_87_0/boost/type_erasure/any.hpp
/root/boost_1_87_0/boost/xpressive/detail/utility/any.hpp
```
7. Выведите в консоль все файлы, где упоминается последовательность `boost::asio`.
```sh
$ grep -rnw ~/boost_1_87_0 -e 'boost::asio'

<[вывод команды в файле 7.txt](https://github.com/PraWek/TPlab01/blob/main/7.txt)>
```
8. Скомпилирутйе *boost*. Можно воспользоваться [инструкцией](https://www.boost.org/doc/libs/1_61_0/more/getting_started/unix-variants.html#or-build-custom-binaries) или [ссылкой](https://codeyarns.com/2017/01/24/how-to-build-boost-on-linux/).
```sh
$ cd ~/boost_1_69_0
$ ./bootstrap.sh
$ ./b2

<[вывод команды в файле 8.txt](https://github.com/PraWek/TPlab01/blob/main/8.txt)>
```
9. Перенесите все скомпилированные на предыдущем шаге статические библиотеки в директорию `~/boost-libs`.
```sh
$ mkdir ~/boost-libs
$ cp lib/*.a ~/boost-libs
$ ls ~/boost-libs

libboost_atomic.a
libboost_charconv.a
libboost_chrono.a
libboost_container.a
libboost_context.a
libboost_contract.a
libboost_coroutine.a
libboost_date_time.a
libboost_exception.a
libboost_fiber.a
libboost_filesystem.a
libboost_graph.a
libboost_iostreams.a
libboost_json.a
libboost_locale.a
libboost_log.a
libboost_log_setup.a
libboost_math_c99.a
libboost_math_c99f.a
libboost_math_c99l.a
libboost_math_tr1.a
libboost_math_tr1f.a
libboost_math_tr1l.a
libboost_nowide.a
libboost_prg_exec_monitor.a
libboost_process.a
libboost_program_options.a
libboost_random.a
libboost_regex.a
libboost_serialization.a
libboost_stacktrace_addr2line.a
libboost_stacktrace_basic.a
libboost_stacktrace_from_exception.a
libboost_stacktrace_noop.a
libboost_system.a
libboost_test_exec_monitor.a
libboost_thread.a
libboost_timer.a
libboost_type_erasure.a
libboost_unit_test_framework.a
libboost_url.a
libboost_wave.a
libboost_wserialization.a
```
10. Подсчитайте сколько занимает дискового пространства каждый файл в этой директории.
```sh
$ du -ah ~/boost-libs

16K	/root/boost-libs/libboost_atomic.a
244K	/root/boost-libs/libboost_charconv.a
148K	/root/boost-libs/libboost_chrono.a
164K	/root/boost-libs/libboost_container.a
12K	/root/boost-libs/libboost_context.a
256K	/root/boost-libs/libboost_contract.a
32K	/root/boost-libs/libboost_coroutine.a
4.0K	/root/boost-libs/libboost_date_time.a
4.0K	/root/boost-libs/libboost_exception.a
244K	/root/boost-libs/libboost_fiber.a
416K	/root/boost-libs/libboost_filesystem.a
932K	/root/boost-libs/libboost_graph.a
124K	/root/boost-libs/libboost_iostreams.a
756K	/root/boost-libs/libboost_json.a
1.7M	/root/boost-libs/libboost_locale.a
2.9M	/root/boost-libs/libboost_log.a
2.7M	/root/boost-libs/libboost_log_setup.a
120K	/root/boost-libs/libboost_math_c99.a
120K	/root/boost-libs/libboost_math_c99f.a
120K	/root/boost-libs/libboost_math_c99l.a
964K	/root/boost-libs/libboost_math_tr1.a
1000K	/root/boost-libs/libboost_math_tr1f.a
928K	/root/boost-libs/libboost_math_tr1l.a
24K	/root/boost-libs/libboost_nowide.a
160K	/root/boost-libs/libboost_prg_exec_monitor.a
480K	/root/boost-libs/libboost_process.a
1.1M	/root/boost-libs/libboost_program_options.a
52K	/root/boost-libs/libboost_random.a
732K	/root/boost-libs/libboost_regex.a
1.2M	/root/boost-libs/libboost_serialization.a
48K	/root/boost-libs/libboost_stacktrace_addr2line.a
16K	/root/boost-libs/libboost_stacktrace_basic.a
8.0K	/root/boost-libs/libboost_stacktrace_from_exception.a
4.0K	/root/boost-libs/libboost_stacktrace_noop.a
4.0K	/root/boost-libs/libboost_system.a
2.2M	/root/boost-libs/libboost_test_exec_monitor.a
284K	/root/boost-libs/libboost_thread.a
24K	/root/boost-libs/libboost_timer.a
116K	/root/boost-libs/libboost_type_erasure.a
2.1M	/root/boost-libs/libboost_unit_test_framework.a
2.3M	/root/boost-libs/libboost_url.a
4.5M	/root/boost-libs/libboost_wave.a
780K	/root/boost-libs/libboost_wserialization.a
30M	/root/boost-libs/
```
11. Найдите *топ10* самых "тяжёлых".
```sh
$ du -ah ~/boost-libs/ | sort -rh | head -n 11

30M	/root/boost-libs/
4.5M	/root/boost-libs/libboost_wave.a
2.9M	/root/boost-libs/libboost_log.a
2.7M	/root/boost-libs/libboost_log_setup.a
2.3M	/root/boost-libs/libboost_url.a
2.2M	/root/boost-libs/libboost_test_exec_monitor.a
2.1M	/root/boost-libs/libboost_unit_test_framework.a
1.7M	/root/boost-libs/libboost_locale.a
1.2M	/root/boost-libs/libboost_serialization.a
1.1M	/root/boost-libs/libboost_program_options.a
1000K	/root/boost-libs/libboost_math_tr1f.a
```
