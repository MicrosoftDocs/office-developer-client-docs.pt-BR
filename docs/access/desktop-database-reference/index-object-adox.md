---
title: Objeto Index (ADOX)
TOCTitle: Index object (ADOX)
ms:assetid: fe368ab1-e396-4684-d930-18b0ba58a925
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250304(v=office.15)
ms:contentKeyID: 48548929
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 02d12fffa2c766425054e344e9f7d9d7a22cb517
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32291772"
---
# <a name="index-object-adox"></a>Objeto Index (ADOX)

**Aplica-se ao:** Access 2013, Office 2013

Representa um índice de uma tabela de banco de dados.

## <a name="remarks"></a>Comentários

O código a seguir criar um novo **Índice**:

`Dim obj As New Index`

Com as propriedades e coleções de um objeto **Index**, você pode:

- Identificar o índice com a propriedade [Name](name-property-adox.md).

- Acessar as colunas do banco de dados do índice com a coleção [Columns](columns-collection-adox.md).

- Especificar se as chaves de índice devem ser exclusivas com a propriedade [Unique](unique-property-adox.md).

- Especificar se o índice é a chave primária de uma tabela com a propriedade [PrimaryKey](primarykey-property-adox.md).

- Especificar se os registros que têm valores nulos em seus campos de índice têm entradas de índice com a propriedade [IndexNulls](indexnulls-property-adox.md).

- Especificar se o índice está agrupado com a propriedade [Clustered](clustered-property-adox.md).

- Acessar propriedades de índice específicas do provedor com a coleção [Properties](properties-collection-ado.md).


> [!NOTE]
> [!OBSERVAçãO] Ocorrerá um erro ao anexar uma [Coluna](column-object-adox.md) à coleção **Columns** de um **Índice**, se a **Coluna** não existir em um objeto [Table](table-object-adox.md) já anexado à coleção [Tables](tables-collection-adox.md).

Seu provedor de dados talvez não ofereça suporte para todas as propriedades dos objetos **Index**. Um erro ocorrerá se você tiver definido um valor para uma propriedade para a qual o provedor não oferece suporte. Para novos objetos **Index**, o erro ocorrerá quando o objeto for acrescentado à coleção. Para objetos existentes, o erro ocorrerá ao definir a propriedade.

Ao criar objetos **Index**, a existência de um valor padrão apropriado para uma propriedade opcional não garante que seu provedor de dados ofereça suporte para a propriedade. Para obter mais informações sobre quais propriedades têm suporte do seu provedor, consulte a documentação do seu provedor.

