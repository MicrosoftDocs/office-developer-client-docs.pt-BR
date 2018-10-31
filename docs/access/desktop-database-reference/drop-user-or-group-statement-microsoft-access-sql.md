---
title: Instrução DROP USER ou GROUP (Microsoft Access SQL)
TOCTitle: DROP USER or GROUP statement (Microsoft Access SQL)
ms:assetid: 46bc5916-556b-17df-2f4c-8fd7bbd21ef7
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193192(v=office.15)
ms:contentKeyID: 48544575
ms.date: 10/18/2018
mtps_version: v=office.15
ms.openlocfilehash: a7988a2124af13dc84cefe678342da969e349a06
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25864016"
---
# <a name="drop-user-or-group-statement-microsoft-access-sql"></a><span data-ttu-id="6c638-102">Instrução DROP USER ou GROUP (Microsoft Access SQL)</span><span class="sxs-lookup"><span data-stu-id="6c638-102">DROP USER or GROUP statement (Microsoft Access SQL)</span></span>

<span data-ttu-id="6c638-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="6c638-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="6c638-104">Exclui um ou mais existentes *usuários* ou *grupos*ou remove um ou mais *usuários* existentes de um *grupo*de existente.</span><span class="sxs-lookup"><span data-stu-id="6c638-104">Deletes one or more existing *users* or *groups*, or removes one or more existing *users* from an existing *group*.</span></span>

## <a name="syntax"></a><span data-ttu-id="6c638-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6c638-105">Syntax</span></span>

<span data-ttu-id="6c638-106">**Excluir um ou mais _usuários_ ou remover um ou mais _usuários_ de um _grupo_**:</span><span class="sxs-lookup"><span data-stu-id="6c638-106">**Delete one or more _users_ or remove one or more _users_ from a _group_**:</span></span>

<span data-ttu-id="6c638-107">DROP USER *usuário*\[, *usuário*,... \] \[De *grupo*\]</span><span class="sxs-lookup"><span data-stu-id="6c638-107">DROP USER *user*\[, *user*, …\] \[FROM *group*\]</span></span>

<span data-ttu-id="6c638-108">**Excluir um ou mais _grupos_**:</span><span class="sxs-lookup"><span data-stu-id="6c638-108">**Delete one or more _groups_**:</span></span>

<span data-ttu-id="6c638-109">DROP GROUP *grupo*\[, *grupo*,...\]</span><span class="sxs-lookup"><span data-stu-id="6c638-109">DROP GROUP *group*\[, *group*, …\]</span></span>

<span data-ttu-id="6c638-110">A instrução DROP USER ou GROUP tem estas partes:</span><span class="sxs-lookup"><span data-stu-id="6c638-110">The DROP USER or GROUP statement has these parts:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="6c638-111">Parte</span><span class="sxs-lookup"><span data-stu-id="6c638-111">Part</span></span></p></th>
<th><p><span data-ttu-id="6c638-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="6c638-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6c638-113"><em>user</em></span><span class="sxs-lookup"><span data-stu-id="6c638-113"><em>user</em></span></span></p></td>
<td><p><span data-ttu-id="6c638-114">O nome de um usuário a ser removido do arquivo de informações do grupo de trabalho.</span><span class="sxs-lookup"><span data-stu-id="6c638-114">The name of a user to be removed from the workgroup information file.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6c638-115"><em>group</em></span><span class="sxs-lookup"><span data-stu-id="6c638-115"><em>group</em></span></span></p></td>
<td><p><span data-ttu-id="6c638-116">O nome de um grupo a ser removido do arquivo de informações do grupo de trabalho.</span><span class="sxs-lookup"><span data-stu-id="6c638-116">The name of a group to be removed from the workgroup information file.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="6c638-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="6c638-117">Remarks</span></span>

<span data-ttu-id="6c638-118">Se a palavra-chave FROM for usada na instrução DROP USER, cada um dos *usuários* listados na instrução será removido do *grupo* especificado após a palavra-chave FROM.</span><span class="sxs-lookup"><span data-stu-id="6c638-118">If the FROM keyword is used in the DROP USER statement, each of the *users* listed in the statement will be removed from the *group* specified following the FROM keyword.</span></span> <span data-ttu-id="6c638-119">No entanto, os *usuários* sozinhos não serão excluídos.</span><span class="sxs-lookup"><span data-stu-id="6c638-119">However, the *users* themselves will not be deleted.</span></span>

<span data-ttu-id="6c638-120">A instrução DROP GROUP excluirá o *grupo*especificado (s).</span><span class="sxs-lookup"><span data-stu-id="6c638-120">The DROP GROUP statement will delete the specified *group*(s).</span></span> <span data-ttu-id="6c638-121">Os *usuários* que são membros do *grupo*(s) não serão afetados, mas eles deixará de ser membros do *grupo*excluído (s).</span><span class="sxs-lookup"><span data-stu-id="6c638-121">The *users* who are members of the *group*(s) will not be affected, but they will no longer be members of the deleted *group*(s).</span></span>

