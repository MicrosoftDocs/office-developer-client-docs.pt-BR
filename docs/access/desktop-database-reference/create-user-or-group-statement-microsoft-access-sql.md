---
title: Instrução CREATE USER ou GROUP (Microsoft Access SQL)
TOCTitle: CREATE USER or GROUP statement (Microsoft Access SQL)
ms:assetid: 62148ce2-0f81-944e-a1ab-edef990fff9f
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194914(v=office.15)
ms:contentKeyID: 48545229
ms.date: 10/18/2018
mtps_version: v=office.15
ms.openlocfilehash: 52d376b05c195ed0ea4707e849c5ae395c2b5590
ms.sourcegitcommit: 38d0db57580cc5f4a0231c27b1643f8db5431ca3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25936823"
---
# <a name="create-user-or-group-statement-microsoft-access-sql"></a><span data-ttu-id="9ffdd-102">Instrução CREATE USER ou GROUP (Microsoft Access SQL)</span><span class="sxs-lookup"><span data-stu-id="9ffdd-102">CREATE USER or GROUP statement (Microsoft Access SQL)</span></span>

<span data-ttu-id="9ffdd-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="9ffdd-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="9ffdd-104">Cria um ou mais usuários ou grupos novos.</span><span class="sxs-lookup"><span data-stu-id="9ffdd-104">Creates one or more new users or groups.</span></span>

## <a name="syntax"></a><span data-ttu-id="9ffdd-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9ffdd-105">Syntax</span></span>

### <a name="create-a-user"></a><span data-ttu-id="9ffdd-106">Criar um usuário</span><span class="sxs-lookup"><span data-stu-id="9ffdd-106">Create a user</span></span>

<span data-ttu-id="9ffdd-107">CREATE USER *usuário* *senha pid* \[, *usuário* *senha pid*,...\]</span><span class="sxs-lookup"><span data-stu-id="9ffdd-107">CREATE USER *user* *password pid* \[, *user* *password pid*, …\]</span></span>

### <a name="create-a-group"></a><span data-ttu-id="9ffdd-108">Criar um grupo</span><span class="sxs-lookup"><span data-stu-id="9ffdd-108">Create a group</span></span>

<span data-ttu-id="9ffdd-109">Criar grupo *grupo* *pid*\[, *grupo* *pid*, …\]</span><span class="sxs-lookup"><span data-stu-id="9ffdd-109">CREATE GROUP *group* *pid*\[, *group* *pid*, …\]</span></span>

<span data-ttu-id="9ffdd-110">A instrução CREATE USER ou GROUP tem estas partes:</span><span class="sxs-lookup"><span data-stu-id="9ffdd-110">The CREATE USER or GROUP statement has these parts:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="9ffdd-111">Parte</span><span class="sxs-lookup"><span data-stu-id="9ffdd-111">Part</span></span></p></th>
<th><p><span data-ttu-id="9ffdd-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="9ffdd-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9ffdd-113"><em>user</em></span><span class="sxs-lookup"><span data-stu-id="9ffdd-113"><em>user</em></span></span></p></td>
<td><p><span data-ttu-id="9ffdd-114">O nome de um usuário que será adicionado ao arquivo de informações do grupo de trabalho.</span><span class="sxs-lookup"><span data-stu-id="9ffdd-114">The name of a user to be added to the workgroup information file.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9ffdd-115"><em>group</em></span><span class="sxs-lookup"><span data-stu-id="9ffdd-115"><em>group</em></span></span></p></td>
<td><p><span data-ttu-id="9ffdd-116">O nome de um grupo a ser adicionado ao arquivo de informações do grupo de trabalho.</span><span class="sxs-lookup"><span data-stu-id="9ffdd-116">The name of a group to be added to the workgroup information file.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9ffdd-117"><em>password</em></span><span class="sxs-lookup"><span data-stu-id="9ffdd-117"><em>password</em></span></span></p></td>
<td><p><span data-ttu-id="9ffdd-118">A senha a ser associada ao nome de <em>usuário</em> especificado.</span><span class="sxs-lookup"><span data-stu-id="9ffdd-118">The password to be associated with the specified <em>user</em> name.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9ffdd-119"><em>pid</em></span><span class="sxs-lookup"><span data-stu-id="9ffdd-119"><em>pid</em></span></span></p></td>
<td><p><span data-ttu-id="9ffdd-120">A identificação pessoal.</span><span class="sxs-lookup"><span data-stu-id="9ffdd-120">The personal id.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="9ffdd-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="9ffdd-121">Remarks</span></span>

<span data-ttu-id="9ffdd-122">Um *usuário* e um *grupo* não podem ter o mesmo nome.</span><span class="sxs-lookup"><span data-stu-id="9ffdd-122">A *user* and a *group* cannot have the same name.</span></span>

<span data-ttu-id="9ffdd-123">Uma *senha* é necessária para cada *usuário* ou *grupo* que é criado.</span><span class="sxs-lookup"><span data-stu-id="9ffdd-123">A *password* is required for each *user* or *group* that is created.</span></span>

