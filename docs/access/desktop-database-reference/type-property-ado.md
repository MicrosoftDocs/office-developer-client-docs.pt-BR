---
<<<<<<< Título cabeça: TOCTitle propriedade tipo (ADO): tipo de propriedade (ADO) === título: (ADO) a propriedade Type TOCTitle: digite propriedade (ADO)
>>>>>>> ms:assetid de mestre: 14d99172-2145-05ae-620b-459ba097f05c ms:mtpsurl: https://msdn.microsoft.com/library/JJ248914(v=office.15) ms:contentKeyID: ms.date 48543397: 18/09/2015 mtps_version: v=office.15
---

<<<<<<< Cabeça
# <a name="type-property-ado"></a>Propriedade Type (ADO)
=======
# <a name="type-property-ado"></a>Propriedade Type (ADO)
>>>>>>> mestre


**Aplica-se a**: Access 2013 | Office 2013

Indica o tipo operacional ou o tipo de dados de um objeto [Parameter](parameter-object-ado.md), [Field](field-object-ado.md) ou [Property](property-object-ado.md).

<<<<<<< Cabeça
## <a name="settings-and-return-values"></a>Configurações e valor de retorno
=======
## <a name="settings-and-return-values"></a>Configurações e valores de retorno
>>>>>>> mestre

Define ou retorna um valor [DataTypeEnum](datatypeenum.md).

## <a name="remarks"></a>Comentários

Para os objetos **Parameter**, a propriedade **Type** é leitura/gravação. Para novos objetos **Field** que foram acrescentados à coleção [Fields](fields-collection-ado.md) de um [Record](record-object-ado.md), **Type** é leitura/gravação somente depois que a propriedade [Value](value-property-ado.md) para o **Field** for especificada e o provedor de dados adicionar com êxito o novo **Field** chamando o método [Update](update-method-ado.md) da coleção **Fields**.

Para todos os outros objetos, a propriedade **Type** é somente leitura.

