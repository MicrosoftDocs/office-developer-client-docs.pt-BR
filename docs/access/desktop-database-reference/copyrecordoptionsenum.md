---
title: CopyRecordOptionsEnum
TOCTitle: CopyRecordOptionsEnum
ms:assetid: ab9426e9-0e4e-6c85-43cf-e4a205a7c4c0
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249795(v=office.15)
ms:contentKeyID: 48546975
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: b33347492562d868781e8bbca346918d55ed597b
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25860277"
---
# <a name="copyrecordoptionsenum"></a><span data-ttu-id="e993e-102">CopyRecordOptionsEnum</span><span class="sxs-lookup"><span data-stu-id="e993e-102">CopyRecordOptionsEnum</span></span>


<span data-ttu-id="e993e-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="e993e-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="e993e-104">Especifica o comportamento do método [CopyRecord](copyrecord-method-ado.md).</span><span class="sxs-lookup"><span data-stu-id="e993e-104">Specifies the behavior of the [CopyRecord](copyrecord-method-ado.md) method.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="e993e-105">Constant</span><span class="sxs-lookup"><span data-stu-id="e993e-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="e993e-106">Valor</span><span class="sxs-lookup"><span data-stu-id="e993e-106">Value</span></span></p></th>
<th><p><span data-ttu-id="e993e-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="e993e-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e993e-108"><strong>adCopyAllowEmulation</strong></span><span class="sxs-lookup"><span data-stu-id="e993e-108"><strong>adCopyAllowEmulation</strong></span></span></p></td>
<td><p><span data-ttu-id="e993e-109">4</span><span class="sxs-lookup"><span data-stu-id="e993e-109">4</span></span></p></td>
<td><p><span data-ttu-id="e993e-p101">Indica que o provedor de <em>Origem</em> tenta simular a cópia usando as operações de download e upload se esse método falhar devido a um <em>Destino</em> estar em um servidor diferente ou se for atendido pro um provedor diferente da <em>Origem</em>. Observe que a diferenciação dos recursos do provedor pode dificulta o desempenho ou ocasionar perda de dados.</span><span class="sxs-lookup"><span data-stu-id="e993e-p101">Indicates that the <em>Source</em> provider attempts to simulate the copy using download and upload operations if this method fails due to <em>Destination</em> being on a different server or is serviced by a different provider than <em>Source</em>. Note that differing provider capabilities may hamper performance or lose data.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e993e-112"><strong>adCopyNonRecursive</strong></span><span class="sxs-lookup"><span data-stu-id="e993e-112"><strong>adCopyNonRecursive</strong></span></span></p></td>
<td><p><span data-ttu-id="e993e-113">2</span><span class="sxs-lookup"><span data-stu-id="e993e-113">2</span></span></p></td>
<td><p><span data-ttu-id="e993e-p102">Copia o diretório atual, mas nenhum dos seus subdiretórios, para o destino. A operação copiar não é recursiva.</span><span class="sxs-lookup"><span data-stu-id="e993e-p102">Copies the current directory, but none of its subdirectories, to the destination. The copy operation is not recursive.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e993e-116"><strong>adCopyOverWrite</strong></span><span class="sxs-lookup"><span data-stu-id="e993e-116"><strong>adCopyOverWrite</strong></span></span></p></td>
<td><p><span data-ttu-id="e993e-117">1</span><span class="sxs-lookup"><span data-stu-id="e993e-117">1</span></span></p></td>
<td><p><span data-ttu-id="e993e-118">Sobregrava o arquivo ou diretório se o <em>Destino</em> apontar para um arquivo ou diretório existente.</span><span class="sxs-lookup"><span data-stu-id="e993e-118">Overwrites the file or directory if the <em>Destination</em> points to an existing file or directory.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e993e-119"><strong>adCopyUnspecified</strong></span><span class="sxs-lookup"><span data-stu-id="e993e-119"><strong>adCopyUnspecified</strong></span></span></p></td>
<td><p><span data-ttu-id="e993e-120">-1</span><span class="sxs-lookup"><span data-stu-id="e993e-120">-1</span></span></p></td>
<td><p><span data-ttu-id="e993e-p103">Padrão. Executa a operação copiar padrão: A operação falha se o arquivo ou diretório de destino já existir e a operação fizer a cópia de maneira recursiva.</span><span class="sxs-lookup"><span data-stu-id="e993e-p103">Default. Performs the default copy operation: The operation fails if the destination file or directory already exists, and the operation copies recursively.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="e993e-123">Equivalente ADO/WFC</span><span class="sxs-lookup"><span data-stu-id="e993e-123">ADO/WFC equivalent</span></span>

<span data-ttu-id="e993e-124">Essas constantes não têm ADO/WFC equivalentes.</span><span class="sxs-lookup"><span data-stu-id="e993e-124">These constants do not have ADO/WFC equivalents.</span></span>

