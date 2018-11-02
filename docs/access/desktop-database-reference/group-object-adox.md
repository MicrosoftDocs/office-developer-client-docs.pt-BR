---
title: Objeto Group (ADOX)
TOCTitle: Group object (ADOX)
ms:assetid: 91cf1b87-c928-1d89-2731-138f6299cc60
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249642(v=office.15)
ms:contentKeyID: 48546359
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: b7196fd6a57292cb335f164d25807f19544076aa
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25925945"
---
# <a name="group-object-adox"></a><span data-ttu-id="91ece-102">Objeto Group (ADOX)</span><span class="sxs-lookup"><span data-stu-id="91ece-102">Group object (ADOX)</span></span>


<span data-ttu-id="91ece-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="91ece-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="91ece-104">Representa uma conta de grupo que tem permissões de acesso em um banco de dados protegido.</span><span class="sxs-lookup"><span data-stu-id="91ece-104">Represents a group account that has access permissions within a secured database.</span></span>

## <a name="remarks"></a><span data-ttu-id="91ece-105">Comentários</span><span class="sxs-lookup"><span data-stu-id="91ece-105">Remarks</span></span>

<span data-ttu-id="91ece-p101">A coleção [Groups](groups-collection-adox.md) de um [Catálogo](catalog-object-adox.md) representa todas as contas de grupo do catálogo. A coleção **Groups** de um [Usuário](user-object-adox.md) representa apenas o grupo ao qual o usuário pertence.</span><span class="sxs-lookup"><span data-stu-id="91ece-p101">The [Groups](groups-collection-adox.md) collection of a [Catalog](catalog-object-adox.md) represents all the catalog's group accounts. The **Groups** collection for a [User](user-object-adox.md) represents only the group to which the user belongs.</span></span>

<span data-ttu-id="91ece-108">Com as propriedades, as coleções e os métodos de um objeto **Group**, você pode:</span><span class="sxs-lookup"><span data-stu-id="91ece-108">With the properties, collections, and methods of a **Group** object, you can:</span></span>

  - <span data-ttu-id="91ece-109">Identificar o grupo com a propriedade [Name](name-property-adox.md).</span><span class="sxs-lookup"><span data-stu-id="91ece-109">Identify the group with the [Name](name-property-adox.md) property.</span></span>

  - <span data-ttu-id="91ece-110">Determinar se um grupo tem permissões de leitura, gravação ou exclusão com os métodos [GetPermissions](getpermissions-method-adox.md) e [SetPermissions](setpermissions-method-adox.md).</span><span class="sxs-lookup"><span data-stu-id="91ece-110">Determine whether a group has read, write, or delete permissions with the [GetPermissions](getpermissions-method-adox.md) and [SetPermissions](setpermissions-method-adox.md) methods.</span></span>

  - <span data-ttu-id="91ece-111">Acessar as contas de usuários que têm associações no grupo com a coleção [Users](users-collection-adox.md).</span><span class="sxs-lookup"><span data-stu-id="91ece-111">Access the user accounts that have memberships in the group with the [Users](users-collection-adox.md) collection.</span></span>

  - <span data-ttu-id="91ece-112">Acessar propriedades específicas do provedor com a coleção [Properties](properties-collection-ado.md).</span><span class="sxs-lookup"><span data-stu-id="91ece-112">Access provider-specific properties with the [Properties](properties-collection-ado.md) collection.</span></span>

