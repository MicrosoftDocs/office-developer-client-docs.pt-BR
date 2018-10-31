---
title: SaveOptionsEnum (referência de banco de dados da área de trabalho do Access)
TOCTitle: SaveOptionsEnum
ms:assetid: 2a4e4c7a-6331-7270-0514-cc549c721ffd
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249053(v=office.15)
ms:contentKeyID: 48543906
ms.date: 10/18/2018
mtps_version: v=office.15
ms.openlocfilehash: ffd37090b264e434b5fd3750f474122f8da4bfbb
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25861901"
---
# <a name="saveoptionsenum"></a><span data-ttu-id="8912d-102">SaveOptionsEnum</span><span class="sxs-lookup"><span data-stu-id="8912d-102">SaveOptionsEnum</span></span>

<span data-ttu-id="8912d-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="8912d-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="8912d-p101">Especifica se um arquivo deveria ser criado ou sobregravado ao salvar a partir de um objeto [Stream](stream-object-ado.md). Os valores podem ser combinados com um operador AND.</span><span class="sxs-lookup"><span data-stu-id="8912d-p101">Specifies whether a file should be created or overwritten when saving from a [Stream](stream-object-ado.md) object. The values can be combined with an AND operator.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="8912d-106">Constant</span><span class="sxs-lookup"><span data-stu-id="8912d-106">Constant</span></span></p></th>
<th><p><span data-ttu-id="8912d-107">Valor</span><span class="sxs-lookup"><span data-stu-id="8912d-107">Value</span></span></p></th>
<th><p><span data-ttu-id="8912d-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="8912d-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8912d-109"><strong>adSaveCreateNotExist</strong></span><span class="sxs-lookup"><span data-stu-id="8912d-109"><strong>adSaveCreateNotExist</strong></span></span></p></td>
<td><p><span data-ttu-id="8912d-110">1</span><span class="sxs-lookup"><span data-stu-id="8912d-110">1</span></span></p></td>
<td><p><span data-ttu-id="8912d-p102">Padrão. Crie um novo arquivo se o arquivo especificado pelo parâmetro <em>FileName</em> ainda não existir.</span><span class="sxs-lookup"><span data-stu-id="8912d-p102">Default. Creates a new file if the file specified by the <em>FileName</em> parameter does not already exist.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8912d-113"><strong>adSaveCreateOverWrite</strong></span><span class="sxs-lookup"><span data-stu-id="8912d-113"><strong>adSaveCreateOverWrite</strong></span></span></p></td>
<td><p><span data-ttu-id="8912d-114">2</span><span class="sxs-lookup"><span data-stu-id="8912d-114">2</span></span></p></td>
<td><p><span data-ttu-id="8912d-115">Sobregrava o arquivo com os dados a partir do objeto <strong>Stream</strong> aberto no momento se o arquivo especificado pelo parâmetro <em>Filename</em> já existir.</span><span class="sxs-lookup"><span data-stu-id="8912d-115">Overwrites the file with the data from the currently open <strong>Stream</strong> object, if the file specified by the <em>Filename</em> parameter already exists.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="8912d-116">Equivalente ADO/WFC</span><span class="sxs-lookup"><span data-stu-id="8912d-116">ADO/WFC equivalent</span></span>

<span data-ttu-id="8912d-117">Essas constantes não têm ADO/WFC equivalentes.</span><span class="sxs-lookup"><span data-stu-id="8912d-117">These constants do not have ADO/WFC equivalents.</span></span>

