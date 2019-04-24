---
title: Instrução de macro Grupo
TOCTitle: Group macro statement
ms:assetid: 42aa4afa-ab5d-9dcc-2182-786f025e316d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192918(v=office.15)
ms:contentKeyID: 48544481
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 2dc25621a49d8fd23078a926d6ec6c5de54e54d9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292108"
---
# <a name="group-macro-statement"></a><span data-ttu-id="36ac2-102">Instrução de macro Grupo</span><span class="sxs-lookup"><span data-stu-id="36ac2-102">Group macro statement</span></span>


<span data-ttu-id="36ac2-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="36ac2-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="36ac2-104">A instrução **Group** permite que você especifique um bloco de ações em uma macro que você pode expandir ou recolher.</span><span class="sxs-lookup"><span data-stu-id="36ac2-104">The **Group** statement enables you to specify a block of actions within a macro that you can expand or collapse.</span></span>

## <a name="setting"></a><span data-ttu-id="36ac2-105">Configuração</span><span class="sxs-lookup"><span data-stu-id="36ac2-105">Setting</span></span>

<span data-ttu-id="36ac2-106">A ação **Grupo** tem os seguintes argumentos.</span><span class="sxs-lookup"><span data-stu-id="36ac2-106">The **Group** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="36ac2-107">Argument</span><span class="sxs-lookup"><span data-stu-id="36ac2-107">Argument</span></span></p></th>
<th><p><span data-ttu-id="36ac2-108">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="36ac2-108">Required</span></span></p></th>
<th><p><span data-ttu-id="36ac2-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="36ac2-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="36ac2-110"><strong>Descrição</strong></span><span class="sxs-lookup"><span data-stu-id="36ac2-110"><strong>Description</strong></span></span></p></td>
<td><p><span data-ttu-id="36ac2-111">Não</span><span class="sxs-lookup"><span data-stu-id="36ac2-111">No</span></span></p></td>
<td><p><span data-ttu-id="36ac2-112">Uma cadeia de caracteres que aparece como o título de um grupo quando ele é recolhido.</span><span class="sxs-lookup"><span data-stu-id="36ac2-112">A string that appears as the title of a group when it is collapsed.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="36ac2-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="36ac2-113">Remarks</span></span>

<span data-ttu-id="36ac2-p101">A instrução **Grupo** não define uma região de uma macro que pode ser executada separadamente. Use a instrução **[Submacro](submacro-macro-statement.md)** para definir um conjunto de ações que podem ser executadas separadamente na janela **Designer de Macros**.</span><span class="sxs-lookup"><span data-stu-id="36ac2-p101">The **Group** statment does not define a region of a macro that can be executed separately. Use the **[Submacro](submacro-macro-statement.md)** statment to define a set of actions to be executed separately in the **Macro Designer** window.</span></span>

