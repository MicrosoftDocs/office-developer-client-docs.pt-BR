---
title: SaveOptionsEnum (referência do banco de dados de área de trabalho do Access)
TOCTitle: SaveOptionsEnum
ms:assetid: 2a4e4c7a-6331-7270-0514-cc549c721ffd
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249053(v=office.15)
ms:contentKeyID: 48543906
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 77a617dc54d8acd145648d926e10cf7c9a3cf252
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314739"
---
# <a name="saveoptionsenum"></a><span data-ttu-id="d3bd6-102">SaveOptionsEnum</span><span class="sxs-lookup"><span data-stu-id="d3bd6-102">SaveOptionsEnum</span></span>

<span data-ttu-id="d3bd6-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="d3bd6-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="d3bd6-p101">Especifica se um arquivo deveria ser criado ou sobregravado ao salvar a partir de um objeto [Stream](stream-object-ado.md). Os valores podem ser combinados com um operador AND.</span><span class="sxs-lookup"><span data-stu-id="d3bd6-p101">Specifies whether a file should be created or overwritten when saving from a [Stream](stream-object-ado.md) object. The values can be combined with an AND operator.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="d3bd6-106">Constant</span><span class="sxs-lookup"><span data-stu-id="d3bd6-106">Constant</span></span></p></th>
<th><p><span data-ttu-id="d3bd6-107">Valor</span><span class="sxs-lookup"><span data-stu-id="d3bd6-107">Value</span></span></p></th>
<th><p><span data-ttu-id="d3bd6-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="d3bd6-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d3bd6-109"><strong>adSaveCreateNotExist</strong></span><span class="sxs-lookup"><span data-stu-id="d3bd6-109"><strong>adSaveCreateNotExist</strong></span></span></p></td>
<td><p><span data-ttu-id="d3bd6-110">1</span><span class="sxs-lookup"><span data-stu-id="d3bd6-110">1</span></span></p></td>
<td><p><span data-ttu-id="d3bd6-p102">Padrão. Crie um novo arquivo se o arquivo especificado pelo parâmetro <em>FileName</em> ainda não existir.</span><span class="sxs-lookup"><span data-stu-id="d3bd6-p102">Default. Creates a new file if the file specified by the <em>FileName</em> parameter does not already exist.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d3bd6-113"><strong>adSaveCreateOverWrite</strong></span><span class="sxs-lookup"><span data-stu-id="d3bd6-113"><strong>adSaveCreateOverWrite</strong></span></span></p></td>
<td><p><span data-ttu-id="d3bd6-114">duas</span><span class="sxs-lookup"><span data-stu-id="d3bd6-114">2</span></span></p></td>
<td><p><span data-ttu-id="d3bd6-115">Sobregrava o arquivo com os dados a partir do objeto <strong>Stream</strong> aberto no momento se o arquivo especificado pelo parâmetro <em>Filename</em> já existir.</span><span class="sxs-lookup"><span data-stu-id="d3bd6-115">Overwrites the file with the data from the currently open <strong>Stream</strong> object, if the file specified by the <em>Filename</em> parameter already exists.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="d3bd6-116">Equivalente do ADO/WFC</span><span class="sxs-lookup"><span data-stu-id="d3bd6-116">ADO/WFC equivalent</span></span>

<span data-ttu-id="d3bd6-117">Essas constantes não têm ADO/WFC equivalentes.</span><span class="sxs-lookup"><span data-stu-id="d3bd6-117">These constants do not have ADO/WFC equivalents.</span></span>

