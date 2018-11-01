---
title: Instrução ADD USER (Microsoft Access SQL)
TOCTitle: ADD USER statement (Microsoft Access SQL)
ms:assetid: 1feb631f-cb8c-14ae-6214-276f1faf1a55
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845862(v=office.15)
ms:contentKeyID: 48543652
ms.date: 10/18/2018
mtps_version: v=office.15
ms.openlocfilehash: 7a27874a7264258fee51f90fabaeecd180d7aeae
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25868606"
---
# <a name="add-user-statement-microsoft-access-sql"></a><span data-ttu-id="e5224-102">Instrução ADD USER (Microsoft Access SQL)</span><span class="sxs-lookup"><span data-stu-id="e5224-102">ADD USER statement (Microsoft Access SQL)</span></span>

<span data-ttu-id="e5224-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="e5224-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="e5224-104">Adiciona um ou vários *usuários* existentes em um *grupo* existente.</span><span class="sxs-lookup"><span data-stu-id="e5224-104">Adds one or more existing *user*s to an existing *group*.</span></span>

## <a name="syntax"></a><span data-ttu-id="e5224-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e5224-105">Syntax</span></span>

<span data-ttu-id="e5224-106">Adicionar usuário *usuário*\[, *usuário*,... \] Ao *grupo*</span><span class="sxs-lookup"><span data-stu-id="e5224-106">ADD USER *user*\[, *user*, …\] TO *group*</span></span>

<span data-ttu-id="e5224-107">A instrução ADD USER possui as seguintes partes:</span><span class="sxs-lookup"><span data-stu-id="e5224-107">The ADD USER statement has these parts:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="e5224-108">Parte</span><span class="sxs-lookup"><span data-stu-id="e5224-108">Part</span></span></p></th>
<th><p><span data-ttu-id="e5224-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="e5224-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e5224-110"><em>user</em></span><span class="sxs-lookup"><span data-stu-id="e5224-110"><em>user</em></span></span></p></td>
<td><p><span data-ttu-id="e5224-111">O nome de um usuário que será adicionado ao arquivo de informações do grupo de trabalho.</span><span class="sxs-lookup"><span data-stu-id="e5224-111">The name of a user to be added to the workgroup information file.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e5224-112"><em>group</em></span><span class="sxs-lookup"><span data-stu-id="e5224-112"><em>group</em></span></span></p></td>
<td><p><span data-ttu-id="e5224-113">O nome de um grupo a ser adicionado ao arquivo de informações do grupo de trabalho.</span><span class="sxs-lookup"><span data-stu-id="e5224-113">The name of a group to be added to the workgroup information file.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="e5224-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="e5224-114">Remarks</span></span>

<span data-ttu-id="e5224-115">Depois que um *usuário* tiver sido adicionado a um *grupo*, o *usuário* tem todas as permissões que tiverem sido concedidas ao *grupo*.</span><span class="sxs-lookup"><span data-stu-id="e5224-115">After a *user* had been added to a *group*, the *user* has all the permissions that have been granted to the *group*.</span></span>

