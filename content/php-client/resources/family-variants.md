## Family variants

### Get a family variant

```php
$client = new \Akeneo\Pim\AkeneoPimClientBuilder('http://akeneo.com/')->buildAuthenticatedByPassword('client_id', 'secret', 'admin', 'admin');
                     
/*
 * Returns an array like this:
 * [
 *     'code' => 'boots_color_size',
 *     'labels' => [
 *         'de_DE' => 'Stiefel nach Farbe und Größe',
 *         'en_US' => 'Boots by color and size',
 *         'fr_FR' => 'Bottes par couleur et taille'
 *     ],
 *     'variant_attribute_sets' => [
 *         [
 *             'level' => 1,
 *             'axes' => ['color'],
 *             'attributes' => ['name', 'description', 'color']
 *         ],
 *         [
 *             'level' => 2,
 *             'axes' => ['size'],
 *             'attributes' => ['sku', 'size']
 *         ]
 *     ]
 * ]
 */
$familyVariant = $client->getFamilyVariantApi()->get('boots', 'boots_color_size');
```