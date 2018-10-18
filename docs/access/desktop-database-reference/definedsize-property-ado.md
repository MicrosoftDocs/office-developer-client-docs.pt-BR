---
<<<<<<< Título cabeça: propriedade DefinedSize (ADO) TOCTitle: propriedade DefinedSize (ADO) === título: propriedade DefinedSize (ADO) TOCTitle: a propriedade DefinedSize (ADO)
>>>>>>> ms:assetid de mestre: 8d6db4c9-fbdc-9fcd-63f0-bd677c5ebcf6 ms:mtpsurl: https://msdn.microsoft.com/library/JJ249619(v=office.15) ms:contentKeyID: ms.date 48546257: 18/09/2015 mtps_version: v=office.15
---

<<<<<<< Cabeça
# <a name="definedsize-property-ado"></a>Propriedade DefinedSize (ADO)
=======
# <a name="definedsize-property-ado"></a>Propriedade DefinedSize (ADO)
>>>>>>> mestre


**Aplica-se a**: Access 2013 | Office 2013

Indica a capacidade de dados de um objeto [Field](field-object-ado.md).

<<<<<<< Cabeça
## <a name="return-value"></a>Valor retornado
=======
## <a name="return-value"></a>Valor de retorno
>>>>>>> mestre

Retorna um valor **Long** que reflete o tamanho definido de um campo como um número de bytes.

## <a name="remarks"></a>Comentários

Use a propriedade **DefinedSize** para determinar a capacidade de dados de um objeto **Field**.

As propriedades **DefinedSize** e [ActualSize](actualsize-property-ado.md) são diferentes. Por exemplo, considere um objeto **Field** com um tipo declarado de **adVarChar** e um valor de propriedade **DefinedSize** de 50, contendo um único caractere. O valor da propriedade **ActualSize** retornado será a extensão em bytes deste único caractere.

