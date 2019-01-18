---
title: CopyRecordOptionsEnum
TOCTitle: CopyRecordOptionsEnum
ms:assetid: ab9426e9-0e4e-6c85-43cf-e4a205a7c4c0
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249795(v=office.15)
ms:contentKeyID: 48546975
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: eb1637d1757a8507c6b6abb2a0c71867e3d1177b
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28703843"
---
# <a name="copyrecordoptionsenum"></a><span data-ttu-id="c5296-102">CopyRecordOptionsEnum</span><span class="sxs-lookup"><span data-stu-id="c5296-102">CopyRecordOptionsEnum</span></span>


<span data-ttu-id="c5296-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="c5296-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="c5296-104">Especifica o comportamento do método [CopyRecord](copyrecord-method-ado.md).</span><span class="sxs-lookup"><span data-stu-id="c5296-104">Specifies the behavior of the [CopyRecord](copyrecord-method-ado.md) method.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="c5296-105">Constant</span><span class="sxs-lookup"><span data-stu-id="c5296-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="c5296-106">Valor</span><span class="sxs-lookup"><span data-stu-id="c5296-106">Value</span></span></p></th>
<th><p><span data-ttu-id="c5296-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="c5296-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c5296-108"><strong>adCopyAllowEmulation</strong></span><span class="sxs-lookup"><span data-stu-id="c5296-108"><strong>adCopyAllowEmulation</strong></span></span></p></td>
<td><p><span data-ttu-id="c5296-109">4</span><span class="sxs-lookup"><span data-stu-id="c5296-109">4</span></span></p></td>
<td><p><span data-ttu-id="c5296-p101">Indica que o provedor de <em>Origem</em> tenta simular a cópia usando as operações de download e upload se esse método falhar devido a um <em>Destino</em> estar em um servidor diferente ou se for atendido pro um provedor diferente da <em>Origem</em>. Observe que a diferenciação dos recursos do provedor pode dificulta o desempenho ou ocasionar perda de dados.</span><span class="sxs-lookup"><span data-stu-id="c5296-p101">Indicates that the <em>Source</em> provider attempts to simulate the copy using download and upload operations if this method fails due to <em>Destination</em> being on a different server or is serviced by a different provider than <em>Source</em>. Note that differing provider capabilities may hamper performance or lose data.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c5296-112"><strong>adCopyNonRecursive</strong></span><span class="sxs-lookup"><span data-stu-id="c5296-112"><strong>adCopyNonRecursive</strong></span></span></p></td>
<td><p><span data-ttu-id="c5296-113">2</span><span class="sxs-lookup"><span data-stu-id="c5296-113">2</span></span></p></td>
<td><p><span data-ttu-id="c5296-p102">Copia o diretório atual, mas nenhum dos seus subdiretórios, para o destino. A operação copiar não é recursiva.</span><span class="sxs-lookup"><span data-stu-id="c5296-p102">Copies the current directory, but none of its subdirectories, to the destination. The copy operation is not recursive.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c5296-116"><strong>adCopyOverWrite</strong></span><span class="sxs-lookup"><span data-stu-id="c5296-116"><strong>adCopyOverWrite</strong></span></span></p></td>
<td><p><span data-ttu-id="c5296-117">1</span><span class="sxs-lookup"><span data-stu-id="c5296-117">1</span></span></p></td>
<td><p><span data-ttu-id="c5296-118">Sobregrava o arquivo ou diretório se o <em>Destino</em> apontar para um arquivo ou diretório existente.</span><span class="sxs-lookup"><span data-stu-id="c5296-118">Overwrites the file or directory if the <em>Destination</em> points to an existing file or directory.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c5296-119"><strong>adCopyUnspecified</strong></span><span class="sxs-lookup"><span data-stu-id="c5296-119"><strong>adCopyUnspecified</strong></span></span></p></td>
<td><p><span data-ttu-id="c5296-120">-1</span><span class="sxs-lookup"><span data-stu-id="c5296-120">-1</span></span></p></td>
<td><p><span data-ttu-id="c5296-p103">Padrão. Executa a operação copiar padrão: A operação falha se o arquivo ou diretório de destino já existir e a operação fizer a cópia de maneira recursiva.</span><span class="sxs-lookup"><span data-stu-id="c5296-p103">Default. Performs the default copy operation: The operation fails if the destination file or directory already exists, and the operation copies recursively.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="c5296-123">Equivalente ADO/WFC</span><span class="sxs-lookup"><span data-stu-id="c5296-123">ADO/WFC equivalent</span></span>

<span data-ttu-id="c5296-124">Essas constantes não têm ADO/WFC equivalentes.</span><span class="sxs-lookup"><span data-stu-id="c5296-124">These constants do not have ADO/WFC equivalents.</span></span>

