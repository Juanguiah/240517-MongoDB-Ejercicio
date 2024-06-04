# Ejercicio
Crear 1 colección con mínimo 10 registros, usando todos los comandos CRUD.

# Solución:
Una vez creada la BD y el Cluster en Atlas, nos conectamos por medio de MongoDB y nos conectamos a la BD llamada 7Voltios, procedemos a ingresar a ella por medio de la consola _MONGOSH para insertar datos:

```
show dbs
7Voltios   40.00 KiB
admin     340.00 KiB
local       7.42 GiB
use 7Voltios
switched to db 7Voltios
show collections()
show collections
Materiales
db.Materiales.drop()
true
show collections
db.createCollection('Materiales')
{ ok: 1 }
show collections
Materiales
db.Materiales.insert({Categoria: 'Automatización y control (PLCs, sensores, contactores, etc.)',item: 'PLC', Costo: '500000'})
DeprecationWarning: Collection.insert() is deprecated. Use insertOne, insertMany, or bulkWrite.
{
  acknowledged: true,
  insertedIds: {
    '0': ObjectId('665e589b032143b827e37e59')
  }
}
db.Materiales.find({})
{
  _id: ObjectId('665e589b032143b827e37e59'),
  Categoria: 'Automatización y control (PLCs, sensores, contactores, etc.)',
  item: 'PLC',
  Costo: '500000'
}
db.Materiales.insert({Categoria: 'Canalización eléctrica (canaletas, tubos, ductos, etc.)',item: 'Caja 12x12x5cm', Costo: '9100'})
{
  acknowledged: true,
  insertedIds: {
    '0': ObjectId('665e5aa5032143b827e37e5a')
  }
}
db.Materiales.find({})
{
  _id: ObjectId('665e589b032143b827e37e59'),
  Categoria: 'Automatización y control (PLCs, sensores, contactores, etc.)',
  item: 'PLC',
  Costo: '500000'
}
{
  _id: ObjectId('665e5aa5032143b827e37e5a'),
  Categoria: 'Canalización eléctrica (canaletas, tubos, ductos, etc.)',
  item: 'Caja 12x12x5cm',
  Costo: '9100'
}
db.Materiales.insertMany([{Categoria: 'Dispositivos de protección eléctrica (breakers, fusibles, etc.)',item: 'Breaker 20A', Costo: '11200'},{Categoria: 'Equipos de distribución eléctrica (tableros, medidores, transformadores, etc.)', item: 'Contador eléctrico monofásico 15(60)A', Costo: '275000'}])
{
  acknowledged: true,
  insertedIds: {
    '0': ObjectId('665e5bc3032143b827e37e5b'),
    '1': ObjectId('665e5bc3032143b827e37e5c')
  }
}
db.Materiales.find({})
{
  _id: ObjectId('665e589b032143b827e37e59'),
  Categoria: 'Automatización y control (PLCs, sensores, contactores, etc.)',
  item: 'PLC',
  Costo: '500000'
}
{
  _id: ObjectId('665e5aa5032143b827e37e5a'),
  Categoria: 'Canalización eléctrica (canaletas, tubos, ductos, etc.)',
  item: 'Caja 12x12x5cm',
  Costo: '9100'
}
{
  _id: ObjectId('665e5bc3032143b827e37e5b'),
  Categoria: 'Dispositivos de protección eléctrica (breakers, fusibles, etc.)',
  item: 'Breaker 20A',
  Costo: '11200'
}
{
  _id: ObjectId('665e5bc3032143b827e37e5c'),
  Categoria: 'Equipos de distribución eléctrica (tableros, medidores, transformadores, etc.)',
  item: 'Contador eléctrico monofásico 15(60)A',
  Costo: '275000'
}
db.Materiales.insert({Categoria: 'Herramientas (andamio, escalera, arnés, taladro, etc.)',item: 'Analizador de redes', Costo: '1200000'})
{
  acknowledged: true,
  insertedIds: {
    '0': ObjectId('665e5c00032143b827e37e5d')
  }
}
db.Materiales.find({})
{
  _id: ObjectId('665e589b032143b827e37e59'),
  Categoria: 'Automatización y control (PLCs, sensores, contactores, etc.)',
  item: 'PLC',
  Costo: '500000'
}
{
  _id: ObjectId('665e5aa5032143b827e37e5a'),
  Categoria: 'Canalización eléctrica (canaletas, tubos, ductos, etc.)',
  item: 'Caja 12x12x5cm',
  Costo: '9100'
}
{
  _id: ObjectId('665e5bc3032143b827e37e5b'),
  Categoria: 'Dispositivos de protección eléctrica (breakers, fusibles, etc.)',
  item: 'Breaker 20A',
  Costo: '11200'
}
{
  _id: ObjectId('665e5bc3032143b827e37e5c'),
  Categoria: 'Equipos de distribución eléctrica (tableros, medidores, transformadores, etc.)',
  item: 'Contador eléctrico monofásico 15(60)A',
  Costo: '275000'
}
{
  _id: ObjectId('665e5c00032143b827e37e5d'),
  Categoria: 'Herramientas (andamio, escalera, arnés, taladro, etc.)',
  item: 'Analizador de redes',
  Costo: '1200000'
}
db.Materiales.insert({Categoria: 'Interruptores y tomacorrientes',item: 'Interruptor con tomacorriente', Costo: '13000'})
{
  acknowledged: true,
  insertedIds: {
    '0': ObjectId('665e5c2a032143b827e37e5e')
  }
}
db.Materiales.insert({Categoria: 'Luminarias y lámparas (reflector, panel led, etc.)',item: 'Lámpara de emergencia', Costo: '57000'})
{
  acknowledged: true,
  insertedIds: {
    '0': ObjectId('665e5c48032143b827e37e5f')
  }
}
db.Materiales.insert({Categoria: 'Material de fijación y sujeción (tornillos, abrazaderas, etc.)',item: 'Abrazadera metálica 1/2 pulgada', Costo: '1500'})
{
  acknowledged: true,
  insertedIds: {
    '0': ObjectId('665e5c6b032143b827e37e60')
  }
}
db.Materiales.insert({Categoria: 'Sistemas de cableado estructurado (Cable UTP, RJ45, etc.)',item: 'Cable UTP CAT 5E CCA Interior', Costo: '539'})
{
  acknowledged: true,
  insertedIds: {
    '0': ObjectId('665e5c91032143b827e37e61')
  }
}
db.Materiales.insert({Categoria: 'Mano de obra',item: 'Transporte intermunicipal para técnico', Costo: '12000'})
{
  acknowledged: true,
  insertedIds: {
    '0': ObjectId('665e5cbf032143b827e37e62')
  }
}
db.Materiales.find({})
{
  _id: ObjectId('665e589b032143b827e37e59'),
  Categoria: 'Automatización y control (PLCs, sensores, contactores, etc.)',
  item: 'PLC',
  Costo: '500000'
}
{
  _id: ObjectId('665e5aa5032143b827e37e5a'),
  Categoria: 'Canalización eléctrica (canaletas, tubos, ductos, etc.)',
  item: 'Caja 12x12x5cm',
  Costo: '9100'
}
{
  _id: ObjectId('665e5bc3032143b827e37e5b'),
  Categoria: 'Dispositivos de protección eléctrica (breakers, fusibles, etc.)',
  item: 'Breaker 20A',
  Costo: '11200'
}
{
  _id: ObjectId('665e5bc3032143b827e37e5c'),
  Categoria: 'Equipos de distribución eléctrica (tableros, medidores, transformadores, etc.)',
  item: 'Contador eléctrico monofásico 15(60)A',
  Costo: '275000'
}
{
  _id: ObjectId('665e5c00032143b827e37e5d'),
  Categoria: 'Herramientas (andamio, escalera, arnés, taladro, etc.)',
  item: 'Analizador de redes',
  Costo: '1200000'
}
{
  _id: ObjectId('665e5c2a032143b827e37e5e'),
  Categoria: 'Interruptores y tomacorrientes',
  item: 'Interruptor con tomacorriente',
  Costo: '13000'
}
{
  _id: ObjectId('665e5c48032143b827e37e5f'),
  Categoria: 'Luminarias y lámparas (reflector, panel led, etc.)',
  item: 'Lámpara de emergencia',
  Costo: '57000'
}
{
  _id: ObjectId('665e5c6b032143b827e37e60'),
  Categoria: 'Material de fijación y sujeción (tornillos, abrazaderas, etc.)',
  item: 'Abrazadera metálica 1/2 pulgada',
  Costo: '1500'
}
{
  _id: ObjectId('665e5c91032143b827e37e61'),
  Categoria: 'Sistemas de cableado estructurado (Cable UTP, RJ45, etc.)',
  item: 'Cable UTP CAT 5E CCA Interior',
  Costo: '539'
}
```
