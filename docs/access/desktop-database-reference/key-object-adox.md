---
title: Objeto Key (ADOX - referência de banco de dados da área de trabalho do Access)
TOCTitle: Key Object (ADOX)
ms:assetid: 727198ec-57d2-7766-790c-370beb931de6
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249461(v=office.15)
ms:contentKeyID: 48545608
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: c77e45f52994f14d79acf424da14b55b2cdd9814
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25465470"
---
# <a name="key-object-adox"></a>Objeto Key (ADOX)


**Aplica-se a**: Access 2013 | Office 2013

Representa um campo de chave primária, estrangeira ou exclusiva de uma tabela de banco de dados.

## <a name="remarks"></a>Comentários

O código a seguir criar uma nova **Chave**:

`Dim obj As New Key`

Com as propriedades e coleções de um objeto **Key**, você pode:

- Identificar a chave com a propriedade [Name](name-property-adox.md).

- Determinar se a chave é primária, externa ou exclusiva com a propriedade [Type](https://msdn.microsoft.com/library/jj248879\(v=office.15\)).

- Acessar as colunas do banco de dados da chave com a coleção [Columns](columns-collection-adox.md).

- Especificar o nome da tabela relacionada com a propriedade [RelatedTable](relatedtable-property-adox.md).

- Determinar a ação executada na exclusão ou atualização de uma chave primária com as propriedades [DeleteRule](deleterule-property-adox.md) e [UpdateRule](updaterule-property-adox.md).

