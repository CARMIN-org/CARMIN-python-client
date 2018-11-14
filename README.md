# CARMIN-python-client
Python module to communicate with a CARMIN platform though the CARMIN API
language.

All the methods/parameters are not fully supported, but the majority and all the useful one are.

This a synchronous implementation, using python 3+

## How to use it

The API URL to use must be referenced in the "\_\_PREFIX" variable in `vip.py`. This defaults to the [VIP](http://vip.creatis.insa-lyon.fr/) url. If it used HTTPS, the certificate should be set. The script will look for it at the `./certif.crt` location, but it cas also be given with the `setCertifPath(str)` function. The VIP certificate is present by default in the repository.

This module then works like a state-machine : first, set the apikey with
setApiKey(str). All the functions will refer to this apikey later.


You can now use all of the functions :)

## Raised errors

If there's any VIP issues, functions will raise *RuntimeError* errors. See
'detect\_errors' and 'manage\_errors' functions if you want to change this.

## Future possible improvements

- an asynchronous version
- support few missing optional parameters in some functions
