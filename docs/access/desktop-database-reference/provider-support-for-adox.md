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
# <a name="provider-support-for-adox"></a><span data-ttu-id="8c24d-102">Suporte do provedor para ADOX</span><span class="sxs-lookup"><span data-stu-id="8c24d-102">Provider support for ADOX</span></span>


<span data-ttu-id="8c24d-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="8c24d-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="8c24d-p101">Determinados recursos do ADOX não têm suporte, dependendo do provedor de dados OLE DB. O ADOX tem suporte completo do [OLE DB Provider for Microsoft Jet](microsoft-ole-db-provider-for-microsoft-jet.md). Os recursos que não têm o suporte do [Microsoft OLE DB Provider for SQL Server](microsoft-ole-db-provider-for-sql-server.md), do [Microsoft OLE DB Provider for ODBC](microsoft-ole-db-provider-for-odbc.md) ou do [Microsoft OLE DB Provider for Oracle](microsoft-ole-db-provider-for-oracle.md) são listados a seguir. O ADOX não tem o suporte de nenhum outro provedor Microsoft OLE DB.</span><span class="sxs-lookup"><span data-stu-id="8c24d-p101">Certain features of ADOX are unsupported, depending upon your OLE DB data provider. ADOX is fully supported with the [OLE DB Provider for Microsoft Jet](microsoft-ole-db-provider-for-microsoft-jet.md). The unsupported features with the [Microsoft OLE DB Provider for SQL Server](microsoft-ole-db-provider-for-sql-server.md), the [Microsoft OLE DB Provider for ODBC](microsoft-ole-db-provider-for-odbc.md), or the [Microsoft OLE DB Provider for Oracle](microsoft-ole-db-provider-for-oracle.md) are listed below. ADOX is not supported by any other Microsoft OLE DB providers.</span></span>

## <a name="microsoft-ole-db-provider-for-sql-server"></a><span data-ttu-id="8c24d-108">Microsoft OLE DB Provider for SQL Server</span><span class="sxs-lookup"><span data-stu-id="8c24d-108">Microsoft OLE DB Provider for SQL Server</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="8c24d-109">Objeto ou coleção</span><span class="sxs-lookup"><span data-stu-id="8c24d-109">Object or Collection</span></span></p></th>
<th><p><span data-ttu-id="8c24d-110">Restrições de uso</span><span class="sxs-lookup"><span data-stu-id="8c24d-110">Usage Restriction</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8c24d-111">Objeto <strong>Catalog</strong></span><span class="sxs-lookup"><span data-stu-id="8c24d-111"><strong>Catalog</strong> object</span></span></p></td>
<td><p><span data-ttu-id="8c24d-112">Não há suporte para o método <strong>Create</strong>.</span><span class="sxs-lookup"><span data-stu-id="8c24d-112">The <strong>Create</strong> method is not supported.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8c24d-113">Coleção <strong>Tables</strong></span><span class="sxs-lookup"><span data-stu-id="8c24d-113"><strong>Tables</strong> collection</span></span></p></td>
<td><p><span data-ttu-id="8c24d-114">As propriedades são leitura/gravação antes da criação do objeto, e são somente leitura quando um objeto existente é referenciado.</span><span class="sxs-lookup"><span data-stu-id="8c24d-114">Properties are read/write prior to object creation, and read-only when referencing an existing object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8c24d-115">Coleção <strong>Views</strong></span><span class="sxs-lookup"><span data-stu-id="8c24d-115"><strong>Views</strong> collection</span></span></p></td>
<td><p><span data-ttu-id="8c24d-116">Não há suporte para <strong>Views</strong>.</span><span class="sxs-lookup"><span data-stu-id="8c24d-116"><strong>Views</strong> is not supported.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8c24d-117">Coleção <strong>Procedures</strong></span><span class="sxs-lookup"><span data-stu-id="8c24d-117"><strong>Procedures</strong> collection</span></span></p></td>
<td><p><span data-ttu-id="8c24d-118">Não há suporte para os métodos <strong>Append</strong> e <strong>Delete</strong>.</span><span class="sxs-lookup"><span data-stu-id="8c24d-118">The <strong>Append</strong> and <strong>Delete</strong> methods are not supported.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8c24d-119">Objeto <strong>Procedure</strong></span><span class="sxs-lookup"><span data-stu-id="8c24d-119"><strong>Procedure</strong> object</span></span></p></td>
<td><p><span data-ttu-id="8c24d-120">Não há suporte para a propriedade <strong>Command</strong>.</span><span class="sxs-lookup"><span data-stu-id="8c24d-120">The <strong>Command</strong> property is not supported.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8c24d-121">Coleção <strong>Keys</strong></span><span class="sxs-lookup"><span data-stu-id="8c24d-121"><strong>Keys</strong> collection</span></span></p></td>
<td><p><span data-ttu-id="8c24d-122">Não há suporte para os métodos <strong>Append</strong> e <strong>Delete</strong>.</span><span class="sxs-lookup"><span data-stu-id="8c24d-122">The <strong>Append</strong> and <strong>Delete</strong> methods are not supported.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8c24d-123">Coleção <strong>Users</strong></span><span class="sxs-lookup"><span data-stu-id="8c24d-123"><strong>Users</strong> collection</span></span></p></td>
<td><p><span data-ttu-id="8c24d-124">Não há suporte para <strong>Users</strong>.</span><span class="sxs-lookup"><span data-stu-id="8c24d-124"><strong>Users</strong> is not supported.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8c24d-125">Coleção <strong>Groups</strong></span><span class="sxs-lookup"><span data-stu-id="8c24d-125"><strong>Groups</strong> collection</span></span></p></td>
<td><p><span data-ttu-id="8c24d-126">Não há suporte para <strong>Groups</strong>.</span><span class="sxs-lookup"><span data-stu-id="8c24d-126"><strong>Groups</strong> is not supported.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="microsoft-ole-db-provider-for-odbc"></a><span data-ttu-id="8c24d-127">Microsoft OLE DB Provider for ODBC</span><span class="sxs-lookup"><span data-stu-id="8c24d-127">Microsoft OLE DB Provider for ODBC</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="8c24d-128">Objeto ou coleção</span><span class="sxs-lookup"><span data-stu-id="8c24d-128">Object or Collection</span></span></p></th>
<th><p><span data-ttu-id="8c24d-129">Restrições de uso</span><span class="sxs-lookup"><span data-stu-id="8c24d-129">Usage Restriction</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8c24d-130">Objeto <strong>Catalog</strong></span><span class="sxs-lookup"><span data-stu-id="8c24d-130"><strong>Catalog</strong> object</span></span></p></td>
<td><p><span data-ttu-id="8c24d-131">Não há suporte para o método <strong>Create</strong>.</span><span class="sxs-lookup"><span data-stu-id="8c24d-131">The <strong>Create</strong> method is not supported.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8c24d-132">Coleção <strong>Tables</strong></span><span class="sxs-lookup"><span data-stu-id="8c24d-132"><strong>Tables</strong> collection</span></span></p></td>
<td><p><span data-ttu-id="8c24d-133">Não há suporte para os métodos <strong>Append</strong> e <strong>Delete</strong>.</span><span class="sxs-lookup"><span data-stu-id="8c24d-133">The <strong>Append</strong> and <strong>Delete</strong> methods are not supported.</span></span> <span data-ttu-id="8c24d-134">As propriedades são leitura/gravação antes da criação do objeto, e são somente leitura quando um objeto existente é referenciado.</span><span class="sxs-lookup"><span data-stu-id="8c24d-134">Properties are read/write prior to object creation, and read-only when referencing an existing object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8c24d-135">Coleção <strong>Procedures</strong></span><span class="sxs-lookup"><span data-stu-id="8c24d-135"><strong>Procedures</strong> collection</span></span></p></td>
<td><p><span data-ttu-id="8c24d-136">Não há suporte para os métodos <strong>Append</strong> e <strong>Delete</strong>.</span><span class="sxs-lookup"><span data-stu-id="8c24d-136">The <strong>Append</strong> and <strong>Delete</strong> methods are not supported.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8c24d-137">Objeto <strong>Procedure</strong></span><span class="sxs-lookup"><span data-stu-id="8c24d-137"><strong>Procedure</strong> object</span></span></p></td>
<td><p><span data-ttu-id="8c24d-138">Não há suporte para a propriedade <strong>Command</strong>.</span><span class="sxs-lookup"><span data-stu-id="8c24d-138">The <strong>Command</strong> property is not supported.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8c24d-139">Coleção <strong>Indexes</strong></span><span class="sxs-lookup"><span data-stu-id="8c24d-139"><strong>Indexes</strong> collection</span></span></p></td>
<td><p><span data-ttu-id="8c24d-140">Não há suporte para os métodos <strong>Append</strong> e <strong>Delete</strong>.</span><span class="sxs-lookup"><span data-stu-id="8c24d-140">The <strong>Append</strong> and <strong>Delete</strong> methods are not supported.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8c24d-141">Coleção <strong>Keys</strong></span><span class="sxs-lookup"><span data-stu-id="8c24d-141"><strong>Keys</strong> collection</span></span></p></td>
<td><p><span data-ttu-id="8c24d-142">Não há suporte para os métodos <strong>Append</strong> e <strong>Delete</strong>.</span><span class="sxs-lookup"><span data-stu-id="8c24d-142">The <strong>Append</strong> and <strong>Delete</strong> methods are not supported.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8c24d-143">Coleção <strong>Users</strong></span><span class="sxs-lookup"><span data-stu-id="8c24d-143"><strong>Users</strong> collection</span></span></p></td>
<td><p><span data-ttu-id="8c24d-144">Não há suporte para <strong>Users</strong>.</span><span class="sxs-lookup"><span data-stu-id="8c24d-144"><strong>Users</strong> is not supported.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8c24d-145">Coleção <strong>Groups</strong></span><span class="sxs-lookup"><span data-stu-id="8c24d-145"><strong>Groups</strong> collection</span></span></p></td>
<td><p><span data-ttu-id="8c24d-146">Não há suporte para <strong>Groups</strong>.</span><span class="sxs-lookup"><span data-stu-id="8c24d-146"><strong>Groups</strong> is not supported.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="microsoft-ole-db-provider-for-oracle"></a><span data-ttu-id="8c24d-147">Microsoft OLE DB Provider for Oracle</span><span class="sxs-lookup"><span data-stu-id="8c24d-147">Microsoft OLE DB Provider for Oracle</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="8c24d-148">Objeto ou coleção</span><span class="sxs-lookup"><span data-stu-id="8c24d-148">Object or Collection</span></span></p></th>
<th><p><span data-ttu-id="8c24d-149">Restrições de uso</span><span class="sxs-lookup"><span data-stu-id="8c24d-149">Usage Restriction</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8c24d-150">Objeto <strong>Catalog</strong></span><span class="sxs-lookup"><span data-stu-id="8c24d-150"><strong>Catalog</strong> object</span></span></p></td>
<td><p><span data-ttu-id="8c24d-151">Não há suporte para o método <strong>Create</strong>.</span><span class="sxs-lookup"><span data-stu-id="8c24d-151">The <strong>Create</strong> method is not supported.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8c24d-152">Coleção <strong>Tables</strong></span><span class="sxs-lookup"><span data-stu-id="8c24d-152"><strong>Tables</strong> collection</span></span></p></td>
<td><p><span data-ttu-id="8c24d-153">Não há suporte para os métodos <strong>Append</strong> e <strong>Delete</strong>.</span><span class="sxs-lookup"><span data-stu-id="8c24d-153">The <strong>Append</strong> and <strong>Delete</strong> methods are not supported.</span></span> <span data-ttu-id="8c24d-154">As propriedades são leitura/gravação antes da criação do objeto, e são somente leitura quando um objeto existente é referenciado.</span><span class="sxs-lookup"><span data-stu-id="8c24d-154">Properties are read/write prior to object creation, and read-only when referencing an existing object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8c24d-155">Coleção <strong>Views</strong></span><span class="sxs-lookup"><span data-stu-id="8c24d-155"><strong>Views</strong> collection</span></span></p></td>
<td><p><span data-ttu-id="8c24d-156">Não há suporte para os métodos <strong>Append</strong> e <strong>Delete</strong>.</span><span class="sxs-lookup"><span data-stu-id="8c24d-156">The <strong>Append</strong> and <strong>Delete</strong> methods are not supported.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8c24d-157">Objeto <strong>View</strong></span><span class="sxs-lookup"><span data-stu-id="8c24d-157"><strong>View</strong> object</span></span></p></td>
<td><p><span data-ttu-id="8c24d-158">Não há suporte para a propriedade <strong>Command</strong>.</span><span class="sxs-lookup"><span data-stu-id="8c24d-158">The <strong>Command</strong> property is not supported.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8c24d-159">Objeto <strong>Procedures</strong></span><span class="sxs-lookup"><span data-stu-id="8c24d-159"><strong>Procedures</strong> object</span></span></p></td>
<td><p><span data-ttu-id="8c24d-160">Não há suporte para os métodos <strong>Append</strong> e <strong>Delete</strong>.</span><span class="sxs-lookup"><span data-stu-id="8c24d-160">The <strong>Append</strong> and <strong>Delete</strong> methods are not supported.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8c24d-161">Objeto <strong>Procedure</strong></span><span class="sxs-lookup"><span data-stu-id="8c24d-161"><strong>Procedure</strong> object</span></span></p></td>
<td><p><span data-ttu-id="8c24d-162">Não há suporte para a propriedade <strong>Command</strong>.</span><span class="sxs-lookup"><span data-stu-id="8c24d-162">The <strong>Command</strong> property is not supported.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8c24d-163">Coleção <strong>Indexes</strong></span><span class="sxs-lookup"><span data-stu-id="8c24d-163"><strong>Indexes</strong> collection</span></span></p></td>
<td><p><span data-ttu-id="8c24d-164">Não há suporte para os métodos <strong>Append</strong> e <strong>Delete</strong>.</span><span class="sxs-lookup"><span data-stu-id="8c24d-164">The <strong>Append</strong> and <strong>Delete</strong> methods are not supported.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8c24d-165">Coleção <strong>Keys</strong></span><span class="sxs-lookup"><span data-stu-id="8c24d-165"><strong>Keys</strong> collection</span></span></p></td>
<td><p><span data-ttu-id="8c24d-166">Não há suporte para os métodos <strong>Append</strong> e <strong>Delete</strong>.</span><span class="sxs-lookup"><span data-stu-id="8c24d-166">The <strong>Append</strong> and <strong>Delete</strong> methods are not supported.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8c24d-167">Coleção <strong>Users</strong></span><span class="sxs-lookup"><span data-stu-id="8c24d-167"><strong>Users</strong> collection</span></span></p></td>
<td><p><span data-ttu-id="8c24d-168">Não há suporte para <strong>Users</strong>.</span><span class="sxs-lookup"><span data-stu-id="8c24d-168"><strong>Users</strong> is not supported.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8c24d-169">Coleção <strong>Groups</strong></span><span class="sxs-lookup"><span data-stu-id="8c24d-169"><strong>Groups</strong> collection</span></span></p></td>
<td><p><span data-ttu-id="8c24d-170">Não há suporte para <strong>Groups</strong>.</span><span class="sxs-lookup"><span data-stu-id="8c24d-170"><strong>Groups</strong> is not supported.</span></span></p></td>
</tr>
</tbody>
</table>

