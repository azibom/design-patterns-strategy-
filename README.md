# design-patterns-strategy-
design patterns (strategy)

```php
<?php

interface Gateway {
    public function setInfo($info);
    public function getName();
    public function pay();
}

class Payment {

    public $gateway;

    public function setGateway(Gateway $gateway) {
        $this->gateway = $gateway;
    }

    public function getName() {
        return $this->gateway->getName();
    }

    public function setInfo($info) {
        $this->gateway->setInfo = $info;
    }

    public function pay() {
        return $this->gateway->pay();
    }
} 

class Mellat implements Gateway {

    protected $info;

    public function setInfo($info) {
        $this->info = $info;
    }

    public function getName() {
        return "Mellat";
    }

    public function pay() {
        return $this->info ;
    }

} 

class Saderat implements Gateway {

    protected $info;

    public function setInfo($info) {
        $this->info = $info;
    }

    public function getName() {
        return "Saderat";
    }

    public function pay() {
        return $this->info ;
    }

} 


$payment = new Payment;
$payment->setGateway(new Mellat);
echo $payment->getName();

?>

```

It is easy to use it only you need to define an interface and then use it an you child classes and the the end like the example use it 
