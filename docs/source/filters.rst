Creating a New Filter =====================

After you have pulled the git repository (), creating a new filter in
`pycinema` and making it available in `Cinema:Theater` involves two steps. 

1. create a new, uniquely named file in the `pycinema/filters` directory and
   edit it to create your filter operation. 

2. include the new filter in the application by adding an import statement to
   the `pycinema/filters/__init__.py` file 
   
3. re-building and installing the `pycinema` module (typically with `pip
   install .`)

The new file must include this minimal class definition code, which defines the
inputs and outputs through a simple python dictionary, and defines an `_update`
method that is called by the framework. An example for a file called
`MyNewFilter.py` would look something like this::

    from pycinema import Filter

    class MyNewFilter(Filter):

        def __init__(self):
            super().__init__(
                inputs={
                    'someAttribute': 'value', 
                    'images': []
                },
                outputs={
                    'images': []
                }
            )

        def _update(self):
            results = []

            print(self.inputs.someAttribute.get())
            for image in self.inputs.images.get():
                # some operation on each image
                # do something here

                # copy data to output (for example)
                outImage = image.copy()
                outImage.channels['rgba'] = # some data here 
                results.append(outImage)

            self.outputs.images.set(results)

            return 1;


