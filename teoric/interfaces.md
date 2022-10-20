class newSpacecraft{
    propulsor: string;

    constructor (propulsor: string){
        this.propulsor = propulsor;
    }

    jumpIntoHyperspace(){
        console.log('Entering hyperspace with ' + this.propulsor);
    } 
}

//herança -> EXTENDS -> consigo herdar as características
class newMilleniumFalcon extends newSpacecraft implements Containership {
    //interface
    cargoContainers: number;

    constructor(){
        //super -> invocar implementação da classe original
        super('hiperdrive');
        
        this.cargoContainers = 4;
    }

    jumpIntoHyperspace() {
        if(Math.random()>=0.5){
            super.jumpIntoHyperspace();
        } else{
            console.log('failed');
        }
    }
}

//INTERFACES
//definem um contrato que as classes devem obedecer
//conjunto de atributos para os objetos

interface Containership{
    cargoContainers: number;
    //olhar a classe millenium falcon acima
}  

//outro exemplo
function goodForTheJob(ship: Containership): boolean{
    return ship.cargoContainers > 2;
}


let newFalcon = new newMilleniumFalcon();
console.log(goodForTheJob(newFalcon));

//interfaces também podem herdar de outras interfaces
interface Smugglership extends Containership {
    hiddenContainers: number;
}