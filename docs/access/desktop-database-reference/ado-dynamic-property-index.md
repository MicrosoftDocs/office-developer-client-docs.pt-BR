---
title: Índice de propriedades dinâmicas do ADO
TOCTitle: ADO dynamic property index
ms:assetid: 437beced-b97a-894d-b08f-4a322629a5a6
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249202(v=office.15)
ms:contentKeyID: 48544502
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 19b7ddca0395869b5a1dba4182a123d33e54e66d
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/03/2018
ms.locfileid: "25947599"
---
# <a name="ado-dynamic-property-index"></a><span data-ttu-id="3cd66-102">Índice de propriedades dinâmicas do ADO</span><span class="sxs-lookup"><span data-stu-id="3cd66-102">ADO dynamic property index</span></span>

<span data-ttu-id="3cd66-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="3cd66-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="3cd66-p101">Os provedores de dados, provedores de serviços e componentes de serviço podem adicionar propriedades dinâmicas às coleções **Properties** dos objetos [ Connection ](connection-object-ado.md) e [Recordset](recordset-object-ado.md) não abertos. Um determinado provedor também pode inserir propriedades adicionais quando esses objetos estão abertos. Algumas dessas propriedades estão listadas na seção [Propriedades dinâmicas do ADO](ado-dynamic-properties.md). Mais propriedades estão relacionadas nos provedores específicos da seção [Apêndice A: provedores](appendix-a-providers.md).</span><span class="sxs-lookup"><span data-stu-id="3cd66-p101">Data providers, service providers, and service components can add dynamic properties to the **Properties** collections of the unopened [Connection](connection-object-ado.md) and [Recordset](recordset-object-ado.md) objects. A given provider may also insert additional properties when these objects are opened. Some of these properties are listed in the [ADO Dynamic Properties](ado-dynamic-properties.md) section. More are listed under the specific providers in the [Appendix A: Providers](appendix-a-providers.md) section.</span></span>

<span data-ttu-id="3cd66-p102">A tabela abaixo é um índice cruzado dos nomes do ADO e do OLE DB para cada propriedade dinâmica do provedor padrão do OLE DB. Seus provedores podem adicionar mais propriedades. além das relacionadas aqui. Para obter informações específicas sobre as propriedades dinâmicas específicas para o provedor, consulte a documentação do provedor.</span><span class="sxs-lookup"><span data-stu-id="3cd66-p102">The table below is a cross-index of the ADO and OLE DB names for each standard OLE DB provider dynamic property. Your providers may add more properties than listed here. For the specific information about provider-specific dynamic properties, see your provider documentation.</span></span>

<span data-ttu-id="3cd66-p103">A Referência do programador do OLE DB diz respeito a um nome de propriedade do ADO de acordo com o termo, "Descrição." Você pode encontrar mais informações sobre essas propriedades padrão na Referência do programador do OLE DB. Procure o nome da propriedade do OLE DB no índice ou consulte os seguintes tópicos:</span><span class="sxs-lookup"><span data-stu-id="3cd66-p103">The OLE DB Programmer's Reference refers to an ADO property name by the term, "Description." You can find more information about these standard properties in the OLE DB Programmer's Reference. Search for the OLE DB property name in the Index or see the following topics:</span></span>

- <span data-ttu-id="3cd66-114">Apêndice C: propriedades do OLE DB</span><span class="sxs-lookup"><span data-stu-id="3cd66-114">Appendix C: OLE DB Properties</span></span>

- <span data-ttu-id="3cd66-115">Propriedades que contam com suporte do Cursor Service</span><span class="sxs-lookup"><span data-stu-id="3cd66-115">Supported Properties of the Cursor Service</span></span>

- <span data-ttu-id="3cd66-116">Propriedades que contam com suporte do Persistence Provider</span><span class="sxs-lookup"><span data-stu-id="3cd66-116">Supported Properties of the Persistence Provider</span></span>

- <span data-ttu-id="3cd66-117">Propriedades do OLE DB que contam com suporte do Remoting Provider</span><span class="sxs-lookup"><span data-stu-id="3cd66-117">Supported OLE DB Properties of the Remoting Provider</span></span>

## <a name="remarks"></a><span data-ttu-id="3cd66-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="3cd66-118">Remarks</span></span>

<span data-ttu-id="3cd66-119">Observe os números utilizados no índice cruzado:</span><span class="sxs-lookup"><span data-stu-id="3cd66-119">Note numbers used in the cross-index:</span></span>

<span data-ttu-id="3cd66-p104">(1) Esta propriedade é um sinalizador Booleano que indica se a interface nomeada deve ser utilizada. Se existir, o nome da propriedade do OLE DB equivalente será relacionado.</span><span class="sxs-lookup"><span data-stu-id="3cd66-p104">(1) This property is a Boolean flag indicating whether the named interface should be used. The equivalent OLE DB property name is listed if it exists.</span></span>

<span data-ttu-id="3cd66-122">(2) a propriedade "Bookmarkable" ADO é gerado internamente para trás para frente compatibilidade e é mapeado para a propriedade do OLE DB, DBPROP\_IROWSETLOCATE.</span><span class="sxs-lookup"><span data-stu-id="3cd66-122">(2) The "Bookmarkable" ADO property is generated internally for backwards compatibility, and is mapped to the OLE DB property, DBPROP\_IROWSETLOCATE.</span></span> <span data-ttu-id="3cd66-123">Essa é a propriedade que corresponde à propriedade do ADO, IRowsetLocate.</span><span class="sxs-lookup"><span data-stu-id="3cd66-123">This is the same property that corresponds to the ADO property, IRowsetLocate.</span></span>

<span data-ttu-id="3cd66-124">(3) A propriedade do ADO, "Hidden Columns", é nomeada de forma diferente da Descrição do nome da propriedade do OLE DB, "Hidden Columns Count."</span><span class="sxs-lookup"><span data-stu-id="3cd66-124">(3) The ADO property name, "Hidden Columns", is named differently than the OLE DB property name Description, "Hidden Columns Count."</span></span>

<span data-ttu-id="3cd66-p106">(4) Para os conjuntos de registros hierárquicos, a propriedade do ADO, "Maximum Rows", é aplicada em todos os filhos. Dependendo da ordem em que as linhas são retornadas, você poderá ter todos, alguns ou nenhum filho para cada pai ou filhos órfãos no conjunto de resultados. Portanto, ao reorganizar os conjuntos de registros hierárquicos, o identificador para cada filho deverá ser exclusivo. Em geral, o provedor [Microsoft Data Shaping Service para OLE DB (MSDATASHAPE)](microsoft-data-shaping-service-for-ole-db-ado-service-provider.md) não permite distinção entre as propriedades que podem ser herdadas do pai e aquelas que não podem ser herdadas.</span><span class="sxs-lookup"><span data-stu-id="3cd66-p106">(4) For hierarchical recordsets, the "Maximum Rows" ADO property gets applied across all children. Depending on the order in which the rows are returned, you might have all, some or no children for each parent or orphaned children in the result set. Therefore, when reshaping hierarchical recordsets, the identifier for every child should be unique. In general, the [Microsoft Data Shaping Service for OLE DB (MSDATASHAPE)](microsoft-data-shaping-service-for-ole-db-ado-service-provider.md) provider does not allow for distinction between properties that can be inherited from the parent and those that cannot be inherited.</span></span>

<span data-ttu-id="3cd66-129">(5) Não se aplica.</span><span class="sxs-lookup"><span data-stu-id="3cd66-129">(5) Does not apply.</span></span>

<span data-ttu-id="3cd66-130">**Propriedades dinâmicas de conexão**</span><span class="sxs-lookup"><span data-stu-id="3cd66-130">**Connection Dynamic Properties**</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="3cd66-131">Nome da propriedade do ADO</span><span class="sxs-lookup"><span data-stu-id="3cd66-131">ADO Property Name</span></span></p></th>
<th><p><span data-ttu-id="3cd66-132">Nome da propriedade do OLE DB</span><span class="sxs-lookup"><span data-stu-id="3cd66-132">OLE DB Property Name</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3cd66-133">Active Sessions</span><span class="sxs-lookup"><span data-stu-id="3cd66-133">Active Sessions</span></span></p></td>
<td><p><span data-ttu-id="3cd66-134">DBPROP_ACTIVESESSIONS</span><span class="sxs-lookup"><span data-stu-id="3cd66-134">DBPROP_ACTIVESESSIONS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3cd66-135">Asynchable Abort</span><span class="sxs-lookup"><span data-stu-id="3cd66-135">Asynchable Abort</span></span></p></td>
<td><p><span data-ttu-id="3cd66-136">DBPROP_ASYNCTXNABORT</span><span class="sxs-lookup"><span data-stu-id="3cd66-136">DBPROP_ASYNCTXNABORT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3cd66-137">Asynchable Commit</span><span class="sxs-lookup"><span data-stu-id="3cd66-137">Asynchable Commit</span></span></p></td>
<td><p><span data-ttu-id="3cd66-138">DBPROP_ASYNCTNXCOMMIT</span><span class="sxs-lookup"><span data-stu-id="3cd66-138">DBPROP_ASYNCTNXCOMMIT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3cd66-139">Autocommit Isolation Levels</span><span class="sxs-lookup"><span data-stu-id="3cd66-139">Autocommit Isolation Levels</span></span></p></td>
<td><p><span data-ttu-id="3cd66-140">DBPROP_SESS_AUTOCOMMITISOLEVELS</span><span class="sxs-lookup"><span data-stu-id="3cd66-140">DBPROP_SESS_AUTOCOMMITISOLEVELS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3cd66-141">Catalog Location</span><span class="sxs-lookup"><span data-stu-id="3cd66-141">Catalog Location</span></span></p></td>
<td><p><span data-ttu-id="3cd66-142">DBPROP_CATALOGLOCATION</span><span class="sxs-lookup"><span data-stu-id="3cd66-142">DBPROP_CATALOGLOCATION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3cd66-143">Catalog Term</span><span class="sxs-lookup"><span data-stu-id="3cd66-143">Catalog Term</span></span></p></td>
<td><p><span data-ttu-id="3cd66-144">DBPROP_CATALOGTERM</span><span class="sxs-lookup"><span data-stu-id="3cd66-144">DBPROP_CATALOGTERM</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3cd66-145">Column Definition</span><span class="sxs-lookup"><span data-stu-id="3cd66-145">Column Definition</span></span></p></td>
<td><p><span data-ttu-id="3cd66-146">DBPROP_COLUMNDEFINITION</span><span class="sxs-lookup"><span data-stu-id="3cd66-146">DBPROP_COLUMNDEFINITION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3cd66-147">Connect Timeout</span><span class="sxs-lookup"><span data-stu-id="3cd66-147">Connect Timeout</span></span></p></td>
<td><p><span data-ttu-id="3cd66-148">DBPROP_INIT_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="3cd66-148">DBPROP_INIT_TIMEOUT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3cd66-149">Current Catalog</span><span class="sxs-lookup"><span data-stu-id="3cd66-149">Current Catalog</span></span></p></td>
<td><p><span data-ttu-id="3cd66-150">DBPROP_CURRENTCATALOG</span><span class="sxs-lookup"><span data-stu-id="3cd66-150">DBPROP_CURRENTCATALOG</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3cd66-151">Data Source</span><span class="sxs-lookup"><span data-stu-id="3cd66-151">Data Source</span></span></p></td>
<td><p><span data-ttu-id="3cd66-152">DBPROP_INIT_DATASOURCE</span><span class="sxs-lookup"><span data-stu-id="3cd66-152">DBPROP_INIT_DATASOURCE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3cd66-153">Data Source Name</span><span class="sxs-lookup"><span data-stu-id="3cd66-153">Data Source Name</span></span></p></td>
<td><p><span data-ttu-id="3cd66-154">DBPROP_DATASOURCENAME</span><span class="sxs-lookup"><span data-stu-id="3cd66-154">DBPROP_DATASOURCENAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3cd66-155">Data Source Object Threading Model</span><span class="sxs-lookup"><span data-stu-id="3cd66-155">Data Source Object Threading Model</span></span></p></td>
<td><p><span data-ttu-id="3cd66-156">DBPROP_DSOTHREADMODEL</span><span class="sxs-lookup"><span data-stu-id="3cd66-156">DBPROP_DSOTHREADMODEL</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3cd66-157">DBMS Name</span><span class="sxs-lookup"><span data-stu-id="3cd66-157">DBMS Name</span></span></p></td>
<td><p><span data-ttu-id="3cd66-158">DBPROP_DBMSNAME</span><span class="sxs-lookup"><span data-stu-id="3cd66-158">DBPROP_DBMSNAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3cd66-159">DBMS Version</span><span class="sxs-lookup"><span data-stu-id="3cd66-159">DBMS Version</span></span></p></td>
<td><p><span data-ttu-id="3cd66-160">DBPROP_DBMSVER</span><span class="sxs-lookup"><span data-stu-id="3cd66-160">DBPROP_DBMSVER</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3cd66-161">Extended Properties</span><span class="sxs-lookup"><span data-stu-id="3cd66-161">Extended Properties</span></span></p></td>
<td><p><span data-ttu-id="3cd66-162">DBPROP_INIT_PROVIDERSTRING</span><span class="sxs-lookup"><span data-stu-id="3cd66-162">DBPROP_INIT_PROVIDERSTRING</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3cd66-163">GROUP BY Support</span><span class="sxs-lookup"><span data-stu-id="3cd66-163">GROUP BY Support</span></span></p></td>
<td><p><span data-ttu-id="3cd66-164">DBPROP_GROUPBY</span><span class="sxs-lookup"><span data-stu-id="3cd66-164">DBPROP_GROUPBY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3cd66-165">Heterogeneous Table Support</span><span class="sxs-lookup"><span data-stu-id="3cd66-165">Heterogeneous Table Support</span></span></p></td>
<td><p><span data-ttu-id="3cd66-166">DBPROP_HETEROGENEOUSTABLES</span><span class="sxs-lookup"><span data-stu-id="3cd66-166">DBPROP_HETEROGENEOUSTABLES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3cd66-167">Identifier Case Sensitivity</span><span class="sxs-lookup"><span data-stu-id="3cd66-167">Identifier Case Sensitivity</span></span></p></td>
<td><p><span data-ttu-id="3cd66-168">DBPROP_IDENTIFIERCASE</span><span class="sxs-lookup"><span data-stu-id="3cd66-168">DBPROP_IDENTIFIERCASE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3cd66-169">Initial Catalog</span><span class="sxs-lookup"><span data-stu-id="3cd66-169">Initial Catalog</span></span></p></td>
<td><p><span data-ttu-id="3cd66-170">DBPROP_INIT_CATALOG</span><span class="sxs-lookup"><span data-stu-id="3cd66-170">DBPROP_INIT_CATALOG</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3cd66-171">Isolation Levels</span><span class="sxs-lookup"><span data-stu-id="3cd66-171">Isolation Levels</span></span></p></td>
<td><p><span data-ttu-id="3cd66-172">DBPROP_SUPPORTEDTXNISOLEVELS</span><span class="sxs-lookup"><span data-stu-id="3cd66-172">DBPROP_SUPPORTEDTXNISOLEVELS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3cd66-173">Isolation Retention</span><span class="sxs-lookup"><span data-stu-id="3cd66-173">Isolation Retention</span></span></p></td>
<td><p><span data-ttu-id="3cd66-174">DBPROP_SUPPORTEDTXNISORETAIN</span><span class="sxs-lookup"><span data-stu-id="3cd66-174">DBPROP_SUPPORTEDTXNISORETAIN</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3cd66-175">Locale Identifier</span><span class="sxs-lookup"><span data-stu-id="3cd66-175">Locale Identifier</span></span></p></td>
<td><p><span data-ttu-id="3cd66-176">DBPROP_INIT_LCID</span><span class="sxs-lookup"><span data-stu-id="3cd66-176">DBPROP_INIT_LCID</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3cd66-177">Location</span><span class="sxs-lookup"><span data-stu-id="3cd66-177">Location</span></span></p></td>
<td><p><span data-ttu-id="3cd66-178">DBPROP_INIT_LOCATION</span><span class="sxs-lookup"><span data-stu-id="3cd66-178">DBPROP_INIT_LOCATION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3cd66-179">Maximum Index Size</span><span class="sxs-lookup"><span data-stu-id="3cd66-179">Maximum Index Size</span></span></p></td>
<td><p><span data-ttu-id="3cd66-180">DBPROP_MAXINDEXSIZE</span><span class="sxs-lookup"><span data-stu-id="3cd66-180">DBPROP_MAXINDEXSIZE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3cd66-181">Maximum Row Size</span><span class="sxs-lookup"><span data-stu-id="3cd66-181">Maximum Row Size</span></span></p></td>
<td><p><span data-ttu-id="3cd66-182">DBPROP_MAXROWSIZE</span><span class="sxs-lookup"><span data-stu-id="3cd66-182">DBPROP_MAXROWSIZE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3cd66-183">Maximum Row Size Includes BLOB</span><span class="sxs-lookup"><span data-stu-id="3cd66-183">Maximum Row Size Includes BLOB</span></span></p></td>
<td><p><span data-ttu-id="3cd66-184">DBPROP_MAXROWSIZEINCLUDESBLOB</span><span class="sxs-lookup"><span data-stu-id="3cd66-184">DBPROP_MAXROWSIZEINCLUDESBLOB</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3cd66-185">Maximum Tables in SELECT</span><span class="sxs-lookup"><span data-stu-id="3cd66-185">Maximum Tables in SELECT</span></span></p></td>
<td><p><span data-ttu-id="3cd66-186">DBPROP_MAXTABLESINSELECT</span><span class="sxs-lookup"><span data-stu-id="3cd66-186">DBPROP_MAXTABLESINSELECT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3cd66-187">Mode</span><span class="sxs-lookup"><span data-stu-id="3cd66-187">Mode</span></span></p></td>
<td><p><span data-ttu-id="3cd66-188">DBPROP_INIT_MODE</span><span class="sxs-lookup"><span data-stu-id="3cd66-188">DBPROP_INIT_MODE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3cd66-189">Multiple Parameter Sets</span><span class="sxs-lookup"><span data-stu-id="3cd66-189">Multiple Parameter Sets</span></span></p></td>
<td><p><span data-ttu-id="3cd66-190">DBPROP_MULTIPLEPARAMSETS</span><span class="sxs-lookup"><span data-stu-id="3cd66-190">DBPROP_MULTIPLEPARAMSETS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3cd66-191">Multiple Results</span><span class="sxs-lookup"><span data-stu-id="3cd66-191">Multiple Results</span></span></p></td>
<td><p><span data-ttu-id="3cd66-192">DBPROP_MULTIPLERESULTS</span><span class="sxs-lookup"><span data-stu-id="3cd66-192">DBPROP_MULTIPLERESULTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3cd66-193">Multiple Storage Objects</span><span class="sxs-lookup"><span data-stu-id="3cd66-193">Multiple Storage Objects</span></span></p></td>
<td><p><span data-ttu-id="3cd66-194">DBPROP_MULTIPLESTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="3cd66-194">DBPROP_MULTIPLESTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3cd66-195">Multi-Table Update</span><span class="sxs-lookup"><span data-stu-id="3cd66-195">Multi-Table Update</span></span></p></td>
<td><p><span data-ttu-id="3cd66-196">DBPROP_MULTITABLEUPDATE</span><span class="sxs-lookup"><span data-stu-id="3cd66-196">DBPROP_MULTITABLEUPDATE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3cd66-197">NULL Collation Order</span><span class="sxs-lookup"><span data-stu-id="3cd66-197">NULL Collation Order</span></span></p></td>
<td><p><span data-ttu-id="3cd66-198">DBPROP_NULLCOLLATION</span><span class="sxs-lookup"><span data-stu-id="3cd66-198">DBPROP_NULLCOLLATION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3cd66-199">NULL Concatenation Behavior</span><span class="sxs-lookup"><span data-stu-id="3cd66-199">NULL Concatenation Behavior</span></span></p></td>
<td><p><span data-ttu-id="3cd66-200">DBPROP_CONCATNULLBEHAVIOR</span><span class="sxs-lookup"><span data-stu-id="3cd66-200">DBPROP_CONCATNULLBEHAVIOR</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3cd66-201">OLE DB Services</span><span class="sxs-lookup"><span data-stu-id="3cd66-201">OLE DB Services</span></span></p></td>
<td><p><span data-ttu-id="3cd66-202">DBPROP_INIT_OLEDBSERVICES</span><span class="sxs-lookup"><span data-stu-id="3cd66-202">DBPROP_INIT_OLEDBSERVICES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3cd66-203">OLE DB Version</span><span class="sxs-lookup"><span data-stu-id="3cd66-203">OLE DB Version</span></span></p></td>
<td><p><span data-ttu-id="3cd66-204">DBPROP_PROVIDEROLEDBVER</span><span class="sxs-lookup"><span data-stu-id="3cd66-204">DBPROP_PROVIDEROLEDBVER</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3cd66-205">OLE Object Support</span><span class="sxs-lookup"><span data-stu-id="3cd66-205">OLE Object Support</span></span></p></td>
<td><p><span data-ttu-id="3cd66-206">DBPROP_OLEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="3cd66-206">DBPROP_OLEOBJECTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3cd66-207">Open Rowset Support</span><span class="sxs-lookup"><span data-stu-id="3cd66-207">Open Rowset Support</span></span></p></td>
<td><p><span data-ttu-id="3cd66-208">DBPROP_OPENROWSETSUPPORT</span><span class="sxs-lookup"><span data-stu-id="3cd66-208">DBPROP_OPENROWSETSUPPORT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3cd66-209">ORDER BY Columns in Select List</span><span class="sxs-lookup"><span data-stu-id="3cd66-209">ORDER BY Columns in Select List</span></span></p></td>
<td><p><span data-ttu-id="3cd66-210">DBPROP_ORDERBYCOLUMNSINSELECT</span><span class="sxs-lookup"><span data-stu-id="3cd66-210">DBPROP_ORDERBYCOLUMNSINSELECT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3cd66-211">Output Parameter Availability</span><span class="sxs-lookup"><span data-stu-id="3cd66-211">Output Parameter Availability</span></span></p></td>
<td><p><span data-ttu-id="3cd66-212">DBPROP_OUTPUTPARAMETERAVAILABILITY</span><span class="sxs-lookup"><span data-stu-id="3cd66-212">DBPROP_OUTPUTPARAMETERAVAILABILITY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3cd66-213">Pass By Ref Accessors</span><span class="sxs-lookup"><span data-stu-id="3cd66-213">Pass By Ref Accessors</span></span></p></td>
<td><p><span data-ttu-id="3cd66-214">DBPROP_BYREFACCESSORS</span><span class="sxs-lookup"><span data-stu-id="3cd66-214">DBPROP_BYREFACCESSORS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3cd66-215">Password</span><span class="sxs-lookup"><span data-stu-id="3cd66-215">Password</span></span></p></td>
<td><p><span data-ttu-id="3cd66-216">DBPROP_AUTH_PASSWORD</span><span class="sxs-lookup"><span data-stu-id="3cd66-216">DBPROP_AUTH_PASSWORD</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3cd66-217">Persist Security Info</span><span class="sxs-lookup"><span data-stu-id="3cd66-217">Persist Security Info</span></span></p></td>
<td><p><span data-ttu-id="3cd66-218">DBPROP_AUTH_PERSIST_SENSITIVE_AUTHINFO</span><span class="sxs-lookup"><span data-stu-id="3cd66-218">DBPROP_AUTH_PERSIST_SENSITIVE_AUTHINFO</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3cd66-219">Persistent ID Type</span><span class="sxs-lookup"><span data-stu-id="3cd66-219">Persistent ID Type</span></span></p></td>
<td><p><span data-ttu-id="3cd66-220">DBPROP_PERSISTENTIDTYPE</span><span class="sxs-lookup"><span data-stu-id="3cd66-220">DBPROP_PERSISTENTIDTYPE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3cd66-221">Prepare Abort Behavior</span><span class="sxs-lookup"><span data-stu-id="3cd66-221">Prepare Abort Behavior</span></span></p></td>
<td><p><span data-ttu-id="3cd66-222">DBPROP_PREPAREABORTBEHAVIOR</span><span class="sxs-lookup"><span data-stu-id="3cd66-222">DBPROP_PREPAREABORTBEHAVIOR</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3cd66-223">Prepare Commit Behavior</span><span class="sxs-lookup"><span data-stu-id="3cd66-223">Prepare Commit Behavior</span></span></p></td>
<td><p><span data-ttu-id="3cd66-224">DBPROP_PREPARECOMMITBEHAVIOR</span><span class="sxs-lookup"><span data-stu-id="3cd66-224">DBPROP_PREPARECOMMITBEHAVIOR</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3cd66-225">Procedure Term</span><span class="sxs-lookup"><span data-stu-id="3cd66-225">Procedure Term</span></span></p></td>
<td><p><span data-ttu-id="3cd66-226">DBPROP_PROCEDURETERM</span><span class="sxs-lookup"><span data-stu-id="3cd66-226">DBPROP_PROCEDURETERM</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3cd66-227">Prompt</span><span class="sxs-lookup"><span data-stu-id="3cd66-227">Prompt</span></span></p></td>
<td><p><span data-ttu-id="3cd66-228">DBPROP_INIT_PROMPT</span><span class="sxs-lookup"><span data-stu-id="3cd66-228">DBPROP_INIT_PROMPT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3cd66-229">Provider Friendly Name</span><span class="sxs-lookup"><span data-stu-id="3cd66-229">Provider Friendly Name</span></span></p></td>
<td><p><span data-ttu-id="3cd66-230">DBPROP_PROVIDERFRIENDLYNAME</span><span class="sxs-lookup"><span data-stu-id="3cd66-230">DBPROP_PROVIDERFRIENDLYNAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3cd66-231">Provider Name</span><span class="sxs-lookup"><span data-stu-id="3cd66-231">Provider Name</span></span></p></td>
<td><p><span data-ttu-id="3cd66-232">DBPROP_PROVIDERFILENAME</span><span class="sxs-lookup"><span data-stu-id="3cd66-232">DBPROP_PROVIDERFILENAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3cd66-233">Provider Version</span><span class="sxs-lookup"><span data-stu-id="3cd66-233">Provider Version</span></span></p></td>
<td><p><span data-ttu-id="3cd66-234">DBPROP_PROVIDERVER</span><span class="sxs-lookup"><span data-stu-id="3cd66-234">DBPROP_PROVIDERVER</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3cd66-235">Read-Only Data Source</span><span class="sxs-lookup"><span data-stu-id="3cd66-235">Read-Only Data Source</span></span></p></td>
<td><p><span data-ttu-id="3cd66-236">DBPROP_DATASOURCEREADONLY</span><span class="sxs-lookup"><span data-stu-id="3cd66-236">DBPROP_DATASOURCEREADONLY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3cd66-237">Rowset Conversions on Command</span><span class="sxs-lookup"><span data-stu-id="3cd66-237">Rowset Conversions on Command</span></span></p></td>
<td><p><span data-ttu-id="3cd66-238">DBPROP_ROWSETCONVERSIONSONCOMMAND</span><span class="sxs-lookup"><span data-stu-id="3cd66-238">DBPROP_ROWSETCONVERSIONSONCOMMAND</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3cd66-239">Schema Term</span><span class="sxs-lookup"><span data-stu-id="3cd66-239">Schema Term</span></span></p></td>
<td><p><span data-ttu-id="3cd66-240">DBPROP_SCHEMATERM</span><span class="sxs-lookup"><span data-stu-id="3cd66-240">DBPROP_SCHEMATERM</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3cd66-241">Schema Usage</span><span class="sxs-lookup"><span data-stu-id="3cd66-241">Schema Usage</span></span></p></td>
<td><p><span data-ttu-id="3cd66-242">DBPROP_SCHEMAUSAGE</span><span class="sxs-lookup"><span data-stu-id="3cd66-242">DBPROP_SCHEMAUSAGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3cd66-243">SQL Support</span><span class="sxs-lookup"><span data-stu-id="3cd66-243">SQL Support</span></span></p></td>
<td><p><span data-ttu-id="3cd66-244">DBPROP_SQLSUPPORT</span><span class="sxs-lookup"><span data-stu-id="3cd66-244">DBPROP_SQLSUPPORT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3cd66-245">Structured Storage</span><span class="sxs-lookup"><span data-stu-id="3cd66-245">Structured Storage</span></span></p></td>
<td><p><span data-ttu-id="3cd66-246">DBPROP_STRUCTUREDSTORAGE</span><span class="sxs-lookup"><span data-stu-id="3cd66-246">DBPROP_STRUCTUREDSTORAGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3cd66-247">Subquery Support</span><span class="sxs-lookup"><span data-stu-id="3cd66-247">Subquery Support</span></span></p></td>
<td><p><span data-ttu-id="3cd66-248">DBPROP_SUBQUERIES</span><span class="sxs-lookup"><span data-stu-id="3cd66-248">DBPROP_SUBQUERIES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3cd66-249">Table Term</span><span class="sxs-lookup"><span data-stu-id="3cd66-249">Table Term</span></span></p></td>
<td><p><span data-ttu-id="3cd66-250">DBPROP_TABLETERM</span><span class="sxs-lookup"><span data-stu-id="3cd66-250">DBPROP_TABLETERM</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3cd66-251">Transaction DDL</span><span class="sxs-lookup"><span data-stu-id="3cd66-251">Transaction DDL</span></span></p></td>
<td><p><span data-ttu-id="3cd66-252">DBPROP_SUPPORTEDTXNDDL</span><span class="sxs-lookup"><span data-stu-id="3cd66-252">DBPROP_SUPPORTEDTXNDDL</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3cd66-253">User ID</span><span class="sxs-lookup"><span data-stu-id="3cd66-253">User ID</span></span></p></td>
<td><p><span data-ttu-id="3cd66-254">DBPROP_AUTH_USERID</span><span class="sxs-lookup"><span data-stu-id="3cd66-254">DBPROP_AUTH_USERID</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3cd66-255">User Name</span><span class="sxs-lookup"><span data-stu-id="3cd66-255">User Name</span></span></p></td>
<td><p><span data-ttu-id="3cd66-256">DBPROP_USERNAME</span><span class="sxs-lookup"><span data-stu-id="3cd66-256">DBPROP_USERNAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3cd66-257">Window Handle</span><span class="sxs-lookup"><span data-stu-id="3cd66-257">Window Handle</span></span></p></td>
<td><p><span data-ttu-id="3cd66-258">DBPROP_INIT_HWND</span><span class="sxs-lookup"><span data-stu-id="3cd66-258">DBPROP_INIT_HWND</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="3cd66-259">**Propriedades dinâmicas do Recordset**</span><span class="sxs-lookup"><span data-stu-id="3cd66-259">**Recordset Dynamic Properties**</span></span>

<span data-ttu-id="3cd66-260">Observe que as **Propriedades Dinâmicas** do objeto **Recordset** ficam fora do escopo (tornam-se indisponíveis) quando o **Recordset** é fechado.</span><span class="sxs-lookup"><span data-stu-id="3cd66-260">Note that the **Dynamic Properties** of the **Recordset** object go out of scope (become unavailable) when the **Recordset** is closed.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="3cd66-261">Nome da propriedade do ADO</span><span class="sxs-lookup"><span data-stu-id="3cd66-261">ADO Property Name</span></span></p></th>
<th><p><span data-ttu-id="3cd66-262">Nome da propriedade do OLE DB</span><span class="sxs-lookup"><span data-stu-id="3cd66-262">OLE DB Property Name</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3cd66-263">IAccessor</span><span class="sxs-lookup"><span data-stu-id="3cd66-263">IAccessor</span></span></p></td>
<td><p><span data-ttu-id="3cd66-264">DBPROP_IACCESSOR (1)</span><span class="sxs-lookup"><span data-stu-id="3cd66-264">DBPROP_IACCESSOR (1)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3cd66-265">IChapteredRowset</span><span class="sxs-lookup"><span data-stu-id="3cd66-265">IChapteredRowset</span></span></p></td>
<td><p><span data-ttu-id="3cd66-266">(1)</span><span class="sxs-lookup"><span data-stu-id="3cd66-266">(1)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3cd66-267">IColumnsInfo</span><span class="sxs-lookup"><span data-stu-id="3cd66-267">IColumnsInfo</span></span></p></td>
<td><p><span data-ttu-id="3cd66-268">DBPROP_ICOLUMNSINFO (1)</span><span class="sxs-lookup"><span data-stu-id="3cd66-268">DBPROP_ICOLUMNSINFO (1)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3cd66-269">IColumnsRowset</span><span class="sxs-lookup"><span data-stu-id="3cd66-269">IColumnsRowset</span></span></p></td>
<td><p><span data-ttu-id="3cd66-270">DBPROP_ICOLUMNSROWSET (1)</span><span class="sxs-lookup"><span data-stu-id="3cd66-270">DBPROP_ICOLUMNSROWSET (1)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3cd66-271">IConnectionPointContainer</span><span class="sxs-lookup"><span data-stu-id="3cd66-271">IConnectionPointContainer</span></span></p></td>
<td><p><span data-ttu-id="3cd66-272">DBPROP_ICONNECTIONPOINTCONTAINER (1)</span><span class="sxs-lookup"><span data-stu-id="3cd66-272">DBPROP_ICONNECTIONPOINTCONTAINER (1)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3cd66-273">IConvertType</span><span class="sxs-lookup"><span data-stu-id="3cd66-273">IConvertType</span></span></p></td>
<td><p><span data-ttu-id="3cd66-274">(1)</span><span class="sxs-lookup"><span data-stu-id="3cd66-274">(1)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3cd66-275">ILockBytes</span><span class="sxs-lookup"><span data-stu-id="3cd66-275">ILockBytes</span></span></p></td>
<td><p><span data-ttu-id="3cd66-276">DBPROP_ILOCKBYTES (1)</span><span class="sxs-lookup"><span data-stu-id="3cd66-276">DBPROP_ILOCKBYTES (1)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3cd66-277">IRowset</span><span class="sxs-lookup"><span data-stu-id="3cd66-277">IRowset</span></span></p></td>
<td><p><span data-ttu-id="3cd66-278">DBPROP_IROWSET (1)</span><span class="sxs-lookup"><span data-stu-id="3cd66-278">DBPROP_IROWSET (1)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3cd66-279">IDBAsynchStatus</span><span class="sxs-lookup"><span data-stu-id="3cd66-279">IDBAsynchStatus</span></span></p></td>
<td><p><span data-ttu-id="3cd66-280">DBPROP_IDBASYNCHSTATUS (1)</span><span class="sxs-lookup"><span data-stu-id="3cd66-280">DBPROP_IDBASYNCHSTATUS (1)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3cd66-281">IParentRowset</span><span class="sxs-lookup"><span data-stu-id="3cd66-281">IParentRowset</span></span></p></td>
<td><p><span data-ttu-id="3cd66-282">(1)</span><span class="sxs-lookup"><span data-stu-id="3cd66-282">(1)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3cd66-283">IRowsetChange</span><span class="sxs-lookup"><span data-stu-id="3cd66-283">IRowsetChange</span></span></p></td>
<td><p><span data-ttu-id="3cd66-284">DBPROP_IROWSETCHANGE (1)</span><span class="sxs-lookup"><span data-stu-id="3cd66-284">DBPROP_IROWSETCHANGE (1)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3cd66-285">IRowsetExactScroll</span><span class="sxs-lookup"><span data-stu-id="3cd66-285">IRowsetExactScroll</span></span></p></td>
<td><p><span data-ttu-id="3cd66-286">(1)</span><span class="sxs-lookup"><span data-stu-id="3cd66-286">(1)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3cd66-287">IRowsetFind</span><span class="sxs-lookup"><span data-stu-id="3cd66-287">IRowsetFind</span></span></p></td>
<td><p><span data-ttu-id="3cd66-288">DBPROP_IROWSETFIND (1)</span><span class="sxs-lookup"><span data-stu-id="3cd66-288">DBPROP_IROWSETFIND (1)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3cd66-289">IRowsetIdentity</span><span class="sxs-lookup"><span data-stu-id="3cd66-289">IRowsetIdentity</span></span></p></td>
<td><p><span data-ttu-id="3cd66-290">DBPROP_IROWSETIDENTITY (1)</span><span class="sxs-lookup"><span data-stu-id="3cd66-290">DBPROP_IROWSETIDENTITY (1)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3cd66-291">IRowsetInfo</span><span class="sxs-lookup"><span data-stu-id="3cd66-291">IRowsetInfo</span></span></p></td>
<td><p><span data-ttu-id="3cd66-292">DBPROP_IROWSETINFO (1)</span><span class="sxs-lookup"><span data-stu-id="3cd66-292">DBPROP_IROWSETINFO (1)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3cd66-293">IRowsetLocate</span><span class="sxs-lookup"><span data-stu-id="3cd66-293">IRowsetLocate</span></span></p></td>
<td><p><span data-ttu-id="3cd66-294">DBPROP_IROWSETLOCATE (1)</span><span class="sxs-lookup"><span data-stu-id="3cd66-294">DBPROP_IROWSETLOCATE (1)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3cd66-295">IRowsetRefresh</span><span class="sxs-lookup"><span data-stu-id="3cd66-295">IRowsetRefresh</span></span></p></td>
<td><p><span data-ttu-id="3cd66-296">DBPROP_IROWSETREFRESH (1)</span><span class="sxs-lookup"><span data-stu-id="3cd66-296">DBPROP_IROWSETREFRESH (1)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3cd66-297">IRowsetResynch</span><span class="sxs-lookup"><span data-stu-id="3cd66-297">IRowsetResynch</span></span></p></td>
<td><p><span data-ttu-id="3cd66-298">(1)</span><span class="sxs-lookup"><span data-stu-id="3cd66-298">(1)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3cd66-299">IRowsetScroll</span><span class="sxs-lookup"><span data-stu-id="3cd66-299">IRowsetScroll</span></span></p></td>
<td><p><span data-ttu-id="3cd66-300">DBPROP_IROWSETSCROLL (1)</span><span class="sxs-lookup"><span data-stu-id="3cd66-300">DBPROP_IROWSETSCROLL (1)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3cd66-301">IRowsetUpdate</span><span class="sxs-lookup"><span data-stu-id="3cd66-301">IRowsetUpdate</span></span></p></td>
<td><p><span data-ttu-id="3cd66-302">DBPROP_IROWSETUPDATE (1)</span><span class="sxs-lookup"><span data-stu-id="3cd66-302">DBPROP_IROWSETUPDATE (1)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3cd66-303">IRowsetView</span><span class="sxs-lookup"><span data-stu-id="3cd66-303">IRowsetView</span></span></p></td>
<td><p><span data-ttu-id="3cd66-304">DBPROP_IROWSETVIEW (1)</span><span class="sxs-lookup"><span data-stu-id="3cd66-304">DBPROP_IROWSETVIEW (1)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3cd66-305">IRowsetIndex</span><span class="sxs-lookup"><span data-stu-id="3cd66-305">IRowsetIndex</span></span></p></td>
<td><p><span data-ttu-id="3cd66-306">DBPROP_IROWSETINDEX (1)</span><span class="sxs-lookup"><span data-stu-id="3cd66-306">DBPROP_IROWSETINDEX (1)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3cd66-307">ISequentialStream</span><span class="sxs-lookup"><span data-stu-id="3cd66-307">ISequentialStream</span></span></p></td>
<td><p><span data-ttu-id="3cd66-308">DBPROP_ISEQUENTIALSTREAM (1)</span><span class="sxs-lookup"><span data-stu-id="3cd66-308">DBPROP_ISEQUENTIALSTREAM (1)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3cd66-309">IStorage</span><span class="sxs-lookup"><span data-stu-id="3cd66-309">IStorage</span></span></p></td>
<td><p><span data-ttu-id="3cd66-310">DBPROP_ISTORAGE (1)</span><span class="sxs-lookup"><span data-stu-id="3cd66-310">DBPROP_ISTORAGE (1)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3cd66-311">IStream</span><span class="sxs-lookup"><span data-stu-id="3cd66-311">IStream</span></span></p></td>
<td><p><span data-ttu-id="3cd66-312">DBPROP_ISTREAM (1)</span><span class="sxs-lookup"><span data-stu-id="3cd66-312">DBPROP_ISTREAM (1)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3cd66-313">ISupportErrorInfo</span><span class="sxs-lookup"><span data-stu-id="3cd66-313">ISupportErrorInfo</span></span></p></td>
<td><p><span data-ttu-id="3cd66-314">DBPROP_ISUPPORTERRORINFO (1)</span><span class="sxs-lookup"><span data-stu-id="3cd66-314">DBPROP_ISUPPORTERRORINFO (1)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3cd66-315">Access Order</span><span class="sxs-lookup"><span data-stu-id="3cd66-315">Access Order</span></span></p></td>
<td><p><span data-ttu-id="3cd66-316">DBPROP_ACCESSORDER</span><span class="sxs-lookup"><span data-stu-id="3cd66-316">DBPROP_ACCESSORDER</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3cd66-317">Append-Only Rowset</span><span class="sxs-lookup"><span data-stu-id="3cd66-317">Append-Only Rowset</span></span></p></td>
<td><p><span data-ttu-id="3cd66-318">DBPROP_APPENDONLY</span><span class="sxs-lookup"><span data-stu-id="3cd66-318">DBPROP_APPENDONLY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3cd66-319">Asynchronous Rowset Processing</span><span class="sxs-lookup"><span data-stu-id="3cd66-319">Asynchronous Rowset Processing</span></span></p></td>
<td><p><span data-ttu-id="3cd66-320">DBPROP_ROWSET_ASYNCH</span><span class="sxs-lookup"><span data-stu-id="3cd66-320">DBPROP_ROWSET_ASYNCH</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3cd66-321">Auto Recalc</span><span class="sxs-lookup"><span data-stu-id="3cd66-321">Auto Recalc</span></span></p></td>
<td><p><span data-ttu-id="3cd66-322">DBPROP_ADC_AUTORECALC</span><span class="sxs-lookup"><span data-stu-id="3cd66-322">DBPROP_ADC_AUTORECALC</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3cd66-323">Background Fetch Size</span><span class="sxs-lookup"><span data-stu-id="3cd66-323">Background Fetch Size</span></span></p></td>
<td><p><span data-ttu-id="3cd66-324">DBPROP_ASYNCHFETCHSIZE</span><span class="sxs-lookup"><span data-stu-id="3cd66-324">DBPROP_ASYNCHFETCHSIZE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3cd66-325">Background Thread Priority</span><span class="sxs-lookup"><span data-stu-id="3cd66-325">Background Thread Priority</span></span></p></td>
<td><p><span data-ttu-id="3cd66-326">DBPROP_ASYNCHTHREADPRIORITY</span><span class="sxs-lookup"><span data-stu-id="3cd66-326">DBPROP_ASYNCHTHREADPRIORITY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3cd66-327">Batch Size</span><span class="sxs-lookup"><span data-stu-id="3cd66-327">Batch Size</span></span></p></td>
<td><p><span data-ttu-id="3cd66-328">DBPROP_ADC_BATCHSIZE</span><span class="sxs-lookup"><span data-stu-id="3cd66-328">DBPROP_ADC_BATCHSIZE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3cd66-329">Blocking Storage Objects</span><span class="sxs-lookup"><span data-stu-id="3cd66-329">Blocking Storage Objects</span></span></p></td>
<td><p><span data-ttu-id="3cd66-330">DBPROP_BLOCKINGSTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="3cd66-330">DBPROP_BLOCKINGSTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3cd66-331">Bookmark Type</span><span class="sxs-lookup"><span data-stu-id="3cd66-331">Bookmark Type</span></span></p></td>
<td><p><span data-ttu-id="3cd66-332">DBPROP_BOOKMARKTYPE</span><span class="sxs-lookup"><span data-stu-id="3cd66-332">DBPROP_BOOKMARKTYPE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3cd66-333">Bookmarkable</span><span class="sxs-lookup"><span data-stu-id="3cd66-333">Bookmarkable</span></span></p></td>
<td><p><span data-ttu-id="3cd66-334">DBPROP_IROWSETLOCATE (2)</span><span class="sxs-lookup"><span data-stu-id="3cd66-334">DBPROP_IROWSETLOCATE (2)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3cd66-335">Bookmarks Ordered</span><span class="sxs-lookup"><span data-stu-id="3cd66-335">Bookmarks Ordered</span></span></p></td>
<td><p><span data-ttu-id="3cd66-336">DBPROP_ORDEREDBOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="3cd66-336">DBPROP_ORDEREDBOOKMARKS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3cd66-337">Cache Child Rows</span><span class="sxs-lookup"><span data-stu-id="3cd66-337">Cache Child Rows</span></span></p></td>
<td><p><span data-ttu-id="3cd66-338">DBPROP_ADC_CACHECHILDROWS</span><span class="sxs-lookup"><span data-stu-id="3cd66-338">DBPROP_ADC_CACHECHILDROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3cd66-339">Cache Deferred Columns</span><span class="sxs-lookup"><span data-stu-id="3cd66-339">Cache Deferred Columns</span></span></p></td>
<td><p><span data-ttu-id="3cd66-340">DBPROP_CACHEDEFERRED</span><span class="sxs-lookup"><span data-stu-id="3cd66-340">DBPROP_CACHEDEFERRED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3cd66-341">Change Inserted Rows</span><span class="sxs-lookup"><span data-stu-id="3cd66-341">Change Inserted Rows</span></span></p></td>
<td><p><span data-ttu-id="3cd66-342">DBPROP_CHANGEINSERTEDROWS</span><span class="sxs-lookup"><span data-stu-id="3cd66-342">DBPROP_CHANGEINSERTEDROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3cd66-343">Column Privileges</span><span class="sxs-lookup"><span data-stu-id="3cd66-343">Column Privileges</span></span></p></td>
<td><p><span data-ttu-id="3cd66-344">DBPROP_COLUMNRESTRICT</span><span class="sxs-lookup"><span data-stu-id="3cd66-344">DBPROP_COLUMNRESTRICT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3cd66-345">Column Set Notification</span><span class="sxs-lookup"><span data-stu-id="3cd66-345">Column Set Notification</span></span></p></td>
<td><p><span data-ttu-id="3cd66-346">DBPROP_NOTIFYCOLUMNSET</span><span class="sxs-lookup"><span data-stu-id="3cd66-346">DBPROP_NOTIFYCOLUMNSET</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3cd66-347">Column Writable</span><span class="sxs-lookup"><span data-stu-id="3cd66-347">Column Writable</span></span></p></td>
<td><p><span data-ttu-id="3cd66-348">DBPROP_MAYWRITECOLUMN</span><span class="sxs-lookup"><span data-stu-id="3cd66-348">DBPROP_MAYWRITECOLUMN</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3cd66-349">Command Time Out</span><span class="sxs-lookup"><span data-stu-id="3cd66-349">Command Time Out</span></span></p></td>
<td><p><span data-ttu-id="3cd66-350">DBPROP_COMMANDTIMEOUT</span><span class="sxs-lookup"><span data-stu-id="3cd66-350">DBPROP_COMMANDTIMEOUT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3cd66-351">Cursor Engine Version</span><span class="sxs-lookup"><span data-stu-id="3cd66-351">Cursor Engine Version</span></span></p></td>
<td><p><span data-ttu-id="3cd66-352">DBPROP_ADC_CEVER</span><span class="sxs-lookup"><span data-stu-id="3cd66-352">DBPROP_ADC_CEVER</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3cd66-353">Defer Column</span><span class="sxs-lookup"><span data-stu-id="3cd66-353">Defer Column</span></span></p></td>
<td><p><span data-ttu-id="3cd66-354">DBPROP_DEFERRED</span><span class="sxs-lookup"><span data-stu-id="3cd66-354">DBPROP_DEFERRED</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3cd66-355">Delay Storage Object Updates</span><span class="sxs-lookup"><span data-stu-id="3cd66-355">Delay Storage Object Updates</span></span></p></td>
<td><p><span data-ttu-id="3cd66-356">DBPROP_DELAYSTORAGEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="3cd66-356">DBPROP_DELAYSTORAGEOBJECTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3cd66-357">Fetch Backwards</span><span class="sxs-lookup"><span data-stu-id="3cd66-357">Fetch Backwards</span></span></p></td>
<td><p><span data-ttu-id="3cd66-358">DBPROP_CANFETCHBACKWARDS</span><span class="sxs-lookup"><span data-stu-id="3cd66-358">DBPROP_CANFETCHBACKWARDS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3cd66-359">Filter Operations</span><span class="sxs-lookup"><span data-stu-id="3cd66-359">Filter Operations</span></span></p></td>
<td><p><span data-ttu-id="3cd66-360">DBPROP_FILTERCOMPAREOPS</span><span class="sxs-lookup"><span data-stu-id="3cd66-360">DBPROP_FILTERCOMPAREOPS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3cd66-361">Find Operations</span><span class="sxs-lookup"><span data-stu-id="3cd66-361">Find Operations</span></span></p></td>
<td><p><span data-ttu-id="3cd66-362">DBPROP_FINDCOMPAREOPS</span><span class="sxs-lookup"><span data-stu-id="3cd66-362">DBPROP_FINDCOMPAREOPS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3cd66-363">Hidden Columns (Count)</span><span class="sxs-lookup"><span data-stu-id="3cd66-363">Hidden Columns (Count)</span></span></p></td>
<td><p><span data-ttu-id="3cd66-364">DBPROP_HIDDENCOLUMNS (3)</span><span class="sxs-lookup"><span data-stu-id="3cd66-364">DBPROP_HIDDENCOLUMNS (3)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3cd66-365">Hold Rows</span><span class="sxs-lookup"><span data-stu-id="3cd66-365">Hold Rows</span></span></p></td>
<td><p><span data-ttu-id="3cd66-366">DBPROP_CANHOLDROWS</span><span class="sxs-lookup"><span data-stu-id="3cd66-366">DBPROP_CANHOLDROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3cd66-367">Immobile Rows</span><span class="sxs-lookup"><span data-stu-id="3cd66-367">Immobile Rows</span></span></p></td>
<td><p><span data-ttu-id="3cd66-368">DBPROP_IMMOBILEROWS</span><span class="sxs-lookup"><span data-stu-id="3cd66-368">DBPROP_IMMOBILEROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3cd66-369">Initial Fetch Size</span><span class="sxs-lookup"><span data-stu-id="3cd66-369">Initial Fetch Size</span></span></p></td>
<td><p><span data-ttu-id="3cd66-370">DBPROP_ASYNCHPREFETCHSIZE</span><span class="sxs-lookup"><span data-stu-id="3cd66-370">DBPROP_ASYNCHPREFETCHSIZE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3cd66-371">Literal Bookmarks</span><span class="sxs-lookup"><span data-stu-id="3cd66-371">Literal Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="3cd66-372">DBPROP_LITERALBOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="3cd66-372">DBPROP_LITERALBOOKMARKS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3cd66-373">Literal Row Identity</span><span class="sxs-lookup"><span data-stu-id="3cd66-373">Literal Row Identity</span></span></p></td>
<td><p><span data-ttu-id="3cd66-374">DBPROP_LITERALIDENTITY</span><span class="sxs-lookup"><span data-stu-id="3cd66-374">DBPROP_LITERALIDENTITY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3cd66-375">Maintain Change Status</span><span class="sxs-lookup"><span data-stu-id="3cd66-375">Maintain Change Status</span></span></p></td>
<td><p><span data-ttu-id="3cd66-376">DBPROP_ADC_MAINTAINCHANGESTATUS</span><span class="sxs-lookup"><span data-stu-id="3cd66-376">DBPROP_ADC_MAINTAINCHANGESTATUS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3cd66-377">Maximum Open Rows</span><span class="sxs-lookup"><span data-stu-id="3cd66-377">Maximum Open Rows</span></span></p></td>
<td><p><span data-ttu-id="3cd66-378">DBPROP_MAXOPENROWS</span><span class="sxs-lookup"><span data-stu-id="3cd66-378">DBPROP_MAXOPENROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3cd66-379">Maximum Pending Rows</span><span class="sxs-lookup"><span data-stu-id="3cd66-379">Maximum Pending Rows</span></span></p></td>
<td><p><span data-ttu-id="3cd66-380">DBPROP_MAXPENDINGROWS</span><span class="sxs-lookup"><span data-stu-id="3cd66-380">DBPROP_MAXPENDINGROWS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3cd66-381">Maximum Rows</span><span class="sxs-lookup"><span data-stu-id="3cd66-381">Maximum Rows</span></span></p></td>
<td><p><span data-ttu-id="3cd66-382">DBPROP_MAXROWS (4)</span><span class="sxs-lookup"><span data-stu-id="3cd66-382">DBPROP_MAXROWS (4)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3cd66-383">Memory Usage</span><span class="sxs-lookup"><span data-stu-id="3cd66-383">Memory Usage</span></span></p></td>
<td><p><span data-ttu-id="3cd66-384">DBPROP_MEMORYUSAGE</span><span class="sxs-lookup"><span data-stu-id="3cd66-384">DBPROP_MEMORYUSAGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3cd66-385">Notification Granularity</span><span class="sxs-lookup"><span data-stu-id="3cd66-385">Notification Granularity</span></span></p></td>
<td><p><span data-ttu-id="3cd66-386">DBPROP_NOTIFICATIONGRANULARITY</span><span class="sxs-lookup"><span data-stu-id="3cd66-386">DBPROP_NOTIFICATIONGRANULARITY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3cd66-387">Notification Phases</span><span class="sxs-lookup"><span data-stu-id="3cd66-387">Notification Phases</span></span></p></td>
<td><p><span data-ttu-id="3cd66-388">DBPROP_NOTIFICATIONPHASES</span><span class="sxs-lookup"><span data-stu-id="3cd66-388">DBPROP_NOTIFICATIONPHASES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3cd66-389">Objects Transacted</span><span class="sxs-lookup"><span data-stu-id="3cd66-389">Objects Transacted</span></span></p></td>
<td><p><span data-ttu-id="3cd66-390">DBPROP_TRANSACTEDOBJECT</span><span class="sxs-lookup"><span data-stu-id="3cd66-390">DBPROP_TRANSACTEDOBJECT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3cd66-391">Others' Changes Visible</span><span class="sxs-lookup"><span data-stu-id="3cd66-391">Others' Changes Visible</span></span></p></td>
<td><p><span data-ttu-id="3cd66-392">DBPROP_OTHERUPDATEDELETE</span><span class="sxs-lookup"><span data-stu-id="3cd66-392">DBPROP_OTHERUPDATEDELETE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3cd66-393">Others' Inserts Visible</span><span class="sxs-lookup"><span data-stu-id="3cd66-393">Others' Inserts Visible</span></span></p></td>
<td><p><span data-ttu-id="3cd66-394">DBPROP_OTHERINSERT</span><span class="sxs-lookup"><span data-stu-id="3cd66-394">DBPROP_OTHERINSERT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3cd66-395">Own Changes Visible</span><span class="sxs-lookup"><span data-stu-id="3cd66-395">Own Changes Visible</span></span></p></td>
<td><p><span data-ttu-id="3cd66-396">DBPROP_OWNUPDATEDELETE</span><span class="sxs-lookup"><span data-stu-id="3cd66-396">DBPROP_OWNUPDATEDELETE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3cd66-397">Own Inserts Visible</span><span class="sxs-lookup"><span data-stu-id="3cd66-397">Own Inserts Visible</span></span></p></td>
<td><p><span data-ttu-id="3cd66-398">DBPROP_OWNINSERT</span><span class="sxs-lookup"><span data-stu-id="3cd66-398">DBPROP_OWNINSERT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3cd66-399">Preserve on Abort</span><span class="sxs-lookup"><span data-stu-id="3cd66-399">Preserve on Abort</span></span></p></td>
<td><p><span data-ttu-id="3cd66-400">DBPROP_ABORTPRESERVE</span><span class="sxs-lookup"><span data-stu-id="3cd66-400">DBPROP_ABORTPRESERVE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3cd66-401">Preserve on Commit</span><span class="sxs-lookup"><span data-stu-id="3cd66-401">Preserve on Commit</span></span></p></td>
<td><p><span data-ttu-id="3cd66-402">DBPROP_COMMITPRESERVE</span><span class="sxs-lookup"><span data-stu-id="3cd66-402">DBPROP_COMMITPRESERVE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3cd66-403">Private1</span><span class="sxs-lookup"><span data-stu-id="3cd66-403">Private1</span></span></p></td>
<td><p><span data-ttu-id="3cd66-404">(5)</span><span class="sxs-lookup"><span data-stu-id="3cd66-404">(5)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3cd66-405">Quick Restart</span><span class="sxs-lookup"><span data-stu-id="3cd66-405">Quick Restart</span></span></p></td>
<td><p><span data-ttu-id="3cd66-406">DBPROP_QUICKRESTART</span><span class="sxs-lookup"><span data-stu-id="3cd66-406">DBPROP_QUICKRESTART</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3cd66-407">Reentrant Events</span><span class="sxs-lookup"><span data-stu-id="3cd66-407">Reentrant Events</span></span></p></td>
<td><p><span data-ttu-id="3cd66-408">DBPROP_REENTRANTEVENTS</span><span class="sxs-lookup"><span data-stu-id="3cd66-408">DBPROP_REENTRANTEVENTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3cd66-409">Remove Deleted Rows</span><span class="sxs-lookup"><span data-stu-id="3cd66-409">Remove Deleted Rows</span></span></p></td>
<td><p><span data-ttu-id="3cd66-410">DBPROP_REMOVEDELETED</span><span class="sxs-lookup"><span data-stu-id="3cd66-410">DBPROP_REMOVEDELETED</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3cd66-411">Report Multiple Changes</span><span class="sxs-lookup"><span data-stu-id="3cd66-411">Report Multiple Changes</span></span></p></td>
<td><p><span data-ttu-id="3cd66-412">DBPROP_REPORTMULTIPLECHANGES</span><span class="sxs-lookup"><span data-stu-id="3cd66-412">DBPROP_REPORTMULTIPLECHANGES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3cd66-413">Reshape Name</span><span class="sxs-lookup"><span data-stu-id="3cd66-413">Reshape Name</span></span></p></td>
<td><p><span data-ttu-id="3cd66-414">DBPROP_ADC_RESHAPENAME</span><span class="sxs-lookup"><span data-stu-id="3cd66-414">DBPROP_ADC_RESHAPENAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3cd66-415">Resync Command</span><span class="sxs-lookup"><span data-stu-id="3cd66-415">Resync Command</span></span></p></td>
<td><p><span data-ttu-id="3cd66-416">DBPROP_ADC_CUSTOMRESYNCH</span><span class="sxs-lookup"><span data-stu-id="3cd66-416">DBPROP_ADC_CUSTOMRESYNCH</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3cd66-417">Return Pending Inserts</span><span class="sxs-lookup"><span data-stu-id="3cd66-417">Return Pending Inserts</span></span></p></td>
<td><p><span data-ttu-id="3cd66-418">DBPROP_RETURNPENDINGINSERTS</span><span class="sxs-lookup"><span data-stu-id="3cd66-418">DBPROP_RETURNPENDINGINSERTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3cd66-419">Row Delete Notification</span><span class="sxs-lookup"><span data-stu-id="3cd66-419">Row Delete Notification</span></span></p></td>
<td><p><span data-ttu-id="3cd66-420">DBPROP_NOTIFYROWDELETE</span><span class="sxs-lookup"><span data-stu-id="3cd66-420">DBPROP_NOTIFYROWDELETE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3cd66-421">Row First Change Notification</span><span class="sxs-lookup"><span data-stu-id="3cd66-421">Row First Change Notification</span></span></p></td>
<td><p><span data-ttu-id="3cd66-422">DBPROP_NOTIFYROWFIRSTCHANGE</span><span class="sxs-lookup"><span data-stu-id="3cd66-422">DBPROP_NOTIFYROWFIRSTCHANGE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3cd66-423">Row Insert Notification</span><span class="sxs-lookup"><span data-stu-id="3cd66-423">Row Insert Notification</span></span></p></td>
<td><p><span data-ttu-id="3cd66-424">DBPROP_NOTIFYROWINSERT</span><span class="sxs-lookup"><span data-stu-id="3cd66-424">DBPROP_NOTIFYROWINSERT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3cd66-425">Row Privileges</span><span class="sxs-lookup"><span data-stu-id="3cd66-425">Row Privileges</span></span></p></td>
<td><p><span data-ttu-id="3cd66-426">DBPROP_ROWRESTRICT</span><span class="sxs-lookup"><span data-stu-id="3cd66-426">DBPROP_ROWRESTRICT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3cd66-427">Row Resynchronization Notification</span><span class="sxs-lookup"><span data-stu-id="3cd66-427">Row Resynchronization Notification</span></span></p></td>
<td><p><span data-ttu-id="3cd66-428">DBPROP_NOTIFYROWRESYNCH</span><span class="sxs-lookup"><span data-stu-id="3cd66-428">DBPROP_NOTIFYROWRESYNCH</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3cd66-429">Row Threading Model</span><span class="sxs-lookup"><span data-stu-id="3cd66-429">Row Threading Model</span></span></p></td>
<td><p><span data-ttu-id="3cd66-430">DBPROP_ROWTHREADMODEL</span><span class="sxs-lookup"><span data-stu-id="3cd66-430">DBPROP_ROWTHREADMODEL</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3cd66-431">Row Undo Change Notification</span><span class="sxs-lookup"><span data-stu-id="3cd66-431">Row Undo Change Notification</span></span></p></td>
<td><p><span data-ttu-id="3cd66-432">DBPROP_NOTIFYROWUNDOCHANGE</span><span class="sxs-lookup"><span data-stu-id="3cd66-432">DBPROP_NOTIFYROWUNDOCHANGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3cd66-433">Row Undo Delete Notification</span><span class="sxs-lookup"><span data-stu-id="3cd66-433">Row Undo Delete Notification</span></span></p></td>
<td><p><span data-ttu-id="3cd66-434">DBPROP_NOTIFYROWUNDODELETE</span><span class="sxs-lookup"><span data-stu-id="3cd66-434">DBPROP_NOTIFYROWUNDODELETE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3cd66-435">Row Undo Insert Notification</span><span class="sxs-lookup"><span data-stu-id="3cd66-435">Row Undo Insert Notification</span></span></p></td>
<td><p><span data-ttu-id="3cd66-436">DBPROP_NOTIFYROWUNDOINSERT</span><span class="sxs-lookup"><span data-stu-id="3cd66-436">DBPROP_NOTIFYROWUNDOINSERT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3cd66-437">Row Update Notification</span><span class="sxs-lookup"><span data-stu-id="3cd66-437">Row Update Notification</span></span></p></td>
<td><p><span data-ttu-id="3cd66-438">DBPROP_NOTIFYROWUPDATE</span><span class="sxs-lookup"><span data-stu-id="3cd66-438">DBPROP_NOTIFYROWUPDATE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3cd66-439">Rowset Fetch Position Change Notification</span><span class="sxs-lookup"><span data-stu-id="3cd66-439">Rowset Fetch Position Change Notification</span></span></p></td>
<td><p><span data-ttu-id="3cd66-440">DBPROP_NOTIFYROWSETFETCHPOSITIONCHANGE</span><span class="sxs-lookup"><span data-stu-id="3cd66-440">DBPROP_NOTIFYROWSETFETCHPOSITIONCHANGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3cd66-441">Rowset Release Notification</span><span class="sxs-lookup"><span data-stu-id="3cd66-441">Rowset Release Notification</span></span></p></td>
<td><p><span data-ttu-id="3cd66-442">DBPROP_NOTIFYROWSETRELEASE</span><span class="sxs-lookup"><span data-stu-id="3cd66-442">DBPROP_NOTIFYROWSETRELEASE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3cd66-443">Scroll Backwards</span><span class="sxs-lookup"><span data-stu-id="3cd66-443">Scroll Backwards</span></span></p></td>
<td><p><span data-ttu-id="3cd66-444">DBPROP_CANSCROLLBACKWARDS</span><span class="sxs-lookup"><span data-stu-id="3cd66-444">DBPROP_CANSCROLLBACKWARDS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3cd66-445">Server Cursor</span><span class="sxs-lookup"><span data-stu-id="3cd66-445">Server Cursor</span></span></p></td>
<td><p><span data-ttu-id="3cd66-446">DBPROP_SERVERCURSOR</span><span class="sxs-lookup"><span data-stu-id="3cd66-446">DBPROP_SERVERCURSOR</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3cd66-447">Skip Deleted Bookmarks</span><span class="sxs-lookup"><span data-stu-id="3cd66-447">Skip Deleted Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="3cd66-448">DBPROP_BOOKMARKSKIPPED</span><span class="sxs-lookup"><span data-stu-id="3cd66-448">DBPROP_BOOKMARKSKIPPED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3cd66-449">Strong Row Identity</span><span class="sxs-lookup"><span data-stu-id="3cd66-449">Strong Row Identity</span></span></p></td>
<td><p><span data-ttu-id="3cd66-450">DBPROP_STRONGIDENTITY</span><span class="sxs-lookup"><span data-stu-id="3cd66-450">DBPROP_STRONGIDENTITY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3cd66-451">Unique Catalog</span><span class="sxs-lookup"><span data-stu-id="3cd66-451">Unique Catalog</span></span></p></td>
<td><p><span data-ttu-id="3cd66-452">DBPROP_ADC_UNIQUECATALOG</span><span class="sxs-lookup"><span data-stu-id="3cd66-452">DBPROP_ADC_UNIQUECATALOG</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3cd66-453">Unique Rows</span><span class="sxs-lookup"><span data-stu-id="3cd66-453">Unique Rows</span></span></p></td>
<td><p><span data-ttu-id="3cd66-454">DBPROP_UNIQUEROWS</span><span class="sxs-lookup"><span data-stu-id="3cd66-454">DBPROP_UNIQUEROWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3cd66-455">Unique Schema</span><span class="sxs-lookup"><span data-stu-id="3cd66-455">Unique Schema</span></span></p></td>
<td><p><span data-ttu-id="3cd66-456">DBPROP_ADC_UNIQUESCHEMA</span><span class="sxs-lookup"><span data-stu-id="3cd66-456">DBPROP_ADC_UNIQUESCHEMA</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3cd66-457">Unique Table</span><span class="sxs-lookup"><span data-stu-id="3cd66-457">Unique Table</span></span></p></td>
<td><p><span data-ttu-id="3cd66-458">DBPROP_ADC_UNIQUETABLE</span><span class="sxs-lookup"><span data-stu-id="3cd66-458">DBPROP_ADC_UNIQUETABLE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3cd66-459">Updatability</span><span class="sxs-lookup"><span data-stu-id="3cd66-459">Updatability</span></span></p></td>
<td><p><span data-ttu-id="3cd66-460">DBPROP_UPDATABILITY</span><span class="sxs-lookup"><span data-stu-id="3cd66-460">DBPROP_UPDATABILITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3cd66-461">Update Criteria</span><span class="sxs-lookup"><span data-stu-id="3cd66-461">Update Criteria</span></span></p></td>
<td><p><span data-ttu-id="3cd66-462">DBPROP_ADC_UPDATECRITERIA</span><span class="sxs-lookup"><span data-stu-id="3cd66-462">DBPROP_ADC_UPDATECRITERIA</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3cd66-463">Update Resync</span><span class="sxs-lookup"><span data-stu-id="3cd66-463">Update Resync</span></span></p></td>
<td><p><span data-ttu-id="3cd66-464">DBPROP_ADC_UPDATERESYNC</span><span class="sxs-lookup"><span data-stu-id="3cd66-464">DBPROP_ADC_UPDATERESYNC</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3cd66-465">Use Bookmarks</span><span class="sxs-lookup"><span data-stu-id="3cd66-465">Use Bookmarks</span></span></p></td>
<td><p><span data-ttu-id="3cd66-466">DBPROP_BOOKMARKS</span><span class="sxs-lookup"><span data-stu-id="3cd66-466">DBPROP_BOOKMARKS</span></span></p></td>
</tr>
</tbody>
</table>

