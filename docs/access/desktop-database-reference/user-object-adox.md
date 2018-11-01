---
title: Objeto User (ADOX - referência de banco de dados da área de trabalho do Access)
TOCTitle: User Object (ADOX)
ms:assetid: e88b9a8a-e70f-c7ca-cb8c-bd274ff24948
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250178(v=office.15)
ms:contentKeyID: 48548426
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 0c37e43f09fb4187de246e687d81dbd72463d390
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25889312"
---
# <a name="user-object-adox"></a>Objeto User (ADOX)


**Aplica-se a**: Access 2013, o Office 2013

Representa uma conta de usuário que tem permissões de acesso em um banco de dados protegido.

## <a name="remarks"></a>Comentários

A coleção [Users](users-collection-adox.md) de um [Catálogo](catalog-object-adox.md) representa todos os usuários do catálogo. A coleção **Users** de um [Grupo](group-object-adox.md) representa apenas os usuários do grupo específico.

Com as propriedades, as coleções e os métodos de um objeto **User**, você pode:

  - Identificar o usuário com a propriedade [Name](name-property-adox.md).

  - Alterar a senha de um usuário com o método [ChangePassword](changepassword-method-adox.md).

  - Determinar se um usuário tem permissões de leitura, gravação ou exclusão com os métodos [GetPermissions](getpermissions-method-adox.md) e [SetPermissions](setpermissions-method-adox.md).

  - Acessar os grupos aos quais um usuário pertence com a coleção [Groups](groups-collection-adox.md).

  - Acessar propriedades específicas do provedor com a coleção [Properties](properties-collection-ado.md).

