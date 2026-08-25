import unittest


class TestExample(unittest.TestCase):
    """示例测试类"""

    def setUp(self):
        """测试前的准备工作"""
        self.value = 10

    def tearDown(self):
        """测试后的清理工作"""
        pass

    def test_addition(self):
        """测试加法"""
        result = self.value + 5
        self.assertEqual(result, 15)

    def test_subtraction(self):
        """测试减法"""
        result = self.value - 3
        self.assertEqual(result, 7)

    def test_multiplication(self):
        """测试乘法"""
        result = self.value * 2
        self.assertEqual(result, 20)

    def test_division(self):
        """测试除法"""
        result = self.value / 2
        self.assertEqual(result, 5.0)

    def test_positive_number(self):
        """测试正数判断"""
        self.assertGreater(self.value, 0)

    def test_type(self):
        """测试类型判断"""
        self.assertIsInstance(self.value, int)


if __name__ == "__main__":
    unittest.main()
