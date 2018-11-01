---
title: Coleção Users (ADOX)
TOCTitle: Users Collection (ADOX)
ms:assetid: bc61c862-1637-02e7-4b56-5ad984bdbcb0
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249905(v=office.15)
ms:contentKeyID: 48547413
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: c3415fb7a2972621978ba3673343eb5f32b0eec1
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25885616"
---
# <a name="users-collection-adox"></a>Coleção Users (ADOX)


**Aplica-se a**: Access 2013, o Office 2013

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
> <P>[!OBSERVAçãO] Antes de um objeto <STRONG>User</STRONG> ser anexado à coleção <STRONG>Users</STRONG> de um objeto <STRONG>Group</STRONG>, na coleção <STRONG>Users</STRONG> do <A href="name-property-adox.md">Catálogo</A> já deve existir um objeto <STRONG>User</STRONG> com o mesmo <STRONG>Nome</STRONG> daquele a ser anexado.</P>


