# routing


INDEX:JS =========>
const express = require('express');
const app = express();

const librosRouter = require('./moduloLibros')

app.use('/libros', librosRouter)

app.listen(3000, () => {
    console.log('Servidor corriendo');
})



MODULO.js ==============>
const express = require('express');

const router = express.Router();


// Rutas 
router.get('/', (req, res) => {
    res.send('listar libros')
})

router.post('/', (req, res) => {
    res.send('Crear un libro')
})

router.get('/:id', (req, res) => {
    res.send(req.params.id)
})

module.exports = router;
