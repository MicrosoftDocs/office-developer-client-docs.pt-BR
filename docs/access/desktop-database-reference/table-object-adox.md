---
title: Objeto Table (ADOX)
TOCTitle: Table Object (ADOX)
ms:assetid: 53a3e2f9-4ec0-8fed-d482-4f995921587b
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249273(v=office.15)
ms:contentKeyID: 48544874
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: b63014a57104d5d31f5ac5620b26712a9f97347b
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25869289"
---
# <a name="table-object-adox"></a>Objeto Table (ADOX)


**Aplica-se a**: Access 2013, o Office 2013

Representa uma tabela de banco de dados, incluindo colunas, índices e chaves.

## <a name="remarks"></a>Comentários

O código a seguir criar uma nova **Tabela**:

`Dim obj As New Table`

Com as propriedades e coleções de um objeto **Table**, você pode:

  - Identificar a tabela com a propriedade [Name](name-property-adox.md).

  - Determinar o tipo da tabela com a propriedade [Type](https://msdn.microsoft.com/library/jj250042\(v=office.15\)).

  - Acessar as colunas do banco de dados da tabela com a coleção [Columns](columns-collection-adox.md).

  - Acessar os índices da tabela com a coleção [Indexes](indexes-collection-adox.md).

  - Acessar as chaves da tabela com a coleção [Keys](keys-collection-adox.md).

  - Especificar o [Catálogo](catalog-object-adox.md) que contém a tabela com a propriedade [ParentCatalog](parentcatalog-property-adox.md).

  - Retornar informações de data com as propriedades [DateCreated](datecreated-property-adox.md) e [DateModified](datemodified-property-adox.md).

  - Acessar propriedades de tabela específicas do provedor com a coleção [Properties](properties-collection-ado.md).


> [!NOTE]
> <P>[!OBSERVAçãO] Seu provedor de dados talvez não ofereça suporte para todas as propriedades dos objetos <STRONG>Table</STRONG>. Um erro ocorrerá se você tiver definido um valor para uma propriedade para a qual o provedor não oferece suporte. Para novos objetos <STRONG>Table</STRONG>, o erro ocorrerá quando o objeto for acrescentado à coleção. Para objetos existentes, o erro ocorrerá ao definir a propriedade.</P>



Ao criar objetos **Table**, a existência de um valor padrão apropriado para uma propriedade opcional não garante que seu provedor de dados ofereça suporte para a propriedade. Para obter mais informações sobre quais propriedades têm suporte do seu provedor, consulte a documentação do seu provedor.

