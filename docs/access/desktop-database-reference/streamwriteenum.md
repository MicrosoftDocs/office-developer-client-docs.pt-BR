---
title: StreamWriteEnum (referência de banco de dados da área de trabalho do Access)
TOCTitle: StreamWriteEnum
ms:assetid: b4356999-d7a8-abfa-f6a8-6c2dd04b9257
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249861(v=office.15)
ms:contentKeyID: 48547216
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 87144e5409fb54cf0cb8f59ad4d593ab05d694a4
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28706167"
---
# <a name="streamwriteenum"></a><span data-ttu-id="44147-102">StreamWriteEnum</span><span class="sxs-lookup"><span data-stu-id="44147-102">StreamWriteEnum</span></span>

<span data-ttu-id="44147-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="44147-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="44147-104">Especifica se um separador de linha está anexado à string gravada em um objeto [Stream](stream-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="44147-104">Specifies whether a line separator is appended to the string written to a [Stream](stream-object-ado.md) object.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="44147-105">Constant</span><span class="sxs-lookup"><span data-stu-id="44147-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="44147-106">Valor</span><span class="sxs-lookup"><span data-stu-id="44147-106">Value</span></span></p></th>
<th><p><span data-ttu-id="44147-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="44147-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="44147-108"><strong>adWriteChar</strong></span><span class="sxs-lookup"><span data-stu-id="44147-108"><strong>adWriteChar</strong></span></span></p></td>
<td><p><span data-ttu-id="44147-109">0</span><span class="sxs-lookup"><span data-stu-id="44147-109">0</span></span></p></td>
<td><p><span data-ttu-id="44147-p101">Padrão. Grava a sequência de texto especificada (especificada por parâmetro <em>Data</em>) no objeto <strong>Stream</strong>.</span><span class="sxs-lookup"><span data-stu-id="44147-p101">Default. Writes the specified text string (specified by the <em>Data</em> parameter) to the <strong>Stream</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="44147-112"><strong>adWriteLine</strong></span><span class="sxs-lookup"><span data-stu-id="44147-112"><strong>adWriteLine</strong></span></span></p></td>
<td><p><span data-ttu-id="44147-113">1</span><span class="sxs-lookup"><span data-stu-id="44147-113">1</span></span></p></td>
<td><p><span data-ttu-id="44147-p102">Grava uma sequência de texto e um caractere de separador de linha em um objeto <strong>Stream</strong>. Se a propriedade <a href="lineseparator-property-ado.md">LineSeparator</a> não for definida, retornará um erro em tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="44147-p102">Writes a text string and a line separator character to a <strong>Stream</strong> object. If the <a href="lineseparator-property-ado.md">LineSeparator</a> property is not defined, then this returns a run-time error.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="44147-116">Equivalente ADO/WFC</span><span class="sxs-lookup"><span data-stu-id="44147-116">ADO/WFC equivalent</span></span>

<span data-ttu-id="44147-117">Essas constantes não têm ADO/WFC equivalentes.</span><span class="sxs-lookup"><span data-stu-id="44147-117">These constants do not have ADO/WFC equivalents.</span></span>

