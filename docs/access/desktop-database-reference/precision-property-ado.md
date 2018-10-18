---
<<<<<<< Título cabeça: propriedade Precision (ADO) TOCTitle: propriedade Precision (ADO) === título: propriedade Precision (ADO) TOCTitle: a propriedade Precision (ADO)
>>>>>>> ms:assetid de mestre: c9d54d78-d5a5-caf8-d635-259d1fcc0595 ms:mtpsurl: https://msdn.microsoft.com/library/JJ249983(v=office.15) ms:contentKeyID: ms.date 48547685: 18/09/2015 mtps_version: v=office.15
---

<<<<<<< Cabeça
# <a name="precision-property-ado"></a>Propriedade Precision (ADO)
=======
# <a name="precision-property-ado"></a>Propriedade Precision (ADO)
>>>>>>> mestre


**Aplica-se a**: Access 2013 | Office 2013

Indica o grau de precisão de valores numéricos em um objeto [Parameter](parameter-object-ado.md) ou de objetos [Field](field-object-ado.md) numéricos.

<<<<<<< Cabeça
## <a name="settings-and-return-values"></a>Configurações e valor de retorno
=======
## <a name="settings-and-return-values"></a>Configurações e valores de retorno
>>>>>>> mestre

Define ou retorna um valor **Byte** que indica o número máximo de dígitos utilizado para representar os valores.

## <a name="remarks"></a>Comentários

Utilize a propriedade **Precision** para determinar o número máximo de dígitos utilizado para representar os valores de um objeto numérico **Parameter** ou **Field**.

O valor é leitura/gravação em um objeto **Parameter**.

Para um objeto **Field**, a propriedade **Precision** normalmente é somente leitura. Entretanto, para novos objetos **Field** que tenham sido acrescentados à coleção [Fields](fields-collection-ado.md) de um [Record](record-object-ado.md), **Precision** será leitura/gravação somente depois que a propriedade [Value](value-property-ado.md) de **Field** tiver sido especificada e o provedor de dados tiver adicionado com êxito o novo **Field** por meio da chamada do método [Update](update-method-ado.md) da coleção **Fields**.

