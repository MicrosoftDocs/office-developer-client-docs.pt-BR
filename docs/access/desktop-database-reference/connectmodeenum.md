---
title: ConnectModeEnum (referência de banco de dados da área de trabalho do Access)
TOCTitle: ConnectModeEnum
ms:assetid: a15aa733-f899-5fe9-e705-67a4301706d1
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249743(v=office.15)
ms:contentKeyID: 48546728
ms.date: 10/18/2018
mtps_version: v=office.15
ms.openlocfilehash: 91d1ad892557ad944dca175a3589a74e7205ad01
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25862573"
---
# <a name="connectmodeenum"></a><span data-ttu-id="45431-102">ConnectModeEnum</span><span class="sxs-lookup"><span data-stu-id="45431-102">ConnectModeEnum</span></span>

<span data-ttu-id="45431-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="45431-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="45431-104">Especifica as permissões disponíveis para modificar os dados em uma [Connection](connection-object-ado.md), abrir um [Record](record-object-ado.md) ou especificar os valores para a propriedade [Mode](mode-property-ado.md) dos objetos **Record** e [Stream](stream-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="45431-104">Specifies the available permissions for modifying data in a [Connection](connection-object-ado.md), opening a [Record](record-object-ado.md), or specifying values for the [Mode](mode-property-ado.md) property of the **Record** and [Stream](stream-object-ado.md) objects.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="45431-105">Constant</span><span class="sxs-lookup"><span data-stu-id="45431-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="45431-106">Valor</span><span class="sxs-lookup"><span data-stu-id="45431-106">Value</span></span></p></th>
<th><p><span data-ttu-id="45431-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="45431-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="45431-108"><strong>adModeRead</strong></span><span class="sxs-lookup"><span data-stu-id="45431-108"><strong>adModeRead</strong></span></span></p></td>
<td><p><span data-ttu-id="45431-109">1</span><span class="sxs-lookup"><span data-stu-id="45431-109">1</span></span></p></td>
<td><p><span data-ttu-id="45431-110">Indica permissões somente leitura.</span><span class="sxs-lookup"><span data-stu-id="45431-110">Indicates read-only permissions.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="45431-111"><strong>adModeReadWrite</strong></span><span class="sxs-lookup"><span data-stu-id="45431-111"><strong>adModeReadWrite</strong></span></span></p></td>
<td><p><span data-ttu-id="45431-112">3</span><span class="sxs-lookup"><span data-stu-id="45431-112">3</span></span></p></td>
<td><p><span data-ttu-id="45431-113">Indica permissões de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="45431-113">Indicates read/write permissions.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="45431-114"><strong>adModeRecursive</strong></span><span class="sxs-lookup"><span data-stu-id="45431-114"><strong>adModeRecursive</strong></span></span></p></td>
<td><p><span data-ttu-id="45431-115">0x400000</span><span class="sxs-lookup"><span data-stu-id="45431-115">0x400000</span></span></p></td>
<td><p><span data-ttu-id="45431-116">Usado em conjunto com os outros valores <em>*ShareDeny*</em> (<strong>adModeShareDenyNone</strong>, <strong>adModeShareDenyWrite</strong>ou <strong>adModeShareDenyRead</strong>) para propagar as restrições de compartilhamento para todos os registros de subsites do <strong>registro</strong>atual.</span><span class="sxs-lookup"><span data-stu-id="45431-116">Used in conjunction with the other <em>*ShareDeny*</em> values (<strong>adModeShareDenyNone</strong>, <strong>adModeShareDenyWrite</strong>, or <strong>adModeShareDenyRead</strong>) to propagate sharing restrictions to all sub-records of the current <strong>Record</strong>.</span></span> <span data-ttu-id="45431-117">Ele não terá efeito se o <strong>registro</strong> não tiver nenhum filho.</span><span class="sxs-lookup"><span data-stu-id="45431-117">It has no affect if the <strong>Record</strong> does not have any children.</span></span></p><p><span data-ttu-id="45431-118">Um erro em tempo de execução é gerado se ele é usado com <strong>adModeShareDenyNone</strong> somente.</span><span class="sxs-lookup"><span data-stu-id="45431-118">A run-time error is generated if it is used with <strong>adModeShareDenyNone</strong> only.</span></span> <span data-ttu-id="45431-119">No entanto, ele pode ser usado com <strong>adModeShareDenyNone</strong> quando combinado com outros valores.</span><span class="sxs-lookup"><span data-stu-id="45431-119">However, it can be used with <strong>adModeShareDenyNone</strong> when combined with other values.</span></span> <span data-ttu-id="45431-120">Por exemplo, você pode usar &quot; <strong>adModeRead</strong> ou <strong>adModeShareDenyNone</strong> ou <strong>adModeRecursive</strong>&quot;.</span><span class="sxs-lookup"><span data-stu-id="45431-120">For example, you can use &quot;<strong>adModeRead</strong> or <strong>adModeShareDenyNone</strong> or <strong>adModeRecursive</strong>&quot;.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="45431-121"><strong>adModeShareDenyNone</strong></span><span class="sxs-lookup"><span data-stu-id="45431-121"><strong>adModeShareDenyNone</strong></span></span></p></td>
<td><p><span data-ttu-id="45431-122">16</span><span class="sxs-lookup"><span data-stu-id="45431-122">16</span></span></p></td>
<td><p><span data-ttu-id="45431-p103">Permite que outras pessoas estabeleçam uma conexão com quaisquer permissões. Não pode ser negado a terceiros acesso de leitura nem de gravação.</span><span class="sxs-lookup"><span data-stu-id="45431-p103">Allows others to open a connection with any permissions. Neither read nor write access can be denied to others.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="45431-125"><strong>adModeShareDenyRead</strong></span><span class="sxs-lookup"><span data-stu-id="45431-125"><strong>adModeShareDenyRead</strong></span></span></p></td>
<td><p><span data-ttu-id="45431-126">4</span><span class="sxs-lookup"><span data-stu-id="45431-126">4</span></span></p></td>
<td><p><span data-ttu-id="45431-127">Impede que outras pessoas estabeleçam uma conexão com permissões de leitura.</span><span class="sxs-lookup"><span data-stu-id="45431-127">Prevents others from opening a connection with read permissions.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="45431-128"><strong>adModeShareDenyWrite</strong></span><span class="sxs-lookup"><span data-stu-id="45431-128"><strong>adModeShareDenyWrite</strong></span></span></p></td>
<td><p><span data-ttu-id="45431-129">8</span><span class="sxs-lookup"><span data-stu-id="45431-129">8</span></span></p></td>
<td><p><span data-ttu-id="45431-130">Impede que outras pessoas estabeleçam uma conexão com permissões de gravação.</span><span class="sxs-lookup"><span data-stu-id="45431-130">Prevents others from opening a connection with write permissions.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="45431-131"><strong>adModeShareExclusive</strong></span><span class="sxs-lookup"><span data-stu-id="45431-131"><strong>adModeShareExclusive</strong></span></span></p></td>
<td><p><span data-ttu-id="45431-132">12</span><span class="sxs-lookup"><span data-stu-id="45431-132">12</span></span></p></td>
<td><p><span data-ttu-id="45431-133">Impede que outras pessoas estabeleçam uma conexão.</span><span class="sxs-lookup"><span data-stu-id="45431-133">Prevents others from opening a connection.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="45431-134"><strong>adModeUnknown</strong></span><span class="sxs-lookup"><span data-stu-id="45431-134"><strong>adModeUnknown</strong></span></span></p></td>
<td><p><span data-ttu-id="45431-135">0</span><span class="sxs-lookup"><span data-stu-id="45431-135">0</span></span></p></td>
<td><p><span data-ttu-id="45431-p104">Padrão. Indica que as permissões ainda não foram definidas ou não podem ser determinadas.</span><span class="sxs-lookup"><span data-stu-id="45431-p104">Default. Indicates that the permissions have not yet been set or cannot be determined.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="45431-138"><strong>adModeWrite</strong></span><span class="sxs-lookup"><span data-stu-id="45431-138"><strong>adModeWrite</strong></span></span></p></td>
<td><p><span data-ttu-id="45431-139">2</span><span class="sxs-lookup"><span data-stu-id="45431-139">2</span></span></p></td>
<td><p><span data-ttu-id="45431-140">Indica permissões de gravação apenas.</span><span class="sxs-lookup"><span data-stu-id="45431-140">Indicates write-only permissions.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="45431-141">Equivalente ADO/WFC</span><span class="sxs-lookup"><span data-stu-id="45431-141">ADO/WFC equivalent</span></span>

<span data-ttu-id="45431-142">Pacote: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="45431-142">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="45431-143">Constante</span><span class="sxs-lookup"><span data-stu-id="45431-143">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="45431-144">AdoEnums.ConnectMode.READ</span><span class="sxs-lookup"><span data-stu-id="45431-144">AdoEnums.ConnectMode.READ</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="45431-145">AdoEnums.ConnectMode.READWRITE</span><span class="sxs-lookup"><span data-stu-id="45431-145">AdoEnums.ConnectMode.READWRITE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="45431-146">(Não há nenhum equivalente a AdoEnums.ConnectMode.RECURSIVE)</span><span class="sxs-lookup"><span data-stu-id="45431-146">(There is no equivalent of AdoEnums.ConnectMode.RECURSIVE)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="45431-147">AdoEnums.ConnectMode.SHAREDENYNONE</span><span class="sxs-lookup"><span data-stu-id="45431-147">AdoEnums.ConnectMode.SHAREDENYNONE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="45431-148">AdoEnums.ConnectMode.SHAREDENYREAD</span><span class="sxs-lookup"><span data-stu-id="45431-148">AdoEnums.ConnectMode.SHAREDENYREAD</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="45431-149">AdoEnums.ConnectMode.SHAREDENYWRITE</span><span class="sxs-lookup"><span data-stu-id="45431-149">AdoEnums.ConnectMode.SHAREDENYWRITE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="45431-150">AdoEnums.ConnectMode.SHAREEXCLUSIVE</span><span class="sxs-lookup"><span data-stu-id="45431-150">AdoEnums.ConnectMode.SHAREEXCLUSIVE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="45431-151">AdoEnums.ConnectMode.UNKNOWN</span><span class="sxs-lookup"><span data-stu-id="45431-151">AdoEnums.ConnectMode.UNKNOWN</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="45431-152">AdoEnums.ConnectMode.WRITE</span><span class="sxs-lookup"><span data-stu-id="45431-152">AdoEnums.ConnectMode.WRITE</span></span></p></td>
</tr>
</tbody>
</table>

