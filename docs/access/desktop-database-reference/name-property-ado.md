---
<<<<<<< Título cabeça: TOCTitle nome Property (ADO): nome Property (ADO) === título: nome de propriedade (ADO) TOCTitle: nome de propriedade (ADO)
>>>>>>> ms:assetid de mestre: 4b19bd08-ac3c-86f0-471d-06a37a0d4f89 ms:mtpsurl: https://msdn.microsoft.com/library/JJ249234(v=office.15) ms:contentKeyID: ms.date 48544683: 18/09/2015 mtps_version: v=office.15
---

<<<<<<< Cabeça
# <a name="name-property-ado"></a>Propriedade Name (ADO)
=======
# <a name="name-property-ado"></a>Propriedade Name (ADO)
>>>>>>> mestre


**Aplica-se a**: Access 2013 | Office 2013

Indica o nome de um objeto

<<<<<<< Cabeça
## <a name="settings-and-return-values"></a>Configurações e valor de retorno
=======
## <a name="settings-and-return-values"></a>Configurações e valores de retorno
>>>>>>> mestre

Define ou retorna um valor **String** que indica o nome de um objeto.

## <a name="remarks"></a>Comentários

Use a propriedade **Name** para atribuir um nome ou recuperar o nome de um objeto **Command**, **Property**, **Field** ou **Parameter**.

O valor é leitura/gravação em um objeto **Command** e somente leitura em um objeto **Property**.

Para um objeto **Field**, **Name** normalmente é somente leitura. No entanto, para novos objetos **Field** que foram acrescentados à coleção [Fields](fields-collection-ado.md) de um [Record](record-object-ado.md), **Name** será leitura/gravação apenas depois que a propriedade [Value](value-property-ado.md) para **Field** for especificada e o provedor de dados adicionar com sucesso o novo **Field** chamando o método [Update](update-method-ado.md) da coleção **Fields**.

Para os objetos **Parameter** que ainda não foram acrescentados à coleção [Parameters](parameters-collection-ado.md), a propriedade **Name** é leitura/gravação. Para objetos **Parameter** acrescentados e todos os outros objetos, a propriedade **Name** é somente leitura. Os nomes não precisam ser exclusivos em uma coleção.

Você pode recuperar a propriedade **Name** de um objeto por uma referência ordinal, após a qual pode se referir ao objeto diretamente pelo nome. Por exemplo, se rstMain.Properties(20). Nome produz a capacidade de atualização, você pode se referir a essa propriedade como produz a capacidade de atualização, você pode se referir a essa propriedade como rstMain.Properties("Updatability").

