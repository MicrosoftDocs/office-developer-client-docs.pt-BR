---
title: Instrução ADD USER (Microsoft Access SQL)
TOCTitle: ADD USER statement (Microsoft Access SQL)
ms:assetid: 1feb631f-cb8c-14ae-6214-276f1faf1a55
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845862(v=office.15)
ms:contentKeyID: 48543652
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 8ba60a646fd234748bcc39b9a5604a33675caee5
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28705390"
---
# <a name="add-user-statement-microsoft-access-sql"></a><span data-ttu-id="a618a-102">Instrução ADD USER (Microsoft Access SQL)</span><span class="sxs-lookup"><span data-stu-id="a618a-102">ADD USER statement (Microsoft Access SQL)</span></span>

<span data-ttu-id="a618a-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="a618a-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="a618a-104">Adiciona um ou vários *usuários* existentes em um *grupo* existente.</span><span class="sxs-lookup"><span data-stu-id="a618a-104">Adds one or more existing *user*s to an existing *group*.</span></span>

## <a name="syntax"></a><span data-ttu-id="a618a-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a618a-105">Syntax</span></span>

<span data-ttu-id="a618a-106">Adicionar usuário *usuário*\[, *usuário*,... \] Ao *grupo*</span><span class="sxs-lookup"><span data-stu-id="a618a-106">ADD USER *user*\[, *user*, …\] TO *group*</span></span>

<span data-ttu-id="a618a-107">A instrução ADD USER possui as seguintes partes:</span><span class="sxs-lookup"><span data-stu-id="a618a-107">The ADD USER statement has these parts:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a618a-108">Parte</span><span class="sxs-lookup"><span data-stu-id="a618a-108">Part</span></span></p></th>
<th><p><span data-ttu-id="a618a-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="a618a-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a618a-110"><em>user</em></span><span class="sxs-lookup"><span data-stu-id="a618a-110"><em>user</em></span></span></p></td>
<td><p><span data-ttu-id="a618a-111">O nome de um usuário que será adicionado ao arquivo de informações do grupo de trabalho.</span><span class="sxs-lookup"><span data-stu-id="a618a-111">The name of a user to be added to the workgroup information file.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a618a-112"><em>grupo</em></span><span class="sxs-lookup"><span data-stu-id="a618a-112"><em>group</em></span></span></p></td>
<td><p><span data-ttu-id="a618a-113">O nome de um grupo a ser adicionado ao arquivo de informações do grupo de trabalho.</span><span class="sxs-lookup"><span data-stu-id="a618a-113">The name of a group to be added to the workgroup information file.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="a618a-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="a618a-114">Remarks</span></span>

<span data-ttu-id="a618a-115">Depois que um *usuário* tiver sido adicionado a um *grupo*, o *usuário* tem todas as permissões que tiverem sido concedidas ao *grupo*.</span><span class="sxs-lookup"><span data-stu-id="a618a-115">After a *user* had been added to a *group*, the *user* has all the permissions that have been granted to the *group*.</span></span>

