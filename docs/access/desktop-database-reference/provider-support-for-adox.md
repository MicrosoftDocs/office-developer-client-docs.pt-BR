---
title: Suporte do provedor para ADOX
TOCTitle: Provider support for ADOX
ms:assetid: 32ea3236-d69f-df94-1685-d8791aeb9e0f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249100(v=office.15)
ms:contentKeyID: 48544091
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: a92ffe9b4b713518330d9dbfd9979d904a5abe8e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32301096"
---
# <a name="provider-support-for-adox"></a><span data-ttu-id="91434-102">Suporte do provedor para ADOX</span><span class="sxs-lookup"><span data-stu-id="91434-102">Provider support for ADOX</span></span>


<span data-ttu-id="91434-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="91434-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="91434-p101">Determinados recursos do ADOX não têm suporte, dependendo do provedor de dados OLE DB. O ADOX tem suporte completo do [OLE DB Provider for Microsoft Jet](microsoft-ole-db-provider-for-microsoft-jet.md). Os recursos que não têm o suporte do [Microsoft OLE DB Provider for SQL Server](microsoft-ole-db-provider-for-sql-server.md), do [Microsoft OLE DB Provider for ODBC](microsoft-ole-db-provider-for-odbc.md) ou do [Microsoft OLE DB Provider for Oracle](microsoft-ole-db-provider-for-oracle.md) são listados a seguir. O ADOX não tem o suporte de nenhum outro provedor Microsoft OLE DB.</span><span class="sxs-lookup"><span data-stu-id="91434-p101">Certain features of ADOX are unsupported, depending upon your OLE DB data provider. ADOX is fully supported with the [OLE DB Provider for Microsoft Jet](microsoft-ole-db-provider-for-microsoft-jet.md). The unsupported features with the [Microsoft OLE DB Provider for SQL Server](microsoft-ole-db-provider-for-sql-server.md), the [Microsoft OLE DB Provider for ODBC](microsoft-ole-db-provider-for-odbc.md), or the [Microsoft OLE DB Provider for Oracle](microsoft-ole-db-provider-for-oracle.md) are listed below. ADOX is not supported by any other Microsoft OLE DB providers.</span></span>

## <a name="microsoft-ole-db-provider-for-sql-server"></a><span data-ttu-id="91434-108">Microsoft OLE DB Provider for SQL Server</span><span class="sxs-lookup"><span data-stu-id="91434-108">Microsoft OLE DB Provider for SQL Server</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="91434-109">Objeto ou coleção</span><span class="sxs-lookup"><span data-stu-id="91434-109">Object or Collection</span></span></p></th>
<th><p><span data-ttu-id="91434-110">Restrições de uso</span><span class="sxs-lookup"><span data-stu-id="91434-110">Usage Restriction</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="91434-111">Objeto <strong>Catalog</strong></span><span class="sxs-lookup"><span data-stu-id="91434-111"><strong>Catalog</strong> object</span></span></p></td>
<td><p><span data-ttu-id="91434-112">Não há suporte para o método <strong>Create</strong>.</span><span class="sxs-lookup"><span data-stu-id="91434-112">The <strong>Create</strong> method is not supported.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="91434-113">Coleção <strong>Tables</strong></span><span class="sxs-lookup"><span data-stu-id="91434-113"><strong>Tables</strong> collection</span></span></p></td>
<td><p><span data-ttu-id="91434-114">As propriedades são leitura/gravação antes da criação do objeto, e são somente leitura quando um objeto existente é referenciado.</span><span class="sxs-lookup"><span data-stu-id="91434-114">Properties are read/write prior to object creation, and read-only when referencing an existing object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="91434-115">Coleção <strong>Views</strong></span><span class="sxs-lookup"><span data-stu-id="91434-115"><strong>Views</strong> collection</span></span></p></td>
<td><p><span data-ttu-id="91434-116">Não há suporte para <strong>Views</strong>.</span><span class="sxs-lookup"><span data-stu-id="91434-116"><strong>Views</strong> is not supported.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="91434-117">Coleção <strong>Procedures</strong></span><span class="sxs-lookup"><span data-stu-id="91434-117"><strong>Procedures</strong> collection</span></span></p></td>
<td><p><span data-ttu-id="91434-118">Não há suporte para os métodos <strong>Append</strong> e <strong>Delete</strong>.</span><span class="sxs-lookup"><span data-stu-id="91434-118">The <strong>Append</strong> and <strong>Delete</strong> methods are not supported.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="91434-119">Objeto <strong>Procedure</strong></span><span class="sxs-lookup"><span data-stu-id="91434-119"><strong>Procedure</strong> object</span></span></p></td>
<td><p><span data-ttu-id="91434-120">Não há suporte para a propriedade <strong>Command</strong>.</span><span class="sxs-lookup"><span data-stu-id="91434-120">The <strong>Command</strong> property is not supported.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="91434-121">Coleção <strong>Keys</strong></span><span class="sxs-lookup"><span data-stu-id="91434-121"><strong>Keys</strong> collection</span></span></p></td>
<td><p><span data-ttu-id="91434-122">Não há suporte para os métodos <strong>Append</strong> e <strong>Delete</strong>.</span><span class="sxs-lookup"><span data-stu-id="91434-122">The <strong>Append</strong> and <strong>Delete</strong> methods are not supported.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="91434-123">Coleção <strong>Users</strong></span><span class="sxs-lookup"><span data-stu-id="91434-123"><strong>Users</strong> collection</span></span></p></td>
<td><p><span data-ttu-id="91434-124">Não há suporte para <strong>Users</strong>.</span><span class="sxs-lookup"><span data-stu-id="91434-124"><strong>Users</strong> is not supported.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="91434-125">Coleção <strong>Groups</strong></span><span class="sxs-lookup"><span data-stu-id="91434-125"><strong>Groups</strong> collection</span></span></p></td>
<td><p><span data-ttu-id="91434-126">Não há suporte para <strong>Groups</strong>.</span><span class="sxs-lookup"><span data-stu-id="91434-126"><strong>Groups</strong> is not supported.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="microsoft-ole-db-provider-for-odbc"></a><span data-ttu-id="91434-127">Microsoft OLE DB Provider for ODBC</span><span class="sxs-lookup"><span data-stu-id="91434-127">Microsoft OLE DB Provider for ODBC</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="91434-128">Objeto ou coleção</span><span class="sxs-lookup"><span data-stu-id="91434-128">Object or Collection</span></span></p></th>
<th><p><span data-ttu-id="91434-129">Restrições de uso</span><span class="sxs-lookup"><span data-stu-id="91434-129">Usage Restriction</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="91434-130">Objeto <strong>Catalog</strong></span><span class="sxs-lookup"><span data-stu-id="91434-130"><strong>Catalog</strong> object</span></span></p></td>
<td><p><span data-ttu-id="91434-131">Não há suporte para o método <strong>Create</strong>.</span><span class="sxs-lookup"><span data-stu-id="91434-131">The <strong>Create</strong> method is not supported.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="91434-132">Coleção <strong>Tables</strong></span><span class="sxs-lookup"><span data-stu-id="91434-132"><strong>Tables</strong> collection</span></span></p></td>
<td><p><span data-ttu-id="91434-133">Não há suporte para os métodos <strong>Append</strong> e <strong>Delete</strong>.</span><span class="sxs-lookup"><span data-stu-id="91434-133">The <strong>Append</strong> and <strong>Delete</strong> methods are not supported.</span></span> <span data-ttu-id="91434-134">As propriedades são leitura/gravação antes da criação do objeto, e são somente leitura quando um objeto existente é referenciado.</span><span class="sxs-lookup"><span data-stu-id="91434-134">Properties are read/write prior to object creation, and read-only when referencing an existing object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="91434-135">Coleção <strong>Procedures</strong></span><span class="sxs-lookup"><span data-stu-id="91434-135"><strong>Procedures</strong> collection</span></span></p></td>
<td><p><span data-ttu-id="91434-136">Não há suporte para os métodos <strong>Append</strong> e <strong>Delete</strong>.</span><span class="sxs-lookup"><span data-stu-id="91434-136">The <strong>Append</strong> and <strong>Delete</strong> methods are not supported.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="91434-137">Objeto <strong>Procedure</strong></span><span class="sxs-lookup"><span data-stu-id="91434-137"><strong>Procedure</strong> object</span></span></p></td>
<td><p><span data-ttu-id="91434-138">Não há suporte para a propriedade <strong>Command</strong>.</span><span class="sxs-lookup"><span data-stu-id="91434-138">The <strong>Command</strong> property is not supported.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="91434-139">Coleção <strong>Indexes</strong></span><span class="sxs-lookup"><span data-stu-id="91434-139"><strong>Indexes</strong> collection</span></span></p></td>
<td><p><span data-ttu-id="91434-140">Não há suporte para os métodos <strong>Append</strong> e <strong>Delete</strong>.</span><span class="sxs-lookup"><span data-stu-id="91434-140">The <strong>Append</strong> and <strong>Delete</strong> methods are not supported.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="91434-141">Coleção <strong>Keys</strong></span><span class="sxs-lookup"><span data-stu-id="91434-141"><strong>Keys</strong> collection</span></span></p></td>
<td><p><span data-ttu-id="91434-142">Não há suporte para os métodos <strong>Append</strong> e <strong>Delete</strong>.</span><span class="sxs-lookup"><span data-stu-id="91434-142">The <strong>Append</strong> and <strong>Delete</strong> methods are not supported.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="91434-143">Coleção <strong>Users</strong></span><span class="sxs-lookup"><span data-stu-id="91434-143"><strong>Users</strong> collection</span></span></p></td>
<td><p><span data-ttu-id="91434-144">Não há suporte para <strong>Users</strong>.</span><span class="sxs-lookup"><span data-stu-id="91434-144"><strong>Users</strong> is not supported.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="91434-145">Coleção <strong>Groups</strong></span><span class="sxs-lookup"><span data-stu-id="91434-145"><strong>Groups</strong> collection</span></span></p></td>
<td><p><span data-ttu-id="91434-146">Não há suporte para <strong>Groups</strong>.</span><span class="sxs-lookup"><span data-stu-id="91434-146"><strong>Groups</strong> is not supported.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="microsoft-ole-db-provider-for-oracle"></a><span data-ttu-id="91434-147">Microsoft OLE DB Provider for Oracle</span><span class="sxs-lookup"><span data-stu-id="91434-147">Microsoft OLE DB Provider for Oracle</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="91434-148">Objeto ou coleção</span><span class="sxs-lookup"><span data-stu-id="91434-148">Object or Collection</span></span></p></th>
<th><p><span data-ttu-id="91434-149">Restrições de uso</span><span class="sxs-lookup"><span data-stu-id="91434-149">Usage Restriction</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="91434-150">Objeto <strong>Catalog</strong></span><span class="sxs-lookup"><span data-stu-id="91434-150"><strong>Catalog</strong> object</span></span></p></td>
<td><p><span data-ttu-id="91434-151">Não há suporte para o método <strong>Create</strong>.</span><span class="sxs-lookup"><span data-stu-id="91434-151">The <strong>Create</strong> method is not supported.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="91434-152">Coleção <strong>Tables</strong></span><span class="sxs-lookup"><span data-stu-id="91434-152"><strong>Tables</strong> collection</span></span></p></td>
<td><p><span data-ttu-id="91434-153">Não há suporte para os métodos <strong>Append</strong> e <strong>Delete</strong>.</span><span class="sxs-lookup"><span data-stu-id="91434-153">The <strong>Append</strong> and <strong>Delete</strong> methods are not supported.</span></span> <span data-ttu-id="91434-154">As propriedades são leitura/gravação antes da criação do objeto, e são somente leitura quando um objeto existente é referenciado.</span><span class="sxs-lookup"><span data-stu-id="91434-154">Properties are read/write prior to object creation, and read-only when referencing an existing object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="91434-155">Coleção <strong>Views</strong></span><span class="sxs-lookup"><span data-stu-id="91434-155"><strong>Views</strong> collection</span></span></p></td>
<td><p><span data-ttu-id="91434-156">Não há suporte para os métodos <strong>Append</strong> e <strong>Delete</strong>.</span><span class="sxs-lookup"><span data-stu-id="91434-156">The <strong>Append</strong> and <strong>Delete</strong> methods are not supported.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="91434-157">Objeto <strong>View</strong></span><span class="sxs-lookup"><span data-stu-id="91434-157"><strong>View</strong> object</span></span></p></td>
<td><p><span data-ttu-id="91434-158">Não há suporte para a propriedade <strong>Command</strong>.</span><span class="sxs-lookup"><span data-stu-id="91434-158">The <strong>Command</strong> property is not supported.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="91434-159">Objeto <strong>Procedures</strong></span><span class="sxs-lookup"><span data-stu-id="91434-159"><strong>Procedures</strong> object</span></span></p></td>
<td><p><span data-ttu-id="91434-160">Não há suporte para os métodos <strong>Append</strong> e <strong>Delete</strong>.</span><span class="sxs-lookup"><span data-stu-id="91434-160">The <strong>Append</strong> and <strong>Delete</strong> methods are not supported.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="91434-161">Objeto <strong>Procedure</strong></span><span class="sxs-lookup"><span data-stu-id="91434-161"><strong>Procedure</strong> object</span></span></p></td>
<td><p><span data-ttu-id="91434-162">Não há suporte para a propriedade <strong>Command</strong>.</span><span class="sxs-lookup"><span data-stu-id="91434-162">The <strong>Command</strong> property is not supported.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="91434-163">Coleção <strong>Indexes</strong></span><span class="sxs-lookup"><span data-stu-id="91434-163"><strong>Indexes</strong> collection</span></span></p></td>
<td><p><span data-ttu-id="91434-164">Não há suporte para os métodos <strong>Append</strong> e <strong>Delete</strong>.</span><span class="sxs-lookup"><span data-stu-id="91434-164">The <strong>Append</strong> and <strong>Delete</strong> methods are not supported.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="91434-165">Coleção <strong>Keys</strong></span><span class="sxs-lookup"><span data-stu-id="91434-165"><strong>Keys</strong> collection</span></span></p></td>
<td><p><span data-ttu-id="91434-166">Não há suporte para os métodos <strong>Append</strong> e <strong>Delete</strong>.</span><span class="sxs-lookup"><span data-stu-id="91434-166">The <strong>Append</strong> and <strong>Delete</strong> methods are not supported.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="91434-167">Coleção <strong>Users</strong></span><span class="sxs-lookup"><span data-stu-id="91434-167"><strong>Users</strong> collection</span></span></p></td>
<td><p><span data-ttu-id="91434-168">Não há suporte para <strong>Users</strong>.</span><span class="sxs-lookup"><span data-stu-id="91434-168"><strong>Users</strong> is not supported.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="91434-169">Coleção <strong>Groups</strong></span><span class="sxs-lookup"><span data-stu-id="91434-169"><strong>Groups</strong> collection</span></span></p></td>
<td><p><span data-ttu-id="91434-170">Não há suporte para <strong>Groups</strong>.</span><span class="sxs-lookup"><span data-stu-id="91434-170"><strong>Groups</strong> is not supported.</span></span></p></td>
</tr>
</tbody>
</table>

