---
title: Objeto Key (ADOX - referência de banco de dados da área de trabalho do Access)
TOCTitle: Key object (ADOX)
ms:assetid: 727198ec-57d2-7766-790c-370beb931de6
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249461(v=office.15)
ms:contentKeyID: 48545608
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: f56a90b7accd1b64c9a52e0a7cf5385f83fd10d5
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28717136"
---
# <a name="key-object-adox"></a>Objeto Key (ADOX)


**Aplica-se a**: Access 2013, o Office 2013

Representa um campo de chave primária, estrangeira ou exclusiva de uma tabela de banco de dados.

## <a name="remarks"></a>Comentários

O código a seguir criar uma nova **Chave**:

`Dim obj As New Key`

Com as propriedades e coleções de um objeto **Key**, você pode:

- Identificar a chave com a propriedade [Name](name-property-adox.md).

- Determinar se a chave é primária, externa ou exclusiva com a propriedade [Type](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/type-property-keyadox).

- Acessar as colunas do banco de dados da chave com a coleção [Columns](columns-collection-adox.md).

- Especificar o nome da tabela relacionada com a propriedade [RelatedTable](relatedtable-property-adox.md).

- Determinar a ação executada na exclusão ou atualização de uma chave primária com as propriedades [DeleteRule](deleterule-property-adox.md) e [UpdateRule](updaterule-property-adox.md).

