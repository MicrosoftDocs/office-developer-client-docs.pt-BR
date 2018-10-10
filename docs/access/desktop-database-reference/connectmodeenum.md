---
title: ConnectModeEnum (referência de banco de dados da área de trabalho do Access)
TOCTitle: ConnectModeEnum
ms:assetid: a15aa733-f899-5fe9-e705-67a4301706d1
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249743(v=office.15)
ms:contentKeyID: 48546728
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 5b39fc42259a1906891b82bf9b9ef252997e6240
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25464862"
---
# <a name="connectmodeenum"></a><span data-ttu-id="46e7c-102">ConnectModeEnum</span><span class="sxs-lookup"><span data-stu-id="46e7c-102">ConnectModeEnum</span></span>


<span data-ttu-id="46e7c-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="46e7c-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="46e7c-104">Especifica as permissões disponíveis para modificar os dados em uma [Connection](connection-object-ado.md), abrir um [Record](record-object-ado.md) ou especificar os valores para a propriedade [Mode](mode-property-ado.md) dos objetos **Record** e [Stream](stream-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="46e7c-104">Specifies the available permissions for modifying data in a [Connection](connection-object-ado.md), opening a [Record](record-object-ado.md), or specifying values for the [Mode](mode-property-ado.md) property of the **Record** and [Stream](stream-object-ado.md) objects.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="46e7c-105">Constant</span><span class="sxs-lookup"><span data-stu-id="46e7c-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="46e7c-106">Valor</span><span class="sxs-lookup"><span data-stu-id="46e7c-106">Value</span></span></p></th>
<th><p><span data-ttu-id="46e7c-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="46e7c-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="46e7c-108"><strong>adModeRead</strong></span><span class="sxs-lookup"><span data-stu-id="46e7c-108"><strong>adModeRead</strong></span></span></p></td>
<td><p><span data-ttu-id="46e7c-109">1</span><span class="sxs-lookup"><span data-stu-id="46e7c-109">1</span></span></p></td>
<td><p><span data-ttu-id="46e7c-110">Indica permissões somente leitura.</span><span class="sxs-lookup"><span data-stu-id="46e7c-110">Indicates read-only permissions.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="46e7c-111"><strong>adModeReadWrite</strong></span><span class="sxs-lookup"><span data-stu-id="46e7c-111"><strong>adModeReadWrite</strong></span></span></p></td>
<td><p><span data-ttu-id="46e7c-112">3</span><span class="sxs-lookup"><span data-stu-id="46e7c-112">3</span></span></p></td>
<td><p><span data-ttu-id="46e7c-113">Indica permissões de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="46e7c-113">Indicates read/write permissions.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="46e7c-114"><strong>adModeRecursive</strong></span><span class="sxs-lookup"><span data-stu-id="46e7c-114"><strong>adModeRecursive</strong></span></span></p></td>
<td><p><span data-ttu-id="46e7c-115">0x400000</span><span class="sxs-lookup"><span data-stu-id="46e7c-115">0x400000</span></span></p></td>
<td><p><span data-ttu-id="46e7c-116">Usado em conjunto com os outros valores <em>*ShareDeny*</em> (<strong>adModeShareDenyNone</strong>, <strong>adModeShareDenyWrite</strong>ou <strong>adModeShareDenyRead</strong>) para propagar as restrições de compartilhamento para todos os registros de subsites do <strong>registro</strong>atual.</span><span class="sxs-lookup"><span data-stu-id="46e7c-116">Used in conjunction with the other <em>*ShareDeny*</em> values (<strong>adModeShareDenyNone</strong>, <strong>adModeShareDenyWrite</strong>, or <strong>adModeShareDenyRead</strong>) to propagate sharing restrictions to all sub-records of the current <strong>Record</strong>.</span></span> <span data-ttu-id="46e7c-117">Ele não terá efeito se o <strong>registro</strong> não tiver nenhum filho.</span><span class="sxs-lookup"><span data-stu-id="46e7c-117">It has no affect if the <strong>Record</strong> does not have any children.</span></span> <span data-ttu-id="46e7c-118">Um erro em tempo de execução é gerado se ele é usado com <strong>adModeShareDenyNone</strong> somente.</span><span class="sxs-lookup"><span data-stu-id="46e7c-118">A run-time error is generated if it is used with <strong>adModeShareDenyNone</strong> only.</span></span> <span data-ttu-id="46e7c-119">No entanto, ele pode ser usado com <strong>adModeShareDenyNone</strong> quando combinado com outros valores.</span><span class="sxs-lookup"><span data-stu-id="46e7c-119">However, it can be used with <strong>adModeShareDenyNone</strong> when combined with other values.</span></span> <span data-ttu-id="46e7c-120">Por exemplo, você pode usar &quot; <strong>adModeRead</strong> ou <strong>adModeShareDenyNone</strong> ou <strong>adModeRecursive</strong>&quot;.</span><span class="sxs-lookup"><span data-stu-id="46e7c-120">For example, you can use &quot;<strong>adModeRead</strong> Or <strong>adModeShareDenyNone</strong> Or <strong>adModeRecursive</strong>&quot;.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="46e7c-121"><strong>adModeShareDenyNone</strong></span><span class="sxs-lookup"><span data-stu-id="46e7c-121"><strong>adModeShareDenyNone</strong></span></span></p></td>
<td><p><span data-ttu-id="46e7c-122">16</span><span class="sxs-lookup"><span data-stu-id="46e7c-122">16</span></span></p></td>
<td><p><span data-ttu-id="46e7c-p102">Permite que outras pessoas estabeleçam uma conexão com quaisquer permissões. Não pode ser negado a terceiros acesso de leitura nem de gravação.</span><span class="sxs-lookup"><span data-stu-id="46e7c-p102">Allows others to open a connection with any permissions. Neither read nor write access can be denied to others.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="46e7c-125"><strong>adModeShareDenyRead</strong></span><span class="sxs-lookup"><span data-stu-id="46e7c-125"><strong>adModeShareDenyRead</strong></span></span></p></td>
<td><p><span data-ttu-id="46e7c-126">4</span><span class="sxs-lookup"><span data-stu-id="46e7c-126">4</span></span></p></td>
<td><p><span data-ttu-id="46e7c-127">Impede que outras pessoas estabeleçam uma conexão com permissões de leitura.</span><span class="sxs-lookup"><span data-stu-id="46e7c-127">Prevents others from opening a connection with read permissions.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="46e7c-128"><strong>adModeShareDenyWrite</strong></span><span class="sxs-lookup"><span data-stu-id="46e7c-128"><strong>adModeShareDenyWrite</strong></span></span></p></td>
<td><p><span data-ttu-id="46e7c-129">8</span><span class="sxs-lookup"><span data-stu-id="46e7c-129">8</span></span></p></td>
<td><p><span data-ttu-id="46e7c-130">Impede que outras pessoas estabeleçam uma conexão com permissões de gravação.</span><span class="sxs-lookup"><span data-stu-id="46e7c-130">Prevents others from opening a connection with write permissions.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="46e7c-131"><strong>adModeShareExclusive</strong></span><span class="sxs-lookup"><span data-stu-id="46e7c-131"><strong>adModeShareExclusive</strong></span></span></p></td>
<td><p><span data-ttu-id="46e7c-132">12</span><span class="sxs-lookup"><span data-stu-id="46e7c-132">12</span></span></p></td>
<td><p><span data-ttu-id="46e7c-133">Impede que outras pessoas estabeleçam uma conexão.</span><span class="sxs-lookup"><span data-stu-id="46e7c-133">Prevents others from opening a connection.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="46e7c-134"><strong>adModeUnknown</strong></span><span class="sxs-lookup"><span data-stu-id="46e7c-134"><strong>adModeUnknown</strong></span></span></p></td>
<td><p><span data-ttu-id="46e7c-135">0</span><span class="sxs-lookup"><span data-stu-id="46e7c-135">0</span></span></p></td>
<td><p><span data-ttu-id="46e7c-p103">Padrão. Indica que as permissões ainda não foram definidas ou não podem ser determinadas.</span><span class="sxs-lookup"><span data-stu-id="46e7c-p103">Default. Indicates that the permissions have not yet been set or cannot be determined.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="46e7c-138"><strong>adModeWrite</strong></span><span class="sxs-lookup"><span data-stu-id="46e7c-138"><strong>adModeWrite</strong></span></span></p></td>
<td><p><span data-ttu-id="46e7c-139">2</span><span class="sxs-lookup"><span data-stu-id="46e7c-139">2</span></span></p></td>
<td><p><span data-ttu-id="46e7c-140">Indica permissões de gravação apenas.</span><span class="sxs-lookup"><span data-stu-id="46e7c-140">Indicates write-only permissions.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="46e7c-141">**ADO/WFC Equivalente**</span><span class="sxs-lookup"><span data-stu-id="46e7c-141">**ADO/WFC Equivalent**</span></span>

<span data-ttu-id="46e7c-142">Pacote: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="46e7c-142">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="46e7c-143">Constante</span><span class="sxs-lookup"><span data-stu-id="46e7c-143">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="46e7c-144">AdoEnums.ConnectMode.READ</span><span class="sxs-lookup"><span data-stu-id="46e7c-144">AdoEnums.ConnectMode.READ</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="46e7c-145">AdoEnums.ConnectMode.READWRITE</span><span class="sxs-lookup"><span data-stu-id="46e7c-145">AdoEnums.ConnectMode.READWRITE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="46e7c-146">(Não há nenhum equivalente a AdoEnums.ConnectMode.RECURSIVE)</span><span class="sxs-lookup"><span data-stu-id="46e7c-146">(There is no equivalent of AdoEnums.ConnectMode.RECURSIVE)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="46e7c-147">AdoEnums.ConnectMode.SHAREDENYNONE</span><span class="sxs-lookup"><span data-stu-id="46e7c-147">AdoEnums.ConnectMode.SHAREDENYNONE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="46e7c-148">AdoEnums.ConnectMode.SHAREDENYREAD</span><span class="sxs-lookup"><span data-stu-id="46e7c-148">AdoEnums.ConnectMode.SHAREDENYREAD</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="46e7c-149">AdoEnums.ConnectMode.SHAREDENYWRITE</span><span class="sxs-lookup"><span data-stu-id="46e7c-149">AdoEnums.ConnectMode.SHAREDENYWRITE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="46e7c-150">AdoEnums.ConnectMode.SHAREEXCLUSIVE</span><span class="sxs-lookup"><span data-stu-id="46e7c-150">AdoEnums.ConnectMode.SHAREEXCLUSIVE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="46e7c-151">AdoEnums.ConnectMode.UNKNOWN</span><span class="sxs-lookup"><span data-stu-id="46e7c-151">AdoEnums.ConnectMode.UNKNOWN</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="46e7c-152">AdoEnums.ConnectMode.WRITE</span><span class="sxs-lookup"><span data-stu-id="46e7c-152">AdoEnums.ConnectMode.WRITE</span></span></p></td>
</tr>
</tbody>
</table>

