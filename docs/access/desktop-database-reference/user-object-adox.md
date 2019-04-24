---
title: Objeto user (referência do banco de dados da área de trabalho do Access)
TOCTitle: User object (ADOX)
ms:assetid: e88b9a8a-e70f-c7ca-cb8c-bd274ff24948
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250178(v=office.15)
ms:contentKeyID: 48548426
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 3299a6c0742e7fcbbd26532f3522fdc96b7956b2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32313157"
---
# <a name="user-object-adox"></a>Objeto user (ADOX)


**Aplica-se ao:** Access 2013, Office 2013

Representa uma conta de usuário que tem permissões de acesso em um banco de dados protegido.

## <a name="remarks"></a>Comentários

A coleção [Users](users-collection-adox.md) de um [Catálogo](catalog-object-adox.md) representa todos os usuários do catálogo. A coleção **Users** de um [Grupo](group-object-adox.md) representa apenas os usuários do grupo específico.

Com as propriedades, as coleções e os métodos de um objeto **User**, você pode:

  - Identificar o usuário com a propriedade [Name](name-property-adox.md).

  - Alterar a senha de um usuário com o método [ChangePassword](changepassword-method-adox.md).

  - Determinar se um usuário tem permissões de leitura, gravação ou exclusão com os métodos [GetPermissions](getpermissions-method-adox.md) e [SetPermissions](setpermissions-method-adox.md).

  - Acessar os grupos aos quais um usuário pertence com a coleção [Groups](groups-collection-adox.md).

  - Acessar propriedades específicas do provedor com a coleção [Properties](properties-collection-ado.md).

