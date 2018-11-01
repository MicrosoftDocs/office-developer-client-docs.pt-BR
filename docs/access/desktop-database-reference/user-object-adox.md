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
# <a name="user-object-adox"></a><span data-ttu-id="cae63-102">Objeto User (ADOX)</span><span class="sxs-lookup"><span data-stu-id="cae63-102">User Object (ADOX)</span></span>


<span data-ttu-id="cae63-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="cae63-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="cae63-104">Representa uma conta de usuário que tem permissões de acesso em um banco de dados protegido.</span><span class="sxs-lookup"><span data-stu-id="cae63-104">Represents a user account that has access permissions within a secured database.</span></span>

## <a name="remarks"></a><span data-ttu-id="cae63-105">Comentários</span><span class="sxs-lookup"><span data-stu-id="cae63-105">Remarks</span></span>

<span data-ttu-id="cae63-p101">A coleção [Users](users-collection-adox.md) de um [Catálogo](catalog-object-adox.md) representa todos os usuários do catálogo. A coleção **Users** de um [Grupo](group-object-adox.md) representa apenas os usuários do grupo específico.</span><span class="sxs-lookup"><span data-stu-id="cae63-p101">The [Users](users-collection-adox.md) collection of a [Catalog](catalog-object-adox.md) represents all the catalog's users. The **Users** collection for a [Group](group-object-adox.md) represents only the users of the specific group.</span></span>

<span data-ttu-id="cae63-108">Com as propriedades, as coleções e os métodos de um objeto **User**, você pode:</span><span class="sxs-lookup"><span data-stu-id="cae63-108">With the properties, collections, and methods of a **User** object, you can:</span></span>

  - <span data-ttu-id="cae63-109">Identificar o usuário com a propriedade [Name](name-property-adox.md).</span><span class="sxs-lookup"><span data-stu-id="cae63-109">Identify the user with the [Name](name-property-adox.md) property.</span></span>

  - <span data-ttu-id="cae63-110">Alterar a senha de um usuário com o método [ChangePassword](changepassword-method-adox.md).</span><span class="sxs-lookup"><span data-stu-id="cae63-110">Change the password for a user with the [ChangePassword](changepassword-method-adox.md) method.</span></span>

  - <span data-ttu-id="cae63-111">Determinar se um usuário tem permissões de leitura, gravação ou exclusão com os métodos [GetPermissions](getpermissions-method-adox.md) e [SetPermissions](setpermissions-method-adox.md).</span><span class="sxs-lookup"><span data-stu-id="cae63-111">Determine whether a user has read, write, or delete permissions with the [GetPermissions](getpermissions-method-adox.md) and [SetPermissions](setpermissions-method-adox.md) methods.</span></span>

  - <span data-ttu-id="cae63-112">Acessar os grupos aos quais um usuário pertence com a coleção [Groups](groups-collection-adox.md).</span><span class="sxs-lookup"><span data-stu-id="cae63-112">Access the groups to which a user belongs with the [Groups](groups-collection-adox.md) collection.</span></span>

  - <span data-ttu-id="cae63-113">Acessar propriedades específicas do provedor com a coleção [Properties](properties-collection-ado.md).</span><span class="sxs-lookup"><span data-stu-id="cae63-113">Access provider-specific properties with the [Properties](properties-collection-ado.md) collection.</span></span>

