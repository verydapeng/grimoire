List comprehension. Takes a vector of one or morebinding-form/collection-expr pairs, each followed by zero or moremodifiers, and yields a lazy sequence of evaluations of expr.Collections are iterated in a nested fashion, rightmost fastest,and nested coll-exprs can refer to bindings created in priorbinding-forms.  Supported modifiers are: :let [binding-form expr ...],:while test, :when test.(take 100 (for [x (range 100000000) y (range 1000000) :while (< y x)] [x y]))