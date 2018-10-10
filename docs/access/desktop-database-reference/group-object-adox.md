---
title: Objeto Group (ADOX)
TOCTitle: Group Object (ADOX)
ms:assetid: 91cf1b87-c928-1d89-2731-138f6299cc60
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249642(v=office.15)
ms:contentKeyID: 48546359
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 21caab66c16c4ca9f77c49f33bf99f4df7be79c7
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25464368"
---
# <a name="group-object-adox"></a>Objeto Group (ADOX)


**Aplica-se a**: Access 2013 | Office 2013

Representa uma conta de grupo que tem permissões de acesso em um banco de dados protegido.

## <a name="remarks"></a>Comentários

A coleção [Groups](groups-collection-adox.md) de um [Catálogo](catalog-object-adox.md) representa todas as contas de grupo do catálogo. A coleção **Groups** de um [Usuário](user-object-adox.md) representa apenas o grupo ao qual o usuário pertence.

Com as propriedades, as coleções e os métodos de um objeto **Group**, você pode:

  - Identificar o grupo com a propriedade [Name](name-property-adox.md).

  - Determinar se um grupo tem permissões de leitura, gravação ou exclusão com os métodos [GetPermissions](getpermissions-method-adox.md) e [SetPermissions](setpermissions-method-adox.md).

  - Acessar as contas de usuários que têm associações no grupo com a coleção [Users](users-collection-adox.md).

  - Acessar propriedades específicas do provedor com a coleção [Properties](properties-collection-ado.md).

