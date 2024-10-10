# Piedra-Papel-o-Tijeras
Este es el código fuente del trabajo Piedra, Papel o Tijeras
function elecciónCompu() {
    let opciones = ['piedra', 'papel', 'tijeras'];
    let numeroRandom = Math.floor(Math.random() * opciones.length);
    return opciones[numeroRandom];
}

// Función para determinar el ganador
function elegirGanador(eleccionJugador, eleccionCpu) {
    if (eleccionJugador === eleccionCpu) {
        return alert('Empate, por un poquitoo');
    }

    if (
        (eleccionJugador === 'piedra' && eleccionCpu === 'tijeras') ||
        (eleccionJugador === 'papel' && eleccionCpu === 'piedra') ||
        (eleccionJugador === 'tijeras' && eleccionCpu === 'papel')
    ) {
        return alert('¡Felicidadeeees Ganaste!');
    } else {
        return alert('Perdiste, suerte en la próxima!');
    }
}

// Función principal del juego
function juego(eleccionJugador) {
    let eleccionCpu = elecciónCompu();
    console.log(`Tu elección: ${eleccionJugador}`);
    console.log(`Elección de la computadora: ${eleccionCpu}`);
    let resultado = elegirGanador(eleccionJugador, eleccionCpu);
    
}
let eleccionJugador = prompt('elige entre "piedra", "papel" o "tijeras": '); // Cambia esto por 'piedra', 'papel' o 'tijeras' para probar
juego(eleccionJugador);
