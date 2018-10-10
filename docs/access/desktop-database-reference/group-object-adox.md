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
# <a name="group-object-adox"></a><span data-ttu-id="b10d9-102">Objeto Group (ADOX)</span><span class="sxs-lookup"><span data-stu-id="b10d9-102">Group Object (ADOX)</span></span>


<span data-ttu-id="b10d9-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="b10d9-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="b10d9-104">Representa uma conta de grupo que tem permissões de acesso em um banco de dados protegido.</span><span class="sxs-lookup"><span data-stu-id="b10d9-104">Represents a group account that has access permissions within a secured database.</span></span>

## <a name="remarks"></a><span data-ttu-id="b10d9-105">Comentários</span><span class="sxs-lookup"><span data-stu-id="b10d9-105">Remarks</span></span>

<span data-ttu-id="b10d9-p101">A coleção [Groups](groups-collection-adox.md) de um [Catálogo](catalog-object-adox.md) representa todas as contas de grupo do catálogo. A coleção **Groups** de um [Usuário](user-object-adox.md) representa apenas o grupo ao qual o usuário pertence.</span><span class="sxs-lookup"><span data-stu-id="b10d9-p101">The [Groups](groups-collection-adox.md) collection of a [Catalog](catalog-object-adox.md) represents all the catalog's group accounts. The **Groups** collection for a [User](user-object-adox.md) represents only the group to which the user belongs.</span></span>

<span data-ttu-id="b10d9-108">Com as propriedades, as coleções e os métodos de um objeto **Group**, você pode:</span><span class="sxs-lookup"><span data-stu-id="b10d9-108">With the properties, collections, and methods of a **Group** object, you can:</span></span>

  - <span data-ttu-id="b10d9-109">Identificar o grupo com a propriedade [Name](name-property-adox.md).</span><span class="sxs-lookup"><span data-stu-id="b10d9-109">Identify the group with the [Name](name-property-adox.md) property.</span></span>

  - <span data-ttu-id="b10d9-110">Determinar se um grupo tem permissões de leitura, gravação ou exclusão com os métodos [GetPermissions](getpermissions-method-adox.md) e [SetPermissions](setpermissions-method-adox.md).</span><span class="sxs-lookup"><span data-stu-id="b10d9-110">Determine whether a group has read, write, or delete permissions with the [GetPermissions](getpermissions-method-adox.md) and [SetPermissions](setpermissions-method-adox.md) methods.</span></span>

  - <span data-ttu-id="b10d9-111">Acessar as contas de usuários que têm associações no grupo com a coleção [Users](users-collection-adox.md).</span><span class="sxs-lookup"><span data-stu-id="b10d9-111">Access the user accounts that have memberships in the group with the [Users](users-collection-adox.md) collection.</span></span>

  - <span data-ttu-id="b10d9-112">Acessar propriedades específicas do provedor com a coleção [Properties](properties-collection-ado.md).</span><span class="sxs-lookup"><span data-stu-id="b10d9-112">Access provider-specific properties with the [Properties](properties-collection-ado.md) collection.</span></span>

