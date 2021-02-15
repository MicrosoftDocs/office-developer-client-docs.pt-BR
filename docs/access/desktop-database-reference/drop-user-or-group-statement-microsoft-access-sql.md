---
title: Instrução DROP USER ou GROUP (Microsoft Access SQL)
TOCTitle: DROP USER or GROUP statement (Microsoft Access SQL)
ms:assetid: 46bc5916-556b-17df-2f4c-8fd7bbd21ef7
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193192(v=office.15)
ms:contentKeyID: 48544575
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 995f935ceea5af3b740215c5a4137e02e7ebb1b2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293641"
---
# <a name="drop-user-or-group-statement-microsoft-access-sql"></a><span data-ttu-id="ab5cc-102">Instrução DROP USER ou GROUP (Microsoft Access SQL)</span><span class="sxs-lookup"><span data-stu-id="ab5cc-102">DROP USER or GROUP statement (Microsoft Access SQL)</span></span>

<span data-ttu-id="ab5cc-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="ab5cc-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="ab5cc-104">Exclui um ou mais usuários *ou* grupos existentes *ou* remove um ou mais usuários *existentes* de um grupo *existente.*</span><span class="sxs-lookup"><span data-stu-id="ab5cc-104">Deletes one or more existing *users* or *groups*, or removes one or more existing *users* from an existing *group*.</span></span>

## <a name="syntax"></a><span data-ttu-id="ab5cc-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ab5cc-105">Syntax</span></span>

### <a name="delete-one-or-more-users-or-remove-one-or-more-users-from-a-group"></a><span data-ttu-id="ab5cc-106">Excluir um ou mais usuários ou remover um ou mais usuários de um grupo</span><span class="sxs-lookup"><span data-stu-id="ab5cc-106">Delete one or more users or remove one or more users from a group</span></span>

<span data-ttu-id="ab5cc-107">DROP USER *user,* \[ *user*, ... \] \[ Grupo  FROM\]</span><span class="sxs-lookup"><span data-stu-id="ab5cc-107">DROP USER *user*\[, *user*, …\] \[FROM *group*\]</span></span>

### <a name="delete-one-or-more-groups"></a><span data-ttu-id="ab5cc-108">Excluir um ou mais grupos</span><span class="sxs-lookup"><span data-stu-id="ab5cc-108">Delete one or more groups</span></span>

<span data-ttu-id="ab5cc-109">DROP GROUP *group* \[ , *group*, ...\]</span><span class="sxs-lookup"><span data-stu-id="ab5cc-109">DROP GROUP *group*\[, *group*, …\]</span></span>

<span data-ttu-id="ab5cc-110">A instrução DROP USER ou GROUP tem estas partes:</span><span class="sxs-lookup"><span data-stu-id="ab5cc-110">The DROP USER or GROUP statement has these parts:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="ab5cc-111">Sair</span><span class="sxs-lookup"><span data-stu-id="ab5cc-111">Part</span></span></p></th>
<th><p><span data-ttu-id="ab5cc-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="ab5cc-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ab5cc-113"><em>user</em></span><span class="sxs-lookup"><span data-stu-id="ab5cc-113"><em>user</em></span></span></p></td>
<td><p><span data-ttu-id="ab5cc-114">O nome de um usuário a ser removido do arquivo de informações do grupo de trabalho.</span><span class="sxs-lookup"><span data-stu-id="ab5cc-114">The name of a user to be removed from the workgroup information file.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ab5cc-115"><em>group</em></span><span class="sxs-lookup"><span data-stu-id="ab5cc-115"><em>group</em></span></span></p></td>
<td><p><span data-ttu-id="ab5cc-116">O nome de um grupo a ser removido do arquivo de informações do grupo de trabalho.</span><span class="sxs-lookup"><span data-stu-id="ab5cc-116">The name of a group to be removed from the workgroup information file.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="ab5cc-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="ab5cc-117">Remarks</span></span>

<span data-ttu-id="ab5cc-118">Se a palavra-chave FROM for usada na  instrução DROP USER, cada  um dos usuários listados na instrução será removido do grupo especificado após a palavra-chave FROM.</span><span class="sxs-lookup"><span data-stu-id="ab5cc-118">If the FROM keyword is used in the DROP USER statement, each of the *users* listed in the statement will be removed from the *group* specified following the FROM keyword.</span></span> <span data-ttu-id="ab5cc-119">No entanto, *os próprios* usuários não serão excluídos.</span><span class="sxs-lookup"><span data-stu-id="ab5cc-119">However, the *users* themselves will not be deleted.</span></span>

<span data-ttu-id="ab5cc-120">A instrução DROP GROUP excluirá o(s) *grupo*(s) especificado(s).</span><span class="sxs-lookup"><span data-stu-id="ab5cc-120">The DROP GROUP statement will delete the specified *group*(s).</span></span> <span data-ttu-id="ab5cc-121">Os *usuários* que são membros *do*(s) grupo(s) não serão afetados, mas eles não serão mais membros *do(s)* grupo(s) excluído(s).</span><span class="sxs-lookup"><span data-stu-id="ab5cc-121">The *users* who are members of the *group*(s) will not be affected, but they will no longer be members of the deleted *group*(s).</span></span>

