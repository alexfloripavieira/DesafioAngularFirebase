# :zap: Angular Firebase CRUD

* Angular 11 app to store fast-food orders in a Firebase database. They are then retrieved and shown in a table on-screen

*** Note: to open web links in a new window use: _ctrl+click on link_**

## :books: General info

* Firebase backend stores customer name and number and what they ordered.

## :camera: Screenshots

* ![Example screenshot](./img/checkout.png)

## :signal_strength: Technologies

* [Angular v11](https://angular.io/) javascript framework
* [Angular Material v11](https://material.angular.io/) component library
* [Angular Material Icons](https://material.io/resources/icons/?style=baseline)
* [Materialize v1](https://materializecss.com/) front-end framework based on Material Design

## :floppy_disk: Setup

* Install dependencies using `npm i`
* Run `ng serve` to get a server at `http://localhost:4200/`
* If required, run `ng build` to build the project. The build artifacts will be stored in the `dist/` directory. Use the `--prod` flag for a production build.

## :computer: Code Examples

* onSubmit function to get order data from form to createOrder function

```typescript
onSubmit() {
    this.ordersService.form.value.order = this.order;
    let data = this.ordersService.form.value;
    console.log('data: ', data); // {CustomerName: Edwward, orderNumber: 3, order: ["burger", "fries"]}

    this.ordersService.createOrder(data).then((res) => {
      console.log("fast food order created");
    });
  }
```

## :cool: Features

* working Firebase backend Database storage of customer orders

