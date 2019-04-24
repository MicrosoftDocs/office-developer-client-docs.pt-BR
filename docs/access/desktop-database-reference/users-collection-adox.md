---
title: Coleção Users (ADOX)
TOCTitle: Users collection (ADOX)
ms:assetid: bc61c862-1637-02e7-4b56-5ad984bdbcb0
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249905(v=office.15)
ms:contentKeyID: 48547413
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 24d7a5cab3260dac80b39e5134938c5f55175851
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32312933"
---
# <a name="users-collection-adox"></a>Coleção Users (ADOX)

**Aplica-se ao:** Access 2013, Office 2013

Contém todos os objetos [User](user-object-adox.md) armazenados de um catálogo ou grupo.

## <a name="remarks"></a>Comentários

A coleção **Users** de um objeto [Catalog](catalog-object-adox.md) representa todos os usuários do catálogo. A coleção **Users** de um objeto [Group](group-object-adox.md) representa apenas os usuários associados ao grupo específico.

O método [Append](append-method-adox-users.md) de uma coleção **Users** é exclusivo do ADOX. Você pode:

- Adicionar um novo usuário à coleção com o método **Append**.

As propriedades e os métodos restantes são padrão das coleções do ADO. Você pode:

- Acessar um usuário na coleção com a propriedade [Item](item-property-ado.md).

- Retornar o número de usuários contidos na coleção com a propriedade [Count](count-property-ado.md).

- Remover um usuário da coleção com o método [Delete](delete-method-adox-collections.md).

- Atualizar os objetos da coleção para refletir o atual esquema do banco de dados com o método [Refresh](refresh-method-ado.md).

> [!NOTE]
> [!OBSERVAçãO] Antes de um objeto **User** ser anexado à coleção **Users** de um objeto **Group**, na coleção **Users** do [Catálogo](name-property-adox.md) já deve existir um objeto **User** com o mesmo **Nome** daquele a ser anexado.

