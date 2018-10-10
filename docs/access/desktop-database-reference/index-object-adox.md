---
title: Objeto Index (ADOX)
TOCTitle: Index Object (ADOX)
ms:assetid: fe368ab1-e396-4684-d930-18b0ba58a925
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250304(v=office.15)
ms:contentKeyID: 48548929
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 535ca6a597c6dd580146f6142731897600264526
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25463370"
---
# <a name="index-object-adox"></a>Objeto Index (ADOX)

**Aplica-se a**: Access 2013 | Office 2013

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

