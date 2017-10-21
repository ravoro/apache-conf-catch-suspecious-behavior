# Apache Conf - Catch Suspecious Behavior

Apache server config for catching suspecious behavior.

Analyzes incoming request data (Request URI, User Agent, etc.) for pre-defined patterns of suspecious activity.

Requests deemed suspecious are stopped from being processed and a standard response is given (by default, a plain 404).

