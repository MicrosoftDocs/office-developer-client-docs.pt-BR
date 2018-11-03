---
title: Suporte do provedor para ADOX
TOCTitle: Provider support for ADOX
ms:assetid: 32ea3236-d69f-df94-1685-d8791aeb9e0f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249100(v=office.15)
ms:contentKeyID: 48544091
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: bdd9ca9a2274f03f1592f73c3da5a6837101fda2
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/03/2018
ms.locfileid: "25947823"
---
# <a name="provider-support-for-adox"></a><span data-ttu-id="a4db9-102">Suporte do provedor para ADOX</span><span class="sxs-lookup"><span data-stu-id="a4db9-102">Provider support for ADOX</span></span>


<span data-ttu-id="a4db9-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="a4db9-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="a4db9-p101">Determinados recursos do ADOX não têm suporte, dependendo do provedor de dados OLE DB. O ADOX tem suporte completo do [OLE DB Provider for Microsoft Jet](microsoft-ole-db-provider-for-microsoft-jet.md). Os recursos que não têm o suporte do [Microsoft OLE DB Provider for SQL Server](microsoft-ole-db-provider-for-sql-server.md), do [Microsoft OLE DB Provider for ODBC](microsoft-ole-db-provider-for-odbc.md) ou do [Microsoft OLE DB Provider for Oracle](microsoft-ole-db-provider-for-oracle.md) são listados a seguir. O ADOX não tem o suporte de nenhum outro provedor Microsoft OLE DB.</span><span class="sxs-lookup"><span data-stu-id="a4db9-p101">Certain features of ADOX are unsupported, depending upon your OLE DB data provider. ADOX is fully supported with the [OLE DB Provider for Microsoft Jet](microsoft-ole-db-provider-for-microsoft-jet.md). The unsupported features with the [Microsoft OLE DB Provider for SQL Server](microsoft-ole-db-provider-for-sql-server.md), the [Microsoft OLE DB Provider for ODBC](microsoft-ole-db-provider-for-odbc.md), or the [Microsoft OLE DB Provider for Oracle](microsoft-ole-db-provider-for-oracle.md) are listed below. ADOX is not supported by any other Microsoft OLE DB providers.</span></span>

## <a name="microsoft-ole-db-provider-for-sql-server"></a><span data-ttu-id="a4db9-108">Microsoft OLE DB Provider for SQL Server</span><span class="sxs-lookup"><span data-stu-id="a4db9-108">Microsoft OLE DB Provider for SQL Server</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a4db9-109">Objeto ou coleção</span><span class="sxs-lookup"><span data-stu-id="a4db9-109">Object or Collection</span></span></p></th>
<th><p><span data-ttu-id="a4db9-110">Restrições de uso</span><span class="sxs-lookup"><span data-stu-id="a4db9-110">Usage Restriction</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a4db9-111">Objeto <strong>Catalog</strong></span><span class="sxs-lookup"><span data-stu-id="a4db9-111"><strong>Catalog</strong> object</span></span></p></td>
<td><p><span data-ttu-id="a4db9-112">Não há suporte para o método <strong>Create</strong>.</span><span class="sxs-lookup"><span data-stu-id="a4db9-112">The <strong>Create</strong> method is not supported.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a4db9-113">Coleção <strong>Tables</strong></span><span class="sxs-lookup"><span data-stu-id="a4db9-113"><strong>Tables</strong> collection</span></span></p></td>
<td><p><span data-ttu-id="a4db9-114">As propriedades são leitura/gravação antes da criação do objeto, e são somente leitura quando um objeto existente é referenciado.</span><span class="sxs-lookup"><span data-stu-id="a4db9-114">Properties are read/write prior to object creation, and read-only when referencing an existing object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a4db9-115">Coleção <strong>Views</strong></span><span class="sxs-lookup"><span data-stu-id="a4db9-115"><strong>Views</strong> collection</span></span></p></td>
<td><p><span data-ttu-id="a4db9-116">Não há suporte para <strong>Views</strong>.</span><span class="sxs-lookup"><span data-stu-id="a4db9-116"><strong>Views</strong> is not supported.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a4db9-117">Coleção <strong>Procedures</strong></span><span class="sxs-lookup"><span data-stu-id="a4db9-117"><strong>Procedures</strong> collection</span></span></p></td>
<td><p><span data-ttu-id="a4db9-118">Não há suporte para os métodos <strong>Append</strong> e <strong>Delete</strong>.</span><span class="sxs-lookup"><span data-stu-id="a4db9-118">The <strong>Append</strong> and <strong>Delete</strong> methods are not supported.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a4db9-119">Objeto <strong>Procedure</strong></span><span class="sxs-lookup"><span data-stu-id="a4db9-119"><strong>Procedure</strong> object</span></span></p></td>
<td><p><span data-ttu-id="a4db9-120">Não há suporte para a propriedade <strong>Command</strong>.</span><span class="sxs-lookup"><span data-stu-id="a4db9-120">The <strong>Command</strong> property is not supported.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a4db9-121">Coleção <strong>Keys</strong></span><span class="sxs-lookup"><span data-stu-id="a4db9-121"><strong>Keys</strong> collection</span></span></p></td>
<td><p><span data-ttu-id="a4db9-122">Não há suporte para os métodos <strong>Append</strong> e <strong>Delete</strong>.</span><span class="sxs-lookup"><span data-stu-id="a4db9-122">The <strong>Append</strong> and <strong>Delete</strong> methods are not supported.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a4db9-123">Coleção <strong>Users</strong></span><span class="sxs-lookup"><span data-stu-id="a4db9-123"><strong>Users</strong> collection</span></span></p></td>
<td><p><span data-ttu-id="a4db9-124">Não há suporte para <strong>Users</strong>.</span><span class="sxs-lookup"><span data-stu-id="a4db9-124"><strong>Users</strong> is not supported.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a4db9-125">Coleção <strong>Groups</strong></span><span class="sxs-lookup"><span data-stu-id="a4db9-125"><strong>Groups</strong> collection</span></span></p></td>
<td><p><span data-ttu-id="a4db9-126">Não há suporte para <strong>Groups</strong>.</span><span class="sxs-lookup"><span data-stu-id="a4db9-126"><strong>Groups</strong> is not supported.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="microsoft-ole-db-provider-for-odbc"></a><span data-ttu-id="a4db9-127">Microsoft OLE DB Provider for ODBC</span><span class="sxs-lookup"><span data-stu-id="a4db9-127">Microsoft OLE DB Provider for ODBC</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a4db9-128">Objeto ou coleção</span><span class="sxs-lookup"><span data-stu-id="a4db9-128">Object or Collection</span></span></p></th>
<th><p><span data-ttu-id="a4db9-129">Restrições de uso</span><span class="sxs-lookup"><span data-stu-id="a4db9-129">Usage Restriction</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a4db9-130">Objeto <strong>Catalog</strong></span><span class="sxs-lookup"><span data-stu-id="a4db9-130"><strong>Catalog</strong> object</span></span></p></td>
<td><p><span data-ttu-id="a4db9-131">Não há suporte para o método <strong>Create</strong>.</span><span class="sxs-lookup"><span data-stu-id="a4db9-131">The <strong>Create</strong> method is not supported.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a4db9-132">Coleção <strong>Tables</strong></span><span class="sxs-lookup"><span data-stu-id="a4db9-132"><strong>Tables</strong> collection</span></span></p></td>
<td><p><span data-ttu-id="a4db9-133">Não há suporte para os métodos <strong>Append</strong> e <strong>Delete</strong>.
</span><span class="sxs-lookup"><span data-stu-id="a4db9-133">The <strong>Append</strong> and <strong>Delete</strong> methods are not supported.</span></span> <span data-ttu-id="a4db9-134">As propriedades são leitura/gravação antes da criação do objeto, e são somente leitura quando um objeto existente é referenciado.</span><span class="sxs-lookup"><span data-stu-id="a4db9-134">Properties are read/write prior to object creation, and read-only when referencing an existing object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a4db9-135">Coleção <strong>Procedures</strong></span><span class="sxs-lookup"><span data-stu-id="a4db9-135"><strong>Procedures</strong> collection</span></span></p></td>
<td><p><span data-ttu-id="a4db9-136">Não há suporte para os métodos <strong>Append</strong> e <strong>Delete</strong>.</span><span class="sxs-lookup"><span data-stu-id="a4db9-136">The <strong>Append</strong> and <strong>Delete</strong> methods are not supported.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a4db9-137">Objeto <strong>Procedure</strong></span><span class="sxs-lookup"><span data-stu-id="a4db9-137"><strong>Procedure</strong> object</span></span></p></td>
<td><p><span data-ttu-id="a4db9-138">Não há suporte para a propriedade <strong>Command</strong>.</span><span class="sxs-lookup"><span data-stu-id="a4db9-138">The <strong>Command</strong> property is not supported.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a4db9-139">Coleção <strong>Indexes</strong></span><span class="sxs-lookup"><span data-stu-id="a4db9-139"><strong>Indexes</strong> collection</span></span></p></td>
<td><p><span data-ttu-id="a4db9-140">Não há suporte para os métodos <strong>Append</strong> e <strong>Delete</strong>.</span><span class="sxs-lookup"><span data-stu-id="a4db9-140">The <strong>Append</strong> and <strong>Delete</strong> methods are not supported.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a4db9-141">Coleção <strong>Keys</strong></span><span class="sxs-lookup"><span data-stu-id="a4db9-141"><strong>Keys</strong> collection</span></span></p></td>
<td><p><span data-ttu-id="a4db9-142">Não há suporte para os métodos <strong>Append</strong> e <strong>Delete</strong>.</span><span class="sxs-lookup"><span data-stu-id="a4db9-142">The <strong>Append</strong> and <strong>Delete</strong> methods are not supported.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a4db9-143">Coleção <strong>Users</strong></span><span class="sxs-lookup"><span data-stu-id="a4db9-143"><strong>Users</strong> collection</span></span></p></td>
<td><p><span data-ttu-id="a4db9-144">Não há suporte para <strong>Users</strong>.</span><span class="sxs-lookup"><span data-stu-id="a4db9-144"><strong>Users</strong> is not supported.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a4db9-145">Coleção <strong>Groups</strong></span><span class="sxs-lookup"><span data-stu-id="a4db9-145"><strong>Groups</strong> collection</span></span></p></td>
<td><p><span data-ttu-id="a4db9-146">Não há suporte para <strong>Groups</strong>.</span><span class="sxs-lookup"><span data-stu-id="a4db9-146"><strong>Groups</strong> is not supported.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="microsoft-ole-db-provider-for-oracle"></a><span data-ttu-id="a4db9-147">Microsoft OLE DB Provider for Oracle</span><span class="sxs-lookup"><span data-stu-id="a4db9-147">Microsoft OLE DB Provider for Oracle</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a4db9-148">Objeto ou coleção</span><span class="sxs-lookup"><span data-stu-id="a4db9-148">Object or Collection</span></span></p></th>
<th><p><span data-ttu-id="a4db9-149">Restrições de uso</span><span class="sxs-lookup"><span data-stu-id="a4db9-149">Usage Restriction</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a4db9-150">Objeto <strong>Catalog</strong></span><span class="sxs-lookup"><span data-stu-id="a4db9-150"><strong>Catalog</strong> object</span></span></p></td>
<td><p><span data-ttu-id="a4db9-151">Não há suporte para o método <strong>Create</strong>.</span><span class="sxs-lookup"><span data-stu-id="a4db9-151">The <strong>Create</strong> method is not supported.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a4db9-152">Coleção <strong>Tables</strong></span><span class="sxs-lookup"><span data-stu-id="a4db9-152"><strong>Tables</strong> collection</span></span></p></td>
<td><p><span data-ttu-id="a4db9-153">Não há suporte para os métodos <strong>Append</strong> e <strong>Delete</strong>.
</span><span class="sxs-lookup"><span data-stu-id="a4db9-153">The <strong>Append</strong> and <strong>Delete</strong> methods are not supported.</span></span> <span data-ttu-id="a4db9-154">As propriedades são leitura/gravação antes da criação do objeto, e são somente leitura quando um objeto existente é referenciado.</span><span class="sxs-lookup"><span data-stu-id="a4db9-154">Properties are read/write prior to object creation, and read-only when referencing an existing object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a4db9-155">Coleção <strong>Views</strong></span><span class="sxs-lookup"><span data-stu-id="a4db9-155"><strong>Views</strong> collection</span></span></p></td>
<td><p><span data-ttu-id="a4db9-156">Não há suporte para os métodos <strong>Append</strong> e <strong>Delete</strong>.</span><span class="sxs-lookup"><span data-stu-id="a4db9-156">The <strong>Append</strong> and <strong>Delete</strong> methods are not supported.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a4db9-157">Objeto <strong>View</strong></span><span class="sxs-lookup"><span data-stu-id="a4db9-157"><strong>View</strong> object</span></span></p></td>
<td><p><span data-ttu-id="a4db9-158">Não há suporte para a propriedade <strong>Command</strong>.</span><span class="sxs-lookup"><span data-stu-id="a4db9-158">The <strong>Command</strong> property is not supported.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a4db9-159">Objeto <strong>Procedures</strong></span><span class="sxs-lookup"><span data-stu-id="a4db9-159"><strong>Procedures</strong> object</span></span></p></td>
<td><p><span data-ttu-id="a4db9-160">Não há suporte para os métodos <strong>Append</strong> e <strong>Delete</strong>.</span><span class="sxs-lookup"><span data-stu-id="a4db9-160">The <strong>Append</strong> and <strong>Delete</strong> methods are not supported.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a4db9-161">Objeto <strong>Procedure</strong></span><span class="sxs-lookup"><span data-stu-id="a4db9-161"><strong>Procedure</strong> object</span></span></p></td>
<td><p><span data-ttu-id="a4db9-162">Não há suporte para a propriedade <strong>Command</strong>.</span><span class="sxs-lookup"><span data-stu-id="a4db9-162">The <strong>Command</strong> property is not supported.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a4db9-163">Coleção <strong>Indexes</strong></span><span class="sxs-lookup"><span data-stu-id="a4db9-163"><strong>Indexes</strong> collection</span></span></p></td>
<td><p><span data-ttu-id="a4db9-164">Não há suporte para os métodos <strong>Append</strong> e <strong>Delete</strong>.</span><span class="sxs-lookup"><span data-stu-id="a4db9-164">The <strong>Append</strong> and <strong>Delete</strong> methods are not supported.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a4db9-165">Coleção <strong>Keys</strong></span><span class="sxs-lookup"><span data-stu-id="a4db9-165"><strong>Keys</strong> collection</span></span></p></td>
<td><p><span data-ttu-id="a4db9-166">Não há suporte para os métodos <strong>Append</strong> e <strong>Delete</strong>.</span><span class="sxs-lookup"><span data-stu-id="a4db9-166">The <strong>Append</strong> and <strong>Delete</strong> methods are not supported.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a4db9-167">Coleção <strong>Users</strong></span><span class="sxs-lookup"><span data-stu-id="a4db9-167"><strong>Users</strong> collection</span></span></p></td>
<td><p><span data-ttu-id="a4db9-168">Não há suporte para <strong>Users</strong>.</span><span class="sxs-lookup"><span data-stu-id="a4db9-168"><strong>Users</strong> is not supported.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a4db9-169">Coleção <strong>Groups</strong></span><span class="sxs-lookup"><span data-stu-id="a4db9-169"><strong>Groups</strong> collection</span></span></p></td>
<td><p><span data-ttu-id="a4db9-170">Não há suporte para <strong>Groups</strong>.</span><span class="sxs-lookup"><span data-stu-id="a4db9-170"><strong>Groups</strong> is not supported.</span></span></p></td>
</tr>
</tbody>
</table>

