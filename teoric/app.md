//variáveis
let message: string = "Hello World";
console.log(message);

let episode: number = 4;
console.log("This episode " + episode);

episode += 1;
console.log("Next episode is " + episode);

let favoriteDroid: string;
favoriteDroid = 'BB-8';
console.log("My favorite droid id " + favoriteDroid);

//funções

//parametro da função será um number e ela retornará um boolean
let isEnoughtToBeatMF = function (parsecs: number): boolean {
    return parsecs < 12;
}

let distance: number = 14;
console.log(`Is ${distance} parsecs enought to beat Millenium Falcon? ${isEnoughtToBeatMF(distance) ? 'YES' : 'NO' }`)

//arrow function

//lado esquerdo da seta = parâmetros, lado direito da seta = implementação
let call = (name: string) => console.log(`Do you copy, ${name}?`);
call('R2');

//parâmetros padrões
function inc (speed: number, inc: number = 1): number {
    return speed + inc;
}

console.log(`inc(5,1) = ${inc(5,1)}`);



