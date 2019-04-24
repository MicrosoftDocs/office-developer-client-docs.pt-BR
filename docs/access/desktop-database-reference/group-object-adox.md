---
title: Objeto Group (ADOX)
TOCTitle: Group object (ADOX)
ms:assetid: 91cf1b87-c928-1d89-2731-138f6299cc60
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249642(v=office.15)
ms:contentKeyID: 48546359
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: e010ac58ff0b573d42c562ce3be7a99acab5abea
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292115"
---
# <a name="group-object-adox"></a>Objeto Group (ADOX)


**Aplica-se ao:** Access 2013, Office 2013

Representa uma conta de grupo que tem permissões de acesso em um banco de dados protegido.

## <a name="remarks"></a>Comentários

A coleção [Groups](groups-collection-adox.md) de um [Catálogo](catalog-object-adox.md) representa todas as contas de grupo do catálogo. A coleção **Groups** de um [Usuário](user-object-adox.md) representa apenas o grupo ao qual o usuário pertence.

Com as propriedades, as coleções e os métodos de um objeto **Group**, você pode:

  - Identificar o grupo com a propriedade [Name](name-property-adox.md).

  - Determinar se um grupo tem permissões de leitura, gravação ou exclusão com os métodos [GetPermissions](getpermissions-method-adox.md) e [SetPermissions](setpermissions-method-adox.md).

  - Acessar as contas de usuários que têm associações no grupo com a coleção [Users](users-collection-adox.md).

  - Acessar propriedades específicas do provedor com a coleção [Properties](properties-collection-ado.md).

