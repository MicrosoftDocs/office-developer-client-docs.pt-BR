---
title: ActionEnum (referência de banco de dados da área de trabalho do Access)
TOCTitle: ActionEnum
ms:assetid: 225024c1-9088-b532-2a23-04c1aaaaa892
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248998(v=office.15)
ms:contentKeyID: 48543704
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: af0e5fd734c03b88990383b99815d6e35f2c1290
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25462405"
---
# <a name="actionenum"></a><span data-ttu-id="b88af-102">ActionEnum</span><span class="sxs-lookup"><span data-stu-id="b88af-102">ActionEnum</span></span>


<span data-ttu-id="b88af-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="b88af-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="b88af-104">Especifica o tipo de ação a ser executada quando [SetPermissions](setpermissions-method-adox.md) é chamado.</span><span class="sxs-lookup"><span data-stu-id="b88af-104">Specifies the type of action to be performed when [SetPermissions](setpermissions-method-adox.md) is called.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b88af-105">Constant</span><span class="sxs-lookup"><span data-stu-id="b88af-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="b88af-106">Valor</span><span class="sxs-lookup"><span data-stu-id="b88af-106">Value</span></span></p></th>
<th><p><span data-ttu-id="b88af-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="b88af-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b88af-108"><strong>adAccessDeny</strong></span><span class="sxs-lookup"><span data-stu-id="b88af-108"><strong>adAccessDeny</strong></span></span></p></td>
<td><p><span data-ttu-id="b88af-109">3</span><span class="sxs-lookup"><span data-stu-id="b88af-109">3</span></span></p></td>
<td><p><span data-ttu-id="b88af-110">As permissões especificadas serão negadas ao grupo ou usuário.</span><span class="sxs-lookup"><span data-stu-id="b88af-110">The group or user will be denied the specified permissions.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b88af-111"><strong>adAccessGrant</strong></span><span class="sxs-lookup"><span data-stu-id="b88af-111"><strong>adAccessGrant</strong></span></span></p></td>
<td><p><span data-ttu-id="b88af-112">1</span><span class="sxs-lookup"><span data-stu-id="b88af-112">1</span></span></p></td>
<td><p><span data-ttu-id="b88af-113">O grupo ou usuário terá, pelo menos, as permissões solicitadas.</span><span class="sxs-lookup"><span data-stu-id="b88af-113">The group or user will have at least the requested permissions.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b88af-114"><strong>adAccessRevoke</strong></span><span class="sxs-lookup"><span data-stu-id="b88af-114"><strong>adAccessRevoke</strong></span></span></p></td>
<td><p><span data-ttu-id="b88af-115">4</span><span class="sxs-lookup"><span data-stu-id="b88af-115">4</span></span></p></td>
<td><p><span data-ttu-id="b88af-116">Serão revogados todos os direitos de acesso explícitos do grupo ou do usuário.</span><span class="sxs-lookup"><span data-stu-id="b88af-116">Any explicit access rights the group or user has will be revoked.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b88af-117"><strong>adAccessSet</strong></span><span class="sxs-lookup"><span data-stu-id="b88af-117"><strong>adAccessSet</strong></span></span></p></td>
<td><p><span data-ttu-id="b88af-118">2</span><span class="sxs-lookup"><span data-stu-id="b88af-118">2</span></span></p></td>
<td><p><span data-ttu-id="b88af-119">O grupo ou usuário terá exatamente as permissões solicitadas.</span><span class="sxs-lookup"><span data-stu-id="b88af-119">The group or user will have exactly the requested permissions.</span></span></p></td>
</tr>
</tbody>
</table>

