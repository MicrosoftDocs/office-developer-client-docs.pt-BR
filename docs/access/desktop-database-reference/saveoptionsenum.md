---
title: SaveOptionsEnum (referência de banco de dados da área de trabalho do Access)
TOCTitle: SaveOptionsEnum
ms:assetid: 2a4e4c7a-6331-7270-0514-cc549c721ffd
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249053(v=office.15)
ms:contentKeyID: 48543906
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 68526eca205fb41dd2789ec187514d0f9b11e35f
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25462876"
---
# <a name="saveoptionsenum"></a><span data-ttu-id="f571e-102">SaveOptionsEnum</span><span class="sxs-lookup"><span data-stu-id="f571e-102">SaveOptionsEnum</span></span>


<span data-ttu-id="f571e-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="f571e-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="f571e-p101">Especifica se um arquivo deveria ser criado ou sobregravado ao salvar a partir de um objeto [Stream](stream-object-ado.md). Os valores podem ser combinados com um operador AND.</span><span class="sxs-lookup"><span data-stu-id="f571e-p101">Specifies whether a file should be created or overwritten when saving from a [Stream](stream-object-ado.md) object. The values can be combined with an AND operator.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="f571e-106">Constant</span><span class="sxs-lookup"><span data-stu-id="f571e-106">Constant</span></span></p></th>
<th><p><span data-ttu-id="f571e-107">Valor</span><span class="sxs-lookup"><span data-stu-id="f571e-107">Value</span></span></p></th>
<th><p><span data-ttu-id="f571e-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="f571e-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f571e-109"><strong>adSaveCreateNotExist</strong></span><span class="sxs-lookup"><span data-stu-id="f571e-109"><strong>adSaveCreateNotExist</strong></span></span></p></td>
<td><p><span data-ttu-id="f571e-110">1</span><span class="sxs-lookup"><span data-stu-id="f571e-110">1</span></span></p></td>
<td><p><span data-ttu-id="f571e-p102">Padrão. Crie um novo arquivo se o arquivo especificado pelo parâmetro <em>FileName</em> ainda não existir.</span><span class="sxs-lookup"><span data-stu-id="f571e-p102">Default. Creates a new file if the file specified by the <em>FileName</em> parameter does not already exist.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f571e-113"><strong>adSaveCreateOverWrite</strong></span><span class="sxs-lookup"><span data-stu-id="f571e-113"><strong>adSaveCreateOverWrite</strong></span></span></p></td>
<td><p><span data-ttu-id="f571e-114">2</span><span class="sxs-lookup"><span data-stu-id="f571e-114">2</span></span></p></td>
<td><p><span data-ttu-id="f571e-115">Sobregrava o arquivo com os dados a partir do objeto <strong>Stream</strong> aberto no momento se o arquivo especificado pelo parâmetro <em>Filename</em> já existir.</span><span class="sxs-lookup"><span data-stu-id="f571e-115">Overwrites the file with the data from the currently open <strong>Stream</strong> object, if the file specified by the <em>Filename</em> parameter already exists.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="f571e-116">**ADO/WFC Equivalente**</span><span class="sxs-lookup"><span data-stu-id="f571e-116">**ADO/WFC Equivalent**</span></span>

<span data-ttu-id="f571e-117">Essas constantes não têm ADO/WFC equivalentes.</span><span class="sxs-lookup"><span data-stu-id="f571e-117">These constants do not have ADO/WFC equivalents.</span></span>

