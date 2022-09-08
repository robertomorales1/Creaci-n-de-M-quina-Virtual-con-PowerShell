# Creacion-de-Maquina-Virtual-con-PowerShell
Azure Resource Manager: Creación de una virtual machine con Powershell.


Iniciamos sesión en portal.azure.com

![image](https://user-images.githubusercontent.com/106035353/188991566-35ab9418-c895-483c-83e7-9d7596064cc8.png)


Hacemos clic en el ícono de Cloudshell

![image](https://user-images.githubusercontent.com/106035353/188991658-e355b318-8e20-43b8-8872-7a9d5cfcf001.png)

SI NOS APARECE LA VENTANA SELECCIONAMOS POWERSHELL, DE NO SER ASÍ MÁS ADELANTE SE PODRÁ ELEGIR.
![image](https://user-images.githubusercontent.com/106035353/189007506-16d8aff2-d7e8-49b3-93e8-0981360b7857.png)

Hacemos clic en Mostrar configuración avanzada:

![image](https://user-images.githubusercontent.com/106035353/189007563-3c1ea929-3882-4768-95f3-9b154677d047.png)

Rellenamos los campos: Grupo de recursos-> lab13
Cuenta de almacenamiento-> cloudshell123
Recurso compartido de archivos-> almacenamientodeshell8283
Y damos clic en crear almacenamiento:

![image](https://user-images.githubusercontent.com/106035353/189007638-4b16d5da-e3fe-43dc-bebf-52567c063334.png)

Con el siguiente comando nos conectamos a nuestra cuenta para mostrar los recursos que tenemos: 

Get-AzResourceGroup | Format-Table

Puede ocurrir un error, por ejemplo que el nombre esté tomado, simplemente modificamos el campo por otro nombre:

![image](https://user-images.githubusercontent.com/106035353/189007844-3aacf64b-5d44-4369-be26-da1ec337a6c0.png)

Para proceder debe de mostrarse la terminal de powershell:

![image](https://user-images.githubusercontent.com/106035353/189008043-1d2f97d3-2fe0-4a50-9869-b4118746e7a1.png)

De no ser así, y aparecer bash, simplemente cliqueamos en la flecha hacia abajo ubicado en la esquina superior izquierda y damos clic en powershell:

![image](https://user-images.githubusercontent.com/106035353/189008180-04d339f9-6878-4131-bd57-2587b11877f0.png)

![image](https://user-images.githubusercontent.com/106035353/189008221-9569746f-af35-423f-af58-fc1d546b01db.png)

Y damos clic en confirmar:

![image](https://user-images.githubusercontent.com/106035353/189008296-e63f4217-8ee2-44ac-aefc-29f3314145a1.png)


En la terminal, con el siguiente comando nos conectamos a nuestra cuenta para mostrar los recursos que tenemos: 

Get-AzResourceGroup | Format-Table

![image](https://user-images.githubusercontent.com/106035353/189008455-99f72ecc-c4ad-4e4d-8bf6-b2a9b5b69ca7.png)

Escribimos el siguiente comando para crear una mv:

New-AzVm `
-ResourceGroupName “myRGPS” `
-Name “myVMPS” `
-Location “East US” `
-VirtualNetworkName “myVnetPS” `
-SubnetName “mySubnetPS”  `
-SecurityGroupName “myNSGPS” `
-PublicIpAddressName “myPublicIpPs”

![image](https://user-images.githubusercontent.com/106035353/189009501-ffa84c1d-39ac-48d2-8309-8c1515b9787e.png)

Ingresamos el usuario y el password (al ingresar el password no notarás los caracteres en pantalla pero sí se estará tomando en cuenta):

![image](https://user-images.githubusercontent.com/106035353/189009650-22bacc19-eb4f-44d5-ba65-a1f2928c42b6.png)

Verificamos en el Grupo de Recursos lo que se está creando:

![image](https://user-images.githubusercontent.com/106035353/189009768-462c9bb0-f0a6-4c77-8f76-fb6b4b21d960.png)

Abrimos haciendo clic en el recurso máquina virtual (myVMPS)

![image](https://user-images.githubusercontent.com/106035353/189009925-5fd133bc-719d-4f35-ac9f-a6e575d4578e.png)







