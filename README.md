# E-Commerce-Product-Management-API-Testing-and-BDD-Suite
import factory
from myapp.models import Product

class ProductFactory(factory.Factory):
    class Meta:
        model = Product

    name = factory.Faker('product_name')
    category = factory.Faker('word')
    price = factory.Faker('random_number', digits=2)
    available = factory.Faker('boolean')
