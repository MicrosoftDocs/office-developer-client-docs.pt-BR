---
title: Instrução de macro Grupo
TOCTitle: Group macro statement
ms:assetid: 42aa4afa-ab5d-9dcc-2182-786f025e316d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192918(v=office.15)
ms:contentKeyID: 48544481
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: c82169ac430496587c6ebab5e439d70bc9319b5e
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25930886"
---
# <a name="group-macro-statement"></a><span data-ttu-id="37067-102">Instrução de macro Grupo</span><span class="sxs-lookup"><span data-stu-id="37067-102">Group macro statement</span></span>


<span data-ttu-id="37067-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="37067-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="37067-104">A instrução **grupo** permite que você especifique um bloco de ações em uma macro que você pode expandir ou recolher.</span><span class="sxs-lookup"><span data-stu-id="37067-104">The **Group** statement enables you to specify a block of actions within a macro that you can expand or collapse.</span></span>

## <a name="setting"></a><span data-ttu-id="37067-105">Configuração</span><span class="sxs-lookup"><span data-stu-id="37067-105">Setting</span></span>

<span data-ttu-id="37067-106">A ação **Grupo** tem os seguintes argumentos.</span><span class="sxs-lookup"><span data-stu-id="37067-106">The **Group** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="37067-107">Argumento</span><span class="sxs-lookup"><span data-stu-id="37067-107">Argument</span></span></p></th>
<th><p><span data-ttu-id="37067-108">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="37067-108">Required</span></span></p></th>
<th><p><span data-ttu-id="37067-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="37067-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="37067-110"><strong>Descrição</strong></span><span class="sxs-lookup"><span data-stu-id="37067-110"><strong>Description</strong></span></span></p></td>
<td><p><span data-ttu-id="37067-111">Não</span><span class="sxs-lookup"><span data-stu-id="37067-111">No</span></span></p></td>
<td><p><span data-ttu-id="37067-112">Uma cadeia de caracteres que aparece como o título de um grupo quando ele é recolhido.</span><span class="sxs-lookup"><span data-stu-id="37067-112">A string that appears as the title of a group when it is collapsed.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="37067-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="37067-113">Remarks</span></span>

<span data-ttu-id="37067-p101">A instrução **Grupo** não define uma região de uma macro que pode ser executada separadamente. Use a instrução **[Submacro](submacro-macro-statement.md)** para definir um conjunto de ações que podem ser executadas separadamente na janela **Designer de Macros**.</span><span class="sxs-lookup"><span data-stu-id="37067-p101">The **Group** statment does not define a region of a macro that can be executed separately. Use the **[Submacro](submacro-macro-statement.md)** statment to define a set of actions to be executed separately in the **Macro Designer** window.</span></span>

