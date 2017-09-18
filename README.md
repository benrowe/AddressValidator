# AddressValidator

An address validation component written in php that provides per country/region validation rules

## Example usage

    $address = new Address;
    
    $address->setDetails([
      'country' => Country::AUSTRALIA,
      'region' => 'NSW',
      'city' => 'Sydney',
      'postal_code' => '2000',
      'street_address' => [
        '1 George Street',
      ]
    ]);

    $addressValidator = new AddressValidator([]);
    if (!$addressValidator->validate($address)) {
      var_dump($addressValidator->getErrors());
      echo $addressValidator->getError('country');
    }

## Limitations

## Other
