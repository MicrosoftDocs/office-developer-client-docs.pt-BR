---
title: StreamReadEnum (referência do banco de dados da área de trabalho do Access)
TOCTitle: StreamReadEnum
ms:assetid: 12432c0d-dc2e-10ea-13db-0c07b6ba29bc
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248895(v=office.15)
ms:contentKeyID: 48543336
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: e4d9c96a7bb34fe0ab3512a316a92e1f7a01ef4b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314718"
---
# <a name="streamreadenum"></a><span data-ttu-id="f039e-102">StreamReadEnum</span><span class="sxs-lookup"><span data-stu-id="f039e-102">StreamReadEnum</span></span>

<span data-ttu-id="f039e-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="f039e-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="f039e-104">Especifica se o fluxo inteiro ou a próxima linha deve ser lido a partir de um objeto [Stream](stream-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="f039e-104">Specifies whether the whole stream or the next line should be read from a [Stream](stream-object-ado.md) object.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="f039e-105">Constant</span><span class="sxs-lookup"><span data-stu-id="f039e-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="f039e-106">Valor</span><span class="sxs-lookup"><span data-stu-id="f039e-106">Value</span></span></p></th>
<th><p><span data-ttu-id="f039e-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="f039e-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f039e-108"><strong>adReadAll</strong></span><span class="sxs-lookup"><span data-stu-id="f039e-108"><strong>adReadAll</strong></span></span></p></td>
<td><p><span data-ttu-id="f039e-109">-1</span><span class="sxs-lookup"><span data-stu-id="f039e-109">-1</span></span></p></td>
<td><p><span data-ttu-id="f039e-p101">Padrão. Lê todos os bytes do fluxo, a partir da posição atual em diante até o marcador <a href="eos-property-ado.md">EOS</a>. Este é o único valor <strong>StreamReadEnum</strong> válido com fluxos binários (<a href="type-property-ado-stream.md">Type</a> é <strong>adTypeBinary</strong>).</span><span class="sxs-lookup"><span data-stu-id="f039e-p101">Default. Reads all bytes from the stream, from the current position onwards to the <a href="eos-property-ado.md">EOS</a> marker. This is the only valid <strong>StreamReadEnum</strong> value with binary streams (<a href="type-property-ado-stream.md">Type</a> is <strong>adTypeBinary</strong>).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f039e-113"><strong>adReadLine</strong></span><span class="sxs-lookup"><span data-stu-id="f039e-113"><strong>adReadLine</strong></span></span></p></td>
<td><p><span data-ttu-id="f039e-114">-2</span><span class="sxs-lookup"><span data-stu-id="f039e-114">-2</span></span></p></td>
<td><p><span data-ttu-id="f039e-115">Lê a próxima linha a partir do fluxo (projetado pela propriedade <a href="lineseparator-property-ado.md">LineSeparator</a>).</span><span class="sxs-lookup"><span data-stu-id="f039e-115">Reads the next line from the stream (designated by the <a href="lineseparator-property-ado.md">LineSeparator</a> property).</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="f039e-116">Equivalente do ADO/WFC</span><span class="sxs-lookup"><span data-stu-id="f039e-116">ADO/WFC equivalent</span></span>

<span data-ttu-id="f039e-117">Essas constantes não têm ADO/WFC equivalentes.</span><span class="sxs-lookup"><span data-stu-id="f039e-117">These constants do not have ADO/WFC equivalents.</span></span>

