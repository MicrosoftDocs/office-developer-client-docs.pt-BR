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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32280422"
---
# <a name="add-user-statement-microsoft-access-sql"></a><span data-ttu-id="28639-102">Instrução ADD USER (Microsoft Access SQL)</span><span class="sxs-lookup"><span data-stu-id="28639-102">ADD USER statement (Microsoft Access SQL)</span></span>

<span data-ttu-id="28639-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="28639-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="28639-104">Adiciona um ou vários *usuários* existentes em um *grupo* existente.</span><span class="sxs-lookup"><span data-stu-id="28639-104">Adds one or more existing *user*s to an existing *group*.</span></span>

## <a name="syntax"></a><span data-ttu-id="28639-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="28639-105">Syntax</span></span>

<span data-ttu-id="28639-106">Adicionar *usuário*\[, *usuário*,... \] Para *Agrupar*</span><span class="sxs-lookup"><span data-stu-id="28639-106">ADD USER *user*\[, *user*, …\] TO *group*</span></span>

<span data-ttu-id="28639-107">A instrução ADD USER possui as seguintes partes:</span><span class="sxs-lookup"><span data-stu-id="28639-107">The ADD USER statement has these parts:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="28639-108">Parte</span><span class="sxs-lookup"><span data-stu-id="28639-108">Part</span></span></p></th>
<th><p><span data-ttu-id="28639-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="28639-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="28639-110"><em>usuário</em></span><span class="sxs-lookup"><span data-stu-id="28639-110"><em>user</em></span></span></p></td>
<td><p><span data-ttu-id="28639-111">O nome de um usuário a ser adicionado ao arquivo de informações do grupo de trabalho.</span><span class="sxs-lookup"><span data-stu-id="28639-111">The name of a user to be added to the workgroup information file.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="28639-112"><em>grupo</em></span><span class="sxs-lookup"><span data-stu-id="28639-112"><em>group</em></span></span></p></td>
<td><p><span data-ttu-id="28639-113">O nome de um grupo a ser adicionado ao arquivo de informações do grupo de trabalho.</span><span class="sxs-lookup"><span data-stu-id="28639-113">The name of a group to be added to the workgroup information file.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="28639-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="28639-114">Remarks</span></span>

<span data-ttu-id="28639-115">Depois que um *usuário* tiver sido adicionado a um *grupo*, o *usuário* terá todas as permissões concedidas ao *grupo*.</span><span class="sxs-lookup"><span data-stu-id="28639-115">After a *user* had been added to a *group*, the *user* has all the permissions that have been granted to the *group*.</span></span>

