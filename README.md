# AddressValidator

An address validation component written in php that provides per country/region validation rules

## Example usage

    $addressValidator = new AddressValidator($options);
    $address = [
      'country' => 'AU',
      'region' => 'NSW',
      'city' => 'Sydney',
      'postal_code' => '2000',
      'street_address' => [
        '1 George Street',
      ]
    ];
    if (!$addressValidator->validate($address)) {
      var_dump($addressValidator->getErrors());
      echo $addressValidator->getError('country');
    }

## Limitations

## Other
