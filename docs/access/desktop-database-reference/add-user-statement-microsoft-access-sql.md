---
title: Instrução ADD USER (Microsoft Access SQL)
TOCTitle: ADD USER statement (Microsoft Access SQL)
ms:assetid: 1feb631f-cb8c-14ae-6214-276f1faf1a55
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845862(v=office.15)
ms:contentKeyID: 48543652
ms.date: 10/18/2018
mtps_version: v=office.15
ms.openlocfilehash: 80e3a8fe62cf077accfc18a30e188898fb279d1d
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25862286"
---
# <a name="add-user-statement-microsoft-access-sql"></a><span data-ttu-id="b9646-102">Instrução ADD USER (Microsoft Access SQL)</span><span class="sxs-lookup"><span data-stu-id="b9646-102">ADD USER statement (Microsoft Access SQL)</span></span>

<span data-ttu-id="b9646-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="b9646-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="b9646-104">Adiciona um ou vários *usuários* existentes em um *grupo* existente.</span><span class="sxs-lookup"><span data-stu-id="b9646-104">Adds one or more existing *user*s to an existing *group*.</span></span>

## <a name="syntax"></a><span data-ttu-id="b9646-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b9646-105">Syntax</span></span>

<span data-ttu-id="b9646-106">Adicionar usuário *usuário*\[, *usuário*,... \] Ao *grupo*</span><span class="sxs-lookup"><span data-stu-id="b9646-106">ADD USER *user*\[, *user*, …\] TO *group*</span></span>

<span data-ttu-id="b9646-107">A instrução ADD USER possui as seguintes partes:</span><span class="sxs-lookup"><span data-stu-id="b9646-107">The ADD USER statement has these parts:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b9646-108">Parte</span><span class="sxs-lookup"><span data-stu-id="b9646-108">Part</span></span></p></th>
<th><p><span data-ttu-id="b9646-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="b9646-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b9646-110"><em>user</em></span><span class="sxs-lookup"><span data-stu-id="b9646-110"><em>user</em></span></span></p></td>
<td><p><span data-ttu-id="b9646-111">O nome de um usuário que será adicionado ao arquivo de informações do grupo de trabalho.</span><span class="sxs-lookup"><span data-stu-id="b9646-111">The name of a user to be added to the workgroup information file.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b9646-112"><em>group</em></span><span class="sxs-lookup"><span data-stu-id="b9646-112"><em>group</em></span></span></p></td>
<td><p><span data-ttu-id="b9646-113">O nome de um grupo a ser adicionado ao arquivo de informações do grupo de trabalho.</span><span class="sxs-lookup"><span data-stu-id="b9646-113">The name of a group to be added to the workgroup information file.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="b9646-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="b9646-114">Remarks</span></span>

<span data-ttu-id="b9646-115">Depois que um *usuário* tiver sido adicionado a um *grupo*, o *usuário* tem todas as permissões que tiverem sido concedidas ao *grupo*.</span><span class="sxs-lookup"><span data-stu-id="b9646-115">After a *user* had been added to a *group*, the *user* has all the permissions that have been granted to the *group*.</span></span>

