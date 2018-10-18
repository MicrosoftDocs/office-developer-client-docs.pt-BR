---
<<<<<<< Título cabeça: propriedade ActualSize (ADO) TOCTitle: ms:assetid propriedade ActualSize (ADO): 020a414d-e6aa-5fb9-9b77-bd9d10124f8a ms:mtpsurl: https://msdn.microsoft.com/library/JJ248787(v=office.15) ms:contentKeyID: ms.date 48542949: 18/09/2015 mtps_version: v = Office.15
---

# <a name="actualsize-property-ado"></a>Propriedade ActualSize (ADO)
=== título: propriedade ActualSize (ADO) TOCTitle: ms:assetid de propriedade (ADO) ActualSize: 020a414d-e6aa-5fb9-9b77-bd9d10124f8a ms:mtpsurl: https://msdn.microsoft.com/library/JJ248787(v=office.15) ms:contentKeyID: ms.date 48542949: 10/16/2018 mtps_version: v=office.15
---

# <a name="actualsize-property-ado"></a>Propriedade ActualSize (ADO)
>>>>>>> mestre

**Aplica-se a**: Access 2013 | Office 2013

Indica o tamanho real do valor de um campo.

<<<<<<< Cabeça
## <a name="settings-and-return-values"></a>Configurações e valor de retorno
=======
## <a name="settings-and-return-values"></a>Configurações e valores de retorno
>>>>>>> mestre

Retorna um valor **Long**. Alguns provedores talvez permitam que essa propriedade seja definida para reservar espaço para dados BLOB, caso em que o valor padrão é 0.

## <a name="remarks"></a>Comentários

Use a propriedade **ActualSize** para retornar o tamanho real do valor de um objeto [Field](field-object-ado.md). Para todos os campos, a propriedade **ActualSize** é somente leitura. Se o ADO não puder determinar o tamanho do valor do objeto **Field**, a propriedade **ActualSize** retornará **adUnknown**.

<<<<<<< De cabeçalho **ActualSize** e [DefinedSize](definedsize-property-ado.md) propriedades são diferentes, conforme mostrado no exemplo a seguir. Um objeto **Field** com um tipo declarado de **adVarChar** e um comprimento máximo de 50 caracteres retornará um valor de propriedade **DefinedSize** de 50, mas o valor da propriedade **ActualSize** a ser retornado será o tamanho dos dados armazenados no campo para o registro atual. **Fields** com um **DefinedSize** maior do que 255 bytes serão tratados como colunas de comprimento variável.
=== As propriedades **ActualSize** e [DefinedSize](definedsize-property-ado.md) são diferentes. Um objeto **Field** com um tipo declarado de **adVarChar** e um comprimento máximo de 50 caracteres retornará um valor de propriedade **DefinedSize** de 50, mas o valor da propriedade **ActualSize** a ser retornado será o tamanho dos dados armazenados no campo para o registro atual. **Fields** com um **DefinedSize** maior do que 255 bytes serão tratados como colunas de comprimento variável.
>>>>>>> mestre

