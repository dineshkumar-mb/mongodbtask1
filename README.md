# Day 1 Task in MongoDB

In this Document using mongodb compass application i have given the Queries to get  data,

## I Executed 10 Questions in Command

Here the commands i executed for each Questions separately:

1. Find all the information about each products

```bash
db.products .find({});
```

2. Find the product price which are between 400 to 800

```bash
db.products .find({product_price: { $gt: 400, $lt: 800 }});
```

3. Find the product price which are not between 400 to 600

```bash
db.products .find({product_price: {$not: { $gte: 400, $lte: 600 }}});
```

4. List the four product which are grater than 500 in price

```bash
db.products .find({product_price:{$gt:500}}).limit(4)
```

5. Find the product name and product material of each products

```bash
db.products .find({},{ product_name: 1, product_material: 1 });
```

6. Find the product with a row id of 10

```bash
db.products .find({id: '10'});
```

7. Find only the product name and product material

```bash
db.products .find({},{ product_name: 1, prodduct_material: 1 });
```

8. Find all products which contain the value of soft in product material

```bash
db.products .find({product_material: 'Soft'});
```

9. Find products which contain product color indigo and product price 492.00

```bash
db.products.find({ [{ product_price: 492 },{ product_color: 'indigo' }]});
```
```bash
10. Delete the products which product price value are same
db.products.deleteOne({product_price:28});

````

## License

This project is licensed under the [License Name] - see the [LICENSE.md](LICENSE.md) file for details.
