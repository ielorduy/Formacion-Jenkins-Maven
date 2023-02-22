def num1=3
def num2=2
pipeline
{
    agent any
	stages
	{
        stage("Variables")
        {
            steps
            {
                script
                {
                    println "num1: "+ num1
                    println "num2: "+ num2
                }
            }
            
        }    
		
        stage("EscribirFichero")
        {
            steps
            {
                script
                {
                    def multiplicacion = num1*num2
                    def suma = num1+num2
                    def potencia= (suma)*(suma)
                    			
                    def info = "Multiplicación:"+multiplicacion+" || Potencia: "+potencia
                    println "Cálculos:\n"+info		
                    writeFile (file: "salida.txt", text: info)
                }
            }
            
        }
	}
}
