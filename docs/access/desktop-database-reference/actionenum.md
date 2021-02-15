---
title: ActionEnum (referência do banco de dados da área de trabalho do Access)
TOCTitle: ActionEnum
ms:assetid: 225024c1-9088-b532-2a23-04c1aaaaa892
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248998(v=office.15)
ms:contentKeyID: 48543704
ms.date: 10/17/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: f098adb42df39d1509a6d22decd8d2cead684f11
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32280653"
---
# <a name="actionenum"></a><span data-ttu-id="fa12b-102">ActionEnum</span><span class="sxs-lookup"><span data-stu-id="fa12b-102">ActionEnum</span></span>

<span data-ttu-id="fa12b-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="fa12b-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="fa12b-104">Especifica o tipo de ação a ser executada quando [SetPermissions](setpermissions-method-adox.md) é chamado.</span><span class="sxs-lookup"><span data-stu-id="fa12b-104">Specifies the type of action to be performed when [SetPermissions](setpermissions-method-adox.md) is called.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="fa12b-105">Constant</span><span class="sxs-lookup"><span data-stu-id="fa12b-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="fa12b-106">Valor</span><span class="sxs-lookup"><span data-stu-id="fa12b-106">Value</span></span></p></th>
<th><p><span data-ttu-id="fa12b-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="fa12b-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="fa12b-108"><strong>adAccessDeny</strong></span><span class="sxs-lookup"><span data-stu-id="fa12b-108"><strong>adAccessDeny</strong></span></span></p></td>
<td><p><span data-ttu-id="fa12b-109">3 </span><span class="sxs-lookup"><span data-stu-id="fa12b-109">3</span></span></p></td>
<td><p><span data-ttu-id="fa12b-110">As permissões especificadas serão negadas ao grupo ou usuário.</span><span class="sxs-lookup"><span data-stu-id="fa12b-110">The group or user will be denied the specified permissions.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fa12b-111"><strong>adAccessGrant</strong></span><span class="sxs-lookup"><span data-stu-id="fa12b-111"><strong>adAccessGrant</strong></span></span></p></td>
<td><p><span data-ttu-id="fa12b-112">1 </span><span class="sxs-lookup"><span data-stu-id="fa12b-112">1</span></span></p></td>
<td><p><span data-ttu-id="fa12b-113">O grupo ou usuário terá, pelo menos, as permissões solicitadas.</span><span class="sxs-lookup"><span data-stu-id="fa12b-113">The group or user will have at least the requested permissions.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fa12b-114"><strong>adAccessRevoke</strong></span><span class="sxs-lookup"><span data-stu-id="fa12b-114"><strong>adAccessRevoke</strong></span></span></p></td>
<td><p><span data-ttu-id="fa12b-115">4 </span><span class="sxs-lookup"><span data-stu-id="fa12b-115">4</span></span></p></td>
<td><p><span data-ttu-id="fa12b-116">Serão revogados todos os direitos de acesso explícitos do grupo ou do usuário.</span><span class="sxs-lookup"><span data-stu-id="fa12b-116">Any explicit access rights the group or user has will be revoked.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fa12b-117"><strong>adAccessSet</strong></span><span class="sxs-lookup"><span data-stu-id="fa12b-117"><strong>adAccessSet</strong></span></span></p></td>
<td><p><span data-ttu-id="fa12b-118">2 </span><span class="sxs-lookup"><span data-stu-id="fa12b-118">2</span></span></p></td>
<td><p><span data-ttu-id="fa12b-119">O grupo ou usuário terá exatamente as permissões solicitadas.</span><span class="sxs-lookup"><span data-stu-id="fa12b-119">The group or user will have exactly the requested permissions.</span></span></p></td>
</tr>
</tbody>
</table>

