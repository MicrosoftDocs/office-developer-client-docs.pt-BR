---
title: MoveRecordOptionsEnum
TOCTitle: MoveRecordOptionsEnum
ms:assetid: 2785bca0-777c-a802-51d7-6f5cf0fb4210
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249039(v=office.15)
ms:contentKeyID: 48543842
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: fc621f620a7d55571aa55296a4d294fff9566bf5
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25862237"
---
# <a name="moverecordoptionsenum"></a><span data-ttu-id="88688-102">MoveRecordOptionsEnum</span><span class="sxs-lookup"><span data-stu-id="88688-102">MoveRecordOptionsEnum</span></span>


<span data-ttu-id="88688-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="88688-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="88688-104">Especifica o comportamento do objeto [Record](record-object-ado.md) do método [MoveRecord](moverecord-method-ado.md).</span><span class="sxs-lookup"><span data-stu-id="88688-104">Specifies the behavior of the [Record](record-object-ado.md) object [MoveRecord](moverecord-method-ado.md) method.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="88688-105">Constant</span><span class="sxs-lookup"><span data-stu-id="88688-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="88688-106">Valor</span><span class="sxs-lookup"><span data-stu-id="88688-106">Value</span></span></p></th>
<th><p><span data-ttu-id="88688-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="88688-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="88688-108"><strong>adMoveUnspecified</strong></span><span class="sxs-lookup"><span data-stu-id="88688-108"><strong>adMoveUnspecified</strong></span></span></p></td>
<td><p><span data-ttu-id="88688-109">-1</span><span class="sxs-lookup"><span data-stu-id="88688-109">-1</span></span></p></td>
<td><p><span data-ttu-id="88688-p101">Padrão. Executa a operação mover padrão: A operação falha se o arquivo ou diretório de destino já existir e a operação atualizar links de hipertexto.</span><span class="sxs-lookup"><span data-stu-id="88688-p101">Default. Performs the default move operation: The operation fails if the destination file or directory already exists, and the operation updates hypertext links.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="88688-112"><strong>adMoveOverWrite</strong></span><span class="sxs-lookup"><span data-stu-id="88688-112"><strong>adMoveOverWrite</strong></span></span></p></td>
<td><p><span data-ttu-id="88688-113">1</span><span class="sxs-lookup"><span data-stu-id="88688-113">1</span></span></p></td>
<td><p><span data-ttu-id="88688-114">Sobregrava o arquivo ou diretório de destino, mesmo se ele já existir.</span><span class="sxs-lookup"><span data-stu-id="88688-114">Overwrites the destination file or directory, even if it already exists.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="88688-115"><strong>adMoveDontUpdateLinks</strong></span><span class="sxs-lookup"><span data-stu-id="88688-115"><strong>adMoveDontUpdateLinks</strong></span></span></p></td>
<td><p><span data-ttu-id="88688-116">2</span><span class="sxs-lookup"><span data-stu-id="88688-116">2</span></span></p></td>
<td><p><span data-ttu-id="88688-p102">Modifica o comportamento padrão do método <strong>MoveRecord</strong> por não atualizar os links de hipertexto do <strong>Record</strong> de origem. O comportamento padrão depende dos recursos do provedor. A operação mover atualiza os links se o provedor tiver recursos. Se ele não puder consertar os links ou se este valor não for especificado, a operação mover terá êxito mesmo que os links não sejam consertados.</span><span class="sxs-lookup"><span data-stu-id="88688-p102">Modifies the default behavior of <strong>MoveRecord</strong> method by not updating the hypertext links of the source <strong>Record</strong>. The default behavior depends on the capabilities of the provider. Move operation updates links if the provider is capable. If the provider cannot fix links or if this value is not specified, then the move succeeds even when links have not been fixed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="88688-121"><strong>adMoveAllowEmulation</strong></span><span class="sxs-lookup"><span data-stu-id="88688-121"><strong>adMoveAllowEmulation</strong></span></span></p></td>
<td><p><span data-ttu-id="88688-122">4</span><span class="sxs-lookup"><span data-stu-id="88688-122">4</span></span></p></td>
<td><p><span data-ttu-id="88688-p103">Solicita que o provedor tente simular a operação mover (usando as operações download, upload e excluir). Se a tentativa de mover o <strong>Record</strong> falhar porque o URL de destino está em um servidor diferente ou está sendo atendido por um provedor diferente da origem, isso poderá causar um aumento na latência ou a perda de dados, devido aos recursos diferentes do provedor ao mover os recursos entre os provedores.</span><span class="sxs-lookup"><span data-stu-id="88688-p103">Requests that the provider attempt to simulate the move (using download, upload, and delete operations). If the attempt to move the <strong>Record</strong> fails because the destination URL is on a different server or serviced by a different provider than the source, this may cause increased latency or data loss, due to different provider capabilities when moving resources between providers.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="88688-125">Equivalente ADO/WFC</span><span class="sxs-lookup"><span data-stu-id="88688-125">ADO/WFC equivalent</span></span>

<span data-ttu-id="88688-126">Essas constantes não têm ADO/WFC equivalentes.</span><span class="sxs-lookup"><span data-stu-id="88688-126">These constants do not have ADO/WFC equivalents.</span></span>

