This is assignment2 part2, written by Yu-Yang, Lee.

This package enable users to encode and decode range and complex datatype.

To install, type "python3 -m pip install jsonapi" in your terminal.

Below are some example of how to use jsonapi
'''python
class TestExtendedJSONApi(unittest.TestCase):
def test_complex_encoding_decoding(self):
complex_number = complex(2, 6)
encoded = jsonapi.dumps(complex_number)
decoded = jsonapi.loads(encoded)
self.assertEqual(decoded, complex_number)

    def test_range_encoding_decoding(self):
        r = range(0, 10, 1)
        encoded = jsonapi.dumps(r)
        decoded = jsonapi.loads(encoded)
        self.assertEqual(list(decoded), list(r))

'''
