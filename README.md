# Name-BruteForcer

## How to
### Example
```python
>>> from name_bruteforcer import NameBruteForcer
>>> name_bruteforcer = NameBruteForcer()
>>> name_bruteforcer.brute_force_name('Юрий')
{'Urij'}
>>> name_bruteforcer.custom_mapping = {
...     'Ю': ['Yu', 'Iy'],
...     'ю': ['yu', 'iy'],
...     'й': ['ii', 'iy', 'yy', 'yu'],
... }
>>> name_bruteforcer.brute_force_name('Юрий')
{'Urij', 'Yuriyu', 'Iyrij', 'Uriyy', 'Yuriii', 'Iyriii', 'Iyriyy', 'Uriiy', 'Yuriyy', 'Iyriyu', 'Uriyu', 'Iyriiy', 'Yurij', 'Uriii', 'Yuriiy'}
>>> name_bruteforcer.brute_force_fullname('Владимир Пехтин')
{'Vladimir Pehtin'}
>>> name_bruteforcer.custom_mapping['х'] = ['kh']
>>> name_bruteforcer.brute_force_fullname('Владимир Пехтин')
{'Vladimir Pehtin', 'Vladimir Pekhtin'}
```
