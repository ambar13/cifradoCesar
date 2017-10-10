**creas una funcion cipher**

+ function cipher(frase){

**declaras Code donde vacio donde se llenara los datos luego**
 + var code ="";

**declaras frase para poder ingresar mediante el prompt el llenado manual**

   + frase = prompt("Ingresa Frase:");
**inicias un for, que inicializa en 0 y es la longitud de la frase, recorriendo de uno en uno**

 +  for (var i=0; i<frase.length; i++){
**declaras newLet como una nueva letra**
    var  newLet= frase.charCodeAt(i);

**condicionas para las letras mayusculas en la tabla ASCII**
    if(newLet >= 65 && newLet <= 90){
      var Letter = (newLet - 65 + 33)% 26 + 65;
      var alpha = String.fromCharCode(Letter);
      code = code + alpha;
  }

**para las minusculas en la tabla ASCII**
  else if(newLet >= 97 && newLet <= 122){
    letterMin = (newLet - 97 + 33)%26 +97;
    var nLetterMin = String.fromCharCode(letterMin);
    code = code + nLetterMin;
   }
}  
return code;

 }
 **el alert te retornara la frase a cifrar**
alert("Aplicando el cifrado:" +cipher(""));

![Diagrama de Flujo](assets docs/diagrama.jpg)

