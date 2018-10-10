---
title: Instrução de macro Grupo
TOCTitle: Group Macro Statement
ms:assetid: 42aa4afa-ab5d-9dcc-2182-786f025e316d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192918(v=office.15)
ms:contentKeyID: 48544481
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 189744d228db0dadd3260ce77457daf8724828f8
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25463452"
---
# <a name="group-macro-statement"></a><span data-ttu-id="f0077-102">Instrução de macro Grupo</span><span class="sxs-lookup"><span data-stu-id="f0077-102">Group Macro Statement</span></span>


<span data-ttu-id="f0077-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="f0077-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="f0077-104">A instrução **grupo** permite que você especifique um bloco de ações em uma macro que você pode expandir ou recolher.</span><span class="sxs-lookup"><span data-stu-id="f0077-104">The **Group** statement enables you to specify a block of actions within a macro that you can expand or collapse.</span></span>

## <a name="setting"></a><span data-ttu-id="f0077-105">Configuração</span><span class="sxs-lookup"><span data-stu-id="f0077-105">Setting</span></span>

<span data-ttu-id="f0077-106">A ação **Grupo** tem os seguintes argumentos.</span><span class="sxs-lookup"><span data-stu-id="f0077-106">The **Group** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="f0077-107">Argumento</span><span class="sxs-lookup"><span data-stu-id="f0077-107">Argument</span></span></p></th>
<th><p><span data-ttu-id="f0077-108">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="f0077-108">Required</span></span></p></th>
<th><p><span data-ttu-id="f0077-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="f0077-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f0077-110"><strong>Descrição</strong></span><span class="sxs-lookup"><span data-stu-id="f0077-110"><strong>Description</strong></span></span></p></td>
<td><p><span data-ttu-id="f0077-111">Não</span><span class="sxs-lookup"><span data-stu-id="f0077-111">No</span></span></p></td>
<td><p><span data-ttu-id="f0077-112">Uma cadeia de caracteres que aparece como o título de um grupo quando ele é recolhido.</span><span class="sxs-lookup"><span data-stu-id="f0077-112">A string that appears as the title of a group when it is collapsed.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="f0077-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="f0077-113">Remarks</span></span>

<span data-ttu-id="f0077-p101">A instrução **Grupo** não define uma região de uma macro que pode ser executada separadamente. Use a instrução **[Submacro](submacro-macro-statement.md)** para definir um conjunto de ações que podem ser executadas separadamente na janela **Designer de Macros**.</span><span class="sxs-lookup"><span data-stu-id="f0077-p101">The **Group** statment does not define a region of a macro that can be executed separately. Use the **[Submacro](submacro-macro-statement.md)** statment to define a set of actions to be executed separately in the **Macro Designer** window.</span></span>

