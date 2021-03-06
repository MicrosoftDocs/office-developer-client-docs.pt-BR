---
title: Objeto Column (ADOX)
TOCTitle: Column object (ADOX)
ms:assetid: ad38c2df-f704-0599-4b7a-8556e430ba46
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249811(v=office.15)
ms:contentKeyID: 48547034
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 188f70d32237385cd82979589aecb989f18748b0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296245"
---
# <a name="column-object-adox"></a>Objeto Column (ADOX)


**Aplica-se ao:** Access 2013, Office 2013

Representa uma coluna de uma tabela, um índice ou uma chave.

## <a name="remarks"></a>Comentários

O código a seguir cria uma nova **Coluna**:

`Dim obj As New Column`

Com as propriedades e coleções de um objeto **Column**, você pode:

  - Identificar a coluna com a propriedade [Name](name-property-adox.md).

  - Especificar os tipos de dados da coluna com a propriedade [Type](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/type-property-columnadox).

  - Determinar se a coluna tem tamanho fixo ou se ela pode conter valores nulos com a propriedade [Attributes](attributes-property-adox.md).

  - Especificar o tamanho máximo da coluna com a propriedade [DefinedSize](definedsize-property-adox.md).

  - Para valores de dados numéricos, especificar a escala com a propriedade [NumericScale](numericscale-property-adox.md).

  - Para valores de dados numéricos, especificar a precisão máxima com a propriedade [Precision](precision-property-adox.md).

  - Especificar o [Catálogo](catalog-object-adox.md) que contém a coluna com a propriedade [ParentCatalog](parentcatalog-property-adox.md).

  - Para colunas-chave, especificar o nome da coluna relacionada na tabela relacionada com a propriedade [RelatedColumn](relatedcolumn-property-adox.md).

  - Para colunas de índice, especificar se a ordem de classificação é ascendente ou descendente com a propriedade [SortOrder](sortorder-property-adox.md).

  - Acessar propriedades específicas do provedor com a coleção [Properties](properties-collection-ado.md).


> [!NOTE]
> [!OBSERVAçãO] Seu provedor de dados talvez não ofereça suporte para todas as propriedades dos objetos **Column**. Um erro ocorrerá se você tiver definido um valor para uma propriedade para a qual o provedor não oferece suporte. Para novos objetos **Column**, o erro ocorrerá quando o objeto for acrescentado à coleção. Para objetos existentes, o erro ocorrerá ao definir a propriedade.
> 
> Ao criar objetos **Column**, a existência de um valor padrão apropriado para uma propriedade opcional não garante que seu provedor de dados ofereça suporte para a propriedade. Para obter mais informações sobre quais propriedades têm suporte do seu provedor, consulte a documentação do seu provedor.

