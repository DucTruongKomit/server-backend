This module was written to  allow you to call code with some `uid` while being sure no security checks (`ir.model.access` and `ir.rule`) are done. In this way, it's the same as `sudo()`, but the crucial difference is that the code still runs with the original user id. This can be important for inherited code that calls workflow functions, subscribes the current user to some object, etc.

Usually, you'll be in in the situation to want something like this if you inherit from a module you can't or don't want to change, and call `super()`.
