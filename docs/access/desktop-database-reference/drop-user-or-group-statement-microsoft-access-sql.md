---
title: Instrução DROP USER ou GROUP (Microsoft Access SQL)
TOCTitle: DROP USER or GROUP Statement (Microsoft Access SQL)
ms:assetid: 46bc5916-556b-17df-2f4c-8fd7bbd21ef7
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193192(v=office.15)
ms:contentKeyID: 48544575
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 3a5cf75de06c13e2452e5f33b8355b7fb480d8a3
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25462482"
---
# <a name="drop-user-or-group-statement-microsoft-access-sql"></a><span data-ttu-id="e6478-102">Instrução DROP USER ou GROUP (Microsoft Access SQL)</span><span class="sxs-lookup"><span data-stu-id="e6478-102">DROP USER or GROUP Statement (Microsoft Access SQL)</span></span>


<span data-ttu-id="e6478-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="e6478-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="e6478-104">Exclui um ou mais *usuários* ou *grupos* ou remove um ou mais *usuários* existentes de um *grupo* existente.</span><span class="sxs-lookup"><span data-stu-id="e6478-104">Deletes one or more existing *user*s or *group*s, or removes one or more existing *user*s from an existing *group*.</span></span>

## <a name="syntax"></a><span data-ttu-id="e6478-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e6478-105">Syntax</span></span>

<span data-ttu-id="e6478-106">Excluir um ou mais *usuários* ou remover um ou mais *usuários* de um *grupo*:</span><span class="sxs-lookup"><span data-stu-id="e6478-106">Delete one or more *user*s or remove one or more *user*s from a *group*:</span></span>

<span data-ttu-id="e6478-107">DROP USER *usuário*\[, *usuário*,... \] \[De *grupo*\]</span><span class="sxs-lookup"><span data-stu-id="e6478-107">DROP USER *user*\[, *user*, …\] \[FROM *group*\]</span></span>

<span data-ttu-id="e6478-108">Excluir um ou mais *grupos*:</span><span class="sxs-lookup"><span data-stu-id="e6478-108">Delete one or more *group*s:</span></span>

<span data-ttu-id="e6478-109">DROP GROUP *grupo*\[, *grupo*,...\]</span><span class="sxs-lookup"><span data-stu-id="e6478-109">DROP GROUP *group*\[, *group*, …\]</span></span>

<span data-ttu-id="e6478-110">A instrução DROP USER ou GROUP tem estas partes:</span><span class="sxs-lookup"><span data-stu-id="e6478-110">The DROP USER or GROUP statement has these parts:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="e6478-111">Parte</span><span class="sxs-lookup"><span data-stu-id="e6478-111">Part</span></span></p></th>
<th><p><span data-ttu-id="e6478-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="e6478-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e6478-113"><em>user</em></span><span class="sxs-lookup"><span data-stu-id="e6478-113"><em>user</em></span></span></p></td>
<td><p><span data-ttu-id="e6478-114">O nome de um usuário a ser removido do arquivo de informações do grupo de trabalho.</span><span class="sxs-lookup"><span data-stu-id="e6478-114">The name of a user to be removed from the workgroup information file.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e6478-115"><em>group</em></span><span class="sxs-lookup"><span data-stu-id="e6478-115"><em>group</em></span></span></p></td>
<td><p><span data-ttu-id="e6478-116">O nome de um grupo a ser removido do arquivo de informações do grupo de trabalho.</span><span class="sxs-lookup"><span data-stu-id="e6478-116">The name of a group to be removed from the workgroup information file.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="e6478-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="e6478-117">Remarks</span></span>

<span data-ttu-id="e6478-p101">Se a palavra-chave FROM for utilizada na instrução DROP USER, cada um dos *usuários* listados na instrução será removido do *grupo* especificado, seguinte à palavra-chave FROM. Entretanto, os próprios *usuários* não serão excluídos.</span><span class="sxs-lookup"><span data-stu-id="e6478-p101">If the FROM keyword is used in the DROP USER statement, then each of the *user*s listed in the statement will be removed from the *group* specified following the FROM keyword. However, the *user*s themselves will not be deleted.</span></span>

<span data-ttu-id="e6478-p102">A instrução DROP GROUP excluirá o(s) *grupo*(s) especificado(s). Os *usuários* que são membros do(s) *grupo*(s) não serão afetados, mas eles não serão mais membros do(s) *grupo*(s) excluídos.</span><span class="sxs-lookup"><span data-stu-id="e6478-p102">The DROP GROUP statement will delete the specified *group*(s). The *user*s who are members of the *group*(s) will not be affected, but they will no longer be members of the deleted *group*(s).</span></span>

