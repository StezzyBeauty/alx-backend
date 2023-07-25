# 0x01. Caching

<img src=https://camo.githubusercontent.com/127cd770bb9da936cc9f5416af65131fad494c73864a87254d8a64c1ec56366b/68747470733a2f2f64336c6b63336e357468303178372e636c6f756466726f6e742e6e65742f77702d636f6e74656e742f75706c6f6164732f323032322f30382f32363031343530302f496d706c656d656e742d63616368696e672d6c617965722d696e2d776562332d70726f64756374732e706e67>

## Learning Objectives
At the end of this project, you are expected to be able to explain to anyone, without the help of Google:

- What a caching system is
- What FIFO means
- What LIFO means
- What LRU means
- What MRU means
- What LFU means
- What the purpose of a caching system
- What limits a caching system have

## More Info

### Parent class BaseCaching
```
$ cat base_caching.py
#!/usr/bin/python3
""" BaseCaching module
"""

class BaseCaching():
    """ BaseCaching defines:
      - constants of your caching system
      - where your data are stored (in a dictionary)
    """
    MAX_ITEMS = 4

    def __init__(self):
        """ Initiliaze
        """
        self.cache_data = {}

    def print_cache(self):
        """ Print the cache
        """
        print("Current cache:")
        for key in sorted(self.cache_data.keys()):
            print("{}: {}".format(key, self.cache_data.get(key)))

    def put(self, key, item):
        """ Add an item in the cache
        """
        raise NotImplementedError("put must be implemented in your cache class")

    def get(self, key):
        """ Get an item by key
        """
        raise NotImplementedError("get must be implemented in your cache class")
```
