# Name-BruteForcer

## How to
### Example
```python
>>> from name_bruteforcer import NameBruteForcer
>>> name_bruteforcer = NameBruteForcer()
>>> name_bruteforcer.run('Юрий')
{'Urij'}
>>> name_bruteforcer.custom_mapping = {
...     'Ю': ['Yu', 'Iy'],
...     'ю': ['yu', 'iy'],
...     'й': ['ii', 'iy', 'yy', 'yu'],
... }
>>> name_bruteforcer.run('Юрий')
{'Urij', 'Yuriyu', 'Iyrij', 'Uriyy', 'Yuriii', 'Iyriii', 'Iyriyy', 'Uriiy', 'Yuriyy', 'Iyriyu', 'Uriyu', 'Iyriiy', 'Yurij', 'Uriii', 'Yuriiy'}
>>> name_bruteforcer.run('Владимир Пехтин')
{'Vladimir Pehtin'}
>>> name_bruteforcer.custom_mapping['х'] = ['kh']
>>> name_bruteforcer.run('Владимир Пехтин')
{'Vladimir Pehtin', 'Vladimir Pekhtin'}
>>> name_bruteforcer.custom_mapping['В'] = ['W']
>>> name_bruteforcer.run('Владимир Пехтин')
{'Vladimir Pekhtin', 'Vladimir Pehtin', 'Wladimir Pekhtin', 'Wladimir Pehtin'}
```
