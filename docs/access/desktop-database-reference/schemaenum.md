---
title: SchemaEnum (referência do banco de dados de área de trabalho do Access)
TOCTitle: SchemaEnum
ms:assetid: 6147b682-3c4f-ea91-fff6-ac73107d206d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249359(v=office.15)
ms:contentKeyID: 48545208
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: aa70f275de164716b5b3975b56588e9dc4aec1a5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308860"
---
# <a name="schemaenum"></a><span data-ttu-id="6a4c1-102">SchemaEnum</span><span class="sxs-lookup"><span data-stu-id="6a4c1-102">SchemaEnum</span></span>

<span data-ttu-id="6a4c1-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="6a4c1-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="6a4c1-104">Especifica o tipo de esquema do **Recordset** que o método [OpenSchema](openschema-method-ado.md) recupera.</span><span class="sxs-lookup"><span data-stu-id="6a4c1-104">Specifies the type of schema **Recordset** that the [OpenSchema](openschema-method-ado.md) method retrieves.</span></span>

## <a name="remarks"></a><span data-ttu-id="6a4c1-105">Comentários</span><span class="sxs-lookup"><span data-stu-id="6a4c1-105">Remarks</span></span>

<span data-ttu-id="6a4c1-106">Informações adicionais sobre a função e as colunas retornadas para cada constante do ADO podem ser encontradas nos tópicos do Apêndice B do manual *OLE DB Programmers Reference (Referência para programadores do OLE DB)*.</span><span class="sxs-lookup"><span data-stu-id="6a4c1-106">Additional information about the function and columns returned for each ADO constant can be found in topics of Appendix B of the *OLE DB Programmers Reference*.</span></span> <span data-ttu-id="6a4c1-107">O nome de cada tópico está listado entre parênteses na seção Descrição da tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="6a4c1-107">The name of each topic is listed in parentheses in the Description section of the following table.</span></span>

<span data-ttu-id="6a4c1-108">Informações adicionais sobre a função e as colunas retornadas para cada constante do ADO MD podem ser encontradas nos tópicos do Capítulo 23 da documentação *OLE DB for OLAP (OLE DB para OLAP)*.</span><span class="sxs-lookup"><span data-stu-id="6a4c1-108">Additional information about the function and columns returned for each ADO MD constant can be found in topics of Chapter 23 of the *OLE DB for OLAP* documentation.</span></span> <span data-ttu-id="6a4c1-109">O nome de cada tópico está listado entre parênteses e marcado com um asterisco (\*) na coluna Descrição da tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="6a4c1-109">The name of each topic is listed in parentheses and marked with an asterisk (\*) in the Description column of the following table.</span></span>

<span data-ttu-id="6a4c1-110">Converta os tipos de dados das colunas na documentação OLE DB para tipos de dados do ADO, consultando a coluna Descrição do tópico ADO [DataTypeEnum](datatypeenum.md).</span><span class="sxs-lookup"><span data-stu-id="6a4c1-110">Translate the data types of columns in the OLE DB documentation to ADO data types by referring to the Description column of the ADO [DataTypeEnum](datatypeenum.md) topic.</span></span> <span data-ttu-id="6a4c1-111">Por exemplo, um tipo de dados OLE DB **de\_DbType WSTR** é equivalente a um tipo de dados do ADO de **adWChar**.</span><span class="sxs-lookup"><span data-stu-id="6a4c1-111">For example, an OLE DB data type of **DBTYPE\_WSTR** is equivalent to an ADO data type of **adWChar**.</span></span>

<span data-ttu-id="6a4c1-112">O ADO gera resultados como esquema para as constantes **adSchemaDBInfoKeywords** e **adSchemaDBInfoLiterals**.</span><span class="sxs-lookup"><span data-stu-id="6a4c1-112">ADO generates schema-like results for the constants, **adSchemaDBInfoKeywords** and **adSchemaDBInfoLiterals**.</span></span> <span data-ttu-id="6a4c1-113">O ADO cria um **Recordset**e, em seguida, preenche cada linha com os valores retornados respectivamente pelos métodos **IDBInfo::** GetKeywords e **IDBInfo:: GetLiteralInfo** .</span><span class="sxs-lookup"><span data-stu-id="6a4c1-113">ADO creates a **Recordset**, and then fills each row with the values returned respectively by the **IDBInfo::GetKeywords** and **IDBInfo::GetLiteralInfo** methods.</span></span> <span data-ttu-id="6a4c1-114">Informações adicionais sobre esses métodos podem ser encontradas na seção IDBInfo da *referência do programador do OLE DB*.</span><span class="sxs-lookup"><span data-stu-id="6a4c1-114">Additional information about these methods can be found in the IDBInfo section of the *OLE DB Programmer's Reference*.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="6a4c1-115">Constant</span><span class="sxs-lookup"><span data-stu-id="6a4c1-115">Constant</span></span></p></th>
<th><p><span data-ttu-id="6a4c1-116">Valor</span><span class="sxs-lookup"><span data-stu-id="6a4c1-116">Value</span></span></p></th>
<th><p><span data-ttu-id="6a4c1-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="6a4c1-117">Description</span></span></p></th>
<th><p><span data-ttu-id="6a4c1-118">Colunas de restrição</span><span class="sxs-lookup"><span data-stu-id="6a4c1-118">Constraint columns</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6a4c1-119"><strong>adSchemaAsserts</strong></span><span class="sxs-lookup"><span data-stu-id="6a4c1-119"><strong>adSchemaAsserts</strong></span></span></p></td>
<td><p><span data-ttu-id="6a4c1-120">,0</span><span class="sxs-lookup"><span data-stu-id="6a4c1-120">0</span></span></p></td>
<td><p><span data-ttu-id="6a4c1-121">Retorna as asserções definidas no catálogo, pertencentes a um usuário específico.</span><span class="sxs-lookup"><span data-stu-id="6a4c1-121">Returns the assertions defined in the catalog that are owned by a given user.</span></span> <span data-ttu-id="6a4c1-122">(Conjunto de linhas ASSERTIONS)</span><span class="sxs-lookup"><span data-stu-id="6a4c1-122">(ASSERTIONS Rowset)</span></span></p></td>
<td><p><span data-ttu-id="6a4c1-123">CONSTRAINT_CATALOG</span><span class="sxs-lookup"><span data-stu-id="6a4c1-123">CONSTRAINT_CATALOG</span></span><br />
<span data-ttu-id="6a4c1-124">CONSTRAINT_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="6a4c1-124">CONSTRAINT_SCHEMA</span></span><br />
<span data-ttu-id="6a4c1-125">CONSTRAINT_NAME</span><span class="sxs-lookup"><span data-stu-id="6a4c1-125">CONSTRAINT_NAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6a4c1-126"><strong>adSchemaCatalogs</strong></span><span class="sxs-lookup"><span data-stu-id="6a4c1-126"><strong>adSchemaCatalogs</strong></span></span></p></td>
<td><p><span data-ttu-id="6a4c1-127">1</span><span class="sxs-lookup"><span data-stu-id="6a4c1-127">1</span></span></p></td>
<td><p><span data-ttu-id="6a4c1-128">Retorna os atributos físicos associados aos catálogos acessíveis do DBMS.</span><span class="sxs-lookup"><span data-stu-id="6a4c1-128">Returns the physical attributes associated with catalogs accessible from the DBMS.</span></span> <span data-ttu-id="6a4c1-129">(Conjunto de linhas CATALOGS)</span><span class="sxs-lookup"><span data-stu-id="6a4c1-129">(CATALOGS Rowset)</span></span></p></td>
<td><p><span data-ttu-id="6a4c1-130">CATALOG_NAME</span><span class="sxs-lookup"><span data-stu-id="6a4c1-130">CATALOG_NAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6a4c1-131"><strong>adSchemaCharacterSets</strong></span><span class="sxs-lookup"><span data-stu-id="6a4c1-131"><strong>adSchemaCharacterSets</strong></span></span></p></td>
<td><p><span data-ttu-id="6a4c1-132">duas</span><span class="sxs-lookup"><span data-stu-id="6a4c1-132">2</span></span></p></td>
<td><p><span data-ttu-id="6a4c1-133">Retorna os conjuntos de caracteres definidos no catálogo que estão acessíveis para um determinado usuário.</span><span class="sxs-lookup"><span data-stu-id="6a4c1-133">Returns the character sets defined in the catalog that are accessible to a given user.</span></span> <span data-ttu-id="6a4c1-134">(Conjunto de linhas CHARACTER_SETS)</span><span class="sxs-lookup"><span data-stu-id="6a4c1-134">(CHARACTER_SETS Rowset)</span></span></p></td>
<td><p><span data-ttu-id="6a4c1-135">CHARACTER_SET_CATALOG</span><span class="sxs-lookup"><span data-stu-id="6a4c1-135">CHARACTER_SET_CATALOG</span></span><br />
<span data-ttu-id="6a4c1-136">CHARACTER_SET_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="6a4c1-136">CHARACTER_SET_SCHEMA</span></span><br />
<span data-ttu-id="6a4c1-137">CHARACTER_SET_NAME</span><span class="sxs-lookup"><span data-stu-id="6a4c1-137">CHARACTER_SET_NAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6a4c1-138"><strong>adSchemaCheckConstraints</strong></span><span class="sxs-lookup"><span data-stu-id="6a4c1-138"><strong>adSchemaCheckConstraints</strong></span></span></p></td>
<td><p><span data-ttu-id="6a4c1-139">0,5</span><span class="sxs-lookup"><span data-stu-id="6a4c1-139">5</span></span></p></td>
<td><p><span data-ttu-id="6a4c1-140">Retorna as restrições de verificação definidas no catálogo, pertencentes a um usuário específico.</span><span class="sxs-lookup"><span data-stu-id="6a4c1-140">Returns the check constraints defined in the catalog that are owned by a given user.</span></span> <span data-ttu-id="6a4c1-141">(Conjunto de linhas CHECK_CONSTRAINTS)</span><span class="sxs-lookup"><span data-stu-id="6a4c1-141">(CHECK_CONSTRAINTS Rowset)</span></span></p></td>
<td><p><span data-ttu-id="6a4c1-142">CONSTRAINT_CATALOG</span><span class="sxs-lookup"><span data-stu-id="6a4c1-142">CONSTRAINT_CATALOG</span></span><br />
<span data-ttu-id="6a4c1-143">CONSTRAINT_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="6a4c1-143">CONSTRAINT_SCHEMA</span></span><br />
<span data-ttu-id="6a4c1-144">CONSTRAINT_NAME</span><span class="sxs-lookup"><span data-stu-id="6a4c1-144">CONSTRAINT_NAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6a4c1-145"><strong>adSchemaCollations</strong></span><span class="sxs-lookup"><span data-stu-id="6a4c1-145"><strong>adSchemaCollations</strong></span></span></p></td>
<td><p><span data-ttu-id="6a4c1-146">3D</span><span class="sxs-lookup"><span data-stu-id="6a4c1-146">3</span></span></p></td>
<td><p><span data-ttu-id="6a4c1-147">Retorna as coleções de caracteres definidas no catálogo que estão acessíveis para um determinado usuário.</span><span class="sxs-lookup"><span data-stu-id="6a4c1-147">Returns the character collations defined in the catalog that are accessible to a given user.</span></span> <span data-ttu-id="6a4c1-148">(Conjunto de linhas COLLATIONS)</span><span class="sxs-lookup"><span data-stu-id="6a4c1-148">(COLLATIONS Rowset)</span></span></p></td>
<td><p><span data-ttu-id="6a4c1-149">COLLATION_CATALOG</span><span class="sxs-lookup"><span data-stu-id="6a4c1-149">COLLATION_CATALOG</span></span><br />
<span data-ttu-id="6a4c1-150">COLLATION_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="6a4c1-150">COLLATION_SCHEMA</span></span><br />
<span data-ttu-id="6a4c1-151">COLLATION_NAME</span><span class="sxs-lookup"><span data-stu-id="6a4c1-151">COLLATION_NAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6a4c1-152"><strong>adSchemaColumnPrivileges</strong></span><span class="sxs-lookup"><span data-stu-id="6a4c1-152"><strong>adSchemaColumnPrivileges</strong></span></span></p></td>
<td><p><span data-ttu-id="6a4c1-153">Treze</span><span class="sxs-lookup"><span data-stu-id="6a4c1-153">13</span></span></p></td>
<td><p><span data-ttu-id="6a4c1-154">Retorna, nas colunas das tabelas definidas no catálogo, os privilégios que estão disponíveis para um determinado usuário ou foram concedidos a ele.</span><span class="sxs-lookup"><span data-stu-id="6a4c1-154">Returns the privileges on columns of tables defined in the catalog that are available to, or granted by, a given user.</span></span> <span data-ttu-id="6a4c1-155">(Conjunto de linhas COLUMN_PRIVILEGES)</span><span class="sxs-lookup"><span data-stu-id="6a4c1-155">(COLUMN_PRIVILEGES Rowset)</span></span></p></td>
<td><p><span data-ttu-id="6a4c1-156">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="6a4c1-156">TABLE_CATALOG</span></span><br />
<span data-ttu-id="6a4c1-157">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="6a4c1-157">TABLE_SCHEMA</span></span><br />
<span data-ttu-id="6a4c1-158">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="6a4c1-158">TABLE_NAME</span></span><br />
<span data-ttu-id="6a4c1-159">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="6a4c1-159">COLUMN_NAME</span></span><br />
<span data-ttu-id="6a4c1-160">CESSO</span><span class="sxs-lookup"><span data-stu-id="6a4c1-160">GRANTOR</span></span><br />
<span data-ttu-id="6a4c1-161">GRANTEE</span><span class="sxs-lookup"><span data-stu-id="6a4c1-161">GRANTEE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6a4c1-162"><strong>adSchemaColumns</strong></span><span class="sxs-lookup"><span data-stu-id="6a4c1-162"><strong>adSchemaColumns</strong></span></span></p></td>
<td><p><span data-ttu-id="6a4c1-163">quatro</span><span class="sxs-lookup"><span data-stu-id="6a4c1-163">4</span></span></p></td>
<td><p><span data-ttu-id="6a4c1-164">Retorna as colunas das tabelas (inclusive as exibições) definidas no catálogo que estão acessíveis para um determinado usuário.</span><span class="sxs-lookup"><span data-stu-id="6a4c1-164">Returns the columns of tables (including views) defined in the catalog that are accessible to a given user.</span></span> <span data-ttu-id="6a4c1-165">(Conjunto de linhas COLUMNS)</span><span class="sxs-lookup"><span data-stu-id="6a4c1-165">(COLUMNS Rowset)</span></span></p></td>
<td><p><span data-ttu-id="6a4c1-166">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="6a4c1-166">TABLE_CATALOG</span></span><br />
<span data-ttu-id="6a4c1-167">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="6a4c1-167">TABLE_SCHEMA</span></span><br />
<span data-ttu-id="6a4c1-168">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="6a4c1-168">TABLE_NAME</span></span><br />
<span data-ttu-id="6a4c1-169">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="6a4c1-169">COLUMN_NAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6a4c1-170"><strong>adSchemaColumnsDomainUsage</strong></span><span class="sxs-lookup"><span data-stu-id="6a4c1-170"><strong>adSchemaColumnsDomainUsage</strong></span></span></p></td>
<td><p><span data-ttu-id="6a4c1-171">11</span><span class="sxs-lookup"><span data-stu-id="6a4c1-171">11</span></span></p></td>
<td><p><span data-ttu-id="6a4c1-172">Retorna as colunas definidas no catálogo que são dependentes de um domínio definido no catálogo e pertencem a um determinado usuário.</span><span class="sxs-lookup"><span data-stu-id="6a4c1-172">Returns the columns defined in the catalog that are dependent on a domain defined in the catalog and owned by a given user.</span></span> <span data-ttu-id="6a4c1-173">(Conjunto de linhas COLUMN_DOMAIN_USAGE)</span><span class="sxs-lookup"><span data-stu-id="6a4c1-173">(COLUMN_DOMAIN_USAGE Rowset)</span></span></p></td>
<td><p><span data-ttu-id="6a4c1-174">DOMAIN_CATALOG</span><span class="sxs-lookup"><span data-stu-id="6a4c1-174">DOMAIN_CATALOG</span></span><br />
<span data-ttu-id="6a4c1-175">DOMAIN_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="6a4c1-175">DOMAIN_SCHEMA</span></span><br />
<span data-ttu-id="6a4c1-176">\\</span><span class="sxs-lookup"><span data-stu-id="6a4c1-176">DOMAIN_NAME</span></span><br />
<span data-ttu-id="6a4c1-177">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="6a4c1-177">COLUMN_NAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6a4c1-178"><strong>adSchemaConstraintColumnUsage</strong></span><span class="sxs-lookup"><span data-stu-id="6a4c1-178"><strong>adSchemaConstraintColumnUsage</strong></span></span></p></td>
<td><p><span data-ttu-id="6a4c1-179">6</span><span class="sxs-lookup"><span data-stu-id="6a4c1-179">6</span></span></p></td>
<td><p><span data-ttu-id="6a4c1-180">Retorna as colunas usadas por restrições de referência, restrições exclusivas, restrições de verificação e asserções, definidas no catálogo e pertencentes a um usuário específico.</span><span class="sxs-lookup"><span data-stu-id="6a4c1-180">Returns the columns used by referential constraints, unique constraints, check constraints, and assertions, defined in the catalog and owned by a given user.</span></span> <span data-ttu-id="6a4c1-181">(Conjunto de linhas CONSTRAINT_COLUMN_USAGE)</span><span class="sxs-lookup"><span data-stu-id="6a4c1-181">(CONSTRAINT_COLUMN_USAGE Rowset)</span></span></p></td>
<td><p><span data-ttu-id="6a4c1-182">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="6a4c1-182">TABLE_CATALOG</span></span><br />
<span data-ttu-id="6a4c1-183">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="6a4c1-183">TABLE_SCHEMA</span></span><br />
<span data-ttu-id="6a4c1-184">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="6a4c1-184">TABLE_NAME</span></span><br />
<span data-ttu-id="6a4c1-185">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="6a4c1-185">COLUMN_NAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6a4c1-186"><strong>adSchemaConstraintTableUsage</strong></span><span class="sxs-lookup"><span data-stu-id="6a4c1-186"><strong>adSchemaConstraintTableUsage</strong></span></span></p></td>
<td><p><span data-ttu-id="6a4c1-187">178</span><span class="sxs-lookup"><span data-stu-id="6a4c1-187">7</span></span></p></td>
<td><p><span data-ttu-id="6a4c1-188">Retorna as tabelas usadas por restrições de referência, restrições exclusivas, restrições de verificação e asserções, definidas no catálogo e pertencentes a um usuário específico.</span><span class="sxs-lookup"><span data-stu-id="6a4c1-188">Returns the tables that are used by referential constraints, unique constraints, check constraints, and assertions defined in the catalog and owned by a given user.</span></span> <span data-ttu-id="6a4c1-189">(Conjunto de linhas CONSTRAINT_TABLE_USAGE)</span><span class="sxs-lookup"><span data-stu-id="6a4c1-189">(CONSTRAINT_TABLE_USAGE Rowset)</span></span></p></td>
<td><p><span data-ttu-id="6a4c1-190">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="6a4c1-190">TABLE_CATALOG</span></span><br />
<span data-ttu-id="6a4c1-191">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="6a4c1-191">TABLE_SCHEMA</span></span><br />
<span data-ttu-id="6a4c1-192">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="6a4c1-192">TABLE_NAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6a4c1-193"><strong>adSchemaCubes</strong></span><span class="sxs-lookup"><span data-stu-id="6a4c1-193"><strong>adSchemaCubes</strong></span></span></p></td>
<td><p><span data-ttu-id="6a4c1-194">32</span><span class="sxs-lookup"><span data-stu-id="6a4c1-194">32</span></span></p></td>
<td><p><span data-ttu-id="6a4c1-195">Retorna informações sobre os cubos disponíveis em um esquema (ou o catálogo se o provedor não oferecer suporte a esquemas).</span><span class="sxs-lookup"><span data-stu-id="6a4c1-195">Returns information about the available cubes in a schema (or the catalog, if the provider does not support schemas).</span></span> <span data-ttu-id="6a4c1-196">(Conjunto de linhas CUBES\*)</span><span class="sxs-lookup"><span data-stu-id="6a4c1-196">(CUBES Rowset\*)</span></span></p></td>
<td><p><span data-ttu-id="6a4c1-197">CATALOG_NAME</span><span class="sxs-lookup"><span data-stu-id="6a4c1-197">CATALOG_NAME</span></span><br />
<span data-ttu-id="6a4c1-198">SCHEMA_NAME</span><span class="sxs-lookup"><span data-stu-id="6a4c1-198">SCHEMA_NAME</span></span><br />
<span data-ttu-id="6a4c1-199">CUBE_NAME</span><span class="sxs-lookup"><span data-stu-id="6a4c1-199">CUBE_NAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6a4c1-200"><strong>adSchemaDBInfoKeywords</strong></span><span class="sxs-lookup"><span data-stu-id="6a4c1-200"><strong>adSchemaDBInfoKeywords</strong></span></span></p></td>
<td><p><span data-ttu-id="6a4c1-201">até</span><span class="sxs-lookup"><span data-stu-id="6a4c1-201">30</span></span></p></td>
<td><p><span data-ttu-id="6a4c1-202">Retorna uma lista de palavras-chave específicas do provedor.</span><span class="sxs-lookup"><span data-stu-id="6a4c1-202">Returns a list of provider-specific keywords.</span></span> <span data-ttu-id="6a4c1-203">(IDBInfo:: getKeywords \*)</span><span class="sxs-lookup"><span data-stu-id="6a4c1-203">(IDBInfo::GetKeywords \*)</span></span></p></td>
<td><p><span data-ttu-id="6a4c1-204">&lt;Nenhum&gt;</span><span class="sxs-lookup"><span data-stu-id="6a4c1-204">&lt;None&gt;</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6a4c1-205"><strong>adSchemaDBInfoLiterals</strong></span><span class="sxs-lookup"><span data-stu-id="6a4c1-205"><strong>adSchemaDBInfoLiterals</strong></span></span></p></td>
<td><p><span data-ttu-id="6a4c1-206">31</span><span class="sxs-lookup"><span data-stu-id="6a4c1-206">31</span></span></p></td>
<td><p><span data-ttu-id="6a4c1-207">Retorna uma lista de literais específicos do provedor utilizados em comandos de texto.</span><span class="sxs-lookup"><span data-stu-id="6a4c1-207">Returns a list of provider-specific literals used in text commands.</span></span> <span data-ttu-id="6a4c1-208">(IDBInfo:: GetLiteralInfo \*)</span><span class="sxs-lookup"><span data-stu-id="6a4c1-208">(IDBInfo::GetLiteralInfo \*)</span></span></p></td>
<td><p><span data-ttu-id="6a4c1-209">&lt;Nenhum&gt;</span><span class="sxs-lookup"><span data-stu-id="6a4c1-209">&lt;None&gt;</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6a4c1-210"><strong>adSchemaDimensions</strong></span><span class="sxs-lookup"><span data-stu-id="6a4c1-210"><strong>adSchemaDimensions</strong></span></span></p></td>
<td><p><span data-ttu-id="6a4c1-211">33</span><span class="sxs-lookup"><span data-stu-id="6a4c1-211">33</span></span></p></td>
<td><p><span data-ttu-id="6a4c1-212">Retorna informações sobre as dimensões em um determinado cubo.</span><span class="sxs-lookup"><span data-stu-id="6a4c1-212">Returns information about the dimensions in a given cube.</span></span> <span data-ttu-id="6a4c1-213">Ele tem uma linha para cada dimensão.</span><span class="sxs-lookup"><span data-stu-id="6a4c1-213">It has one row for each dimension.</span></span> <span data-ttu-id="6a4c1-214">(Conjunto de linhas DIMENSIONS\*)</span><span class="sxs-lookup"><span data-stu-id="6a4c1-214">(DIMENSIONS Rowset \*)</span></span></p></td>
<td><p><span data-ttu-id="6a4c1-215">CATALOG_NAME</span><span class="sxs-lookup"><span data-stu-id="6a4c1-215">CATALOG_NAME</span></span><br />
<span data-ttu-id="6a4c1-216">SCHEMA_NAME</span><span class="sxs-lookup"><span data-stu-id="6a4c1-216">SCHEMA_NAME</span></span><br />
<span data-ttu-id="6a4c1-217">CUBE_NAME</span><span class="sxs-lookup"><span data-stu-id="6a4c1-217">CUBE_NAME</span></span><br />
<span data-ttu-id="6a4c1-218">DIMENSION_NAME</span><span class="sxs-lookup"><span data-stu-id="6a4c1-218">DIMENSION_NAME</span></span><br />
<span data-ttu-id="6a4c1-219">DIMENSION_UNIQUE_NAME</span><span class="sxs-lookup"><span data-stu-id="6a4c1-219">DIMENSION_UNIQUE_NAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6a4c1-220"><strong>adSchemaForeignKeys</strong></span><span class="sxs-lookup"><span data-stu-id="6a4c1-220"><strong>adSchemaForeignKeys</strong></span></span></p></td>
<td><p><span data-ttu-id="6a4c1-221">27</span><span class="sxs-lookup"><span data-stu-id="6a4c1-221">27</span></span></p></td>
<td><p><span data-ttu-id="6a4c1-222">Retorna as colunas de chave estrangeira definidas no catálogo por um determinado usuário.</span><span class="sxs-lookup"><span data-stu-id="6a4c1-222">Returns the foreign key columns defined in the catalog by a given user.</span></span> <span data-ttu-id="6a4c1-223">(Conjunto de linhas FOREIGN_KEYS)</span><span class="sxs-lookup"><span data-stu-id="6a4c1-223">(FOREIGN_KEYS Rowset)</span></span></p></td>
<td><p><span data-ttu-id="6a4c1-224">PK_TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="6a4c1-224">PK_TABLE_CATALOG</span></span><br />
<span data-ttu-id="6a4c1-225">PK_TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="6a4c1-225">PK_TABLE_SCHEMA</span></span><br />
<span data-ttu-id="6a4c1-226">PK_TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="6a4c1-226">PK_TABLE_NAME</span></span><br />
<span data-ttu-id="6a4c1-227">FK_TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="6a4c1-227">FK_TABLE_CATALOG</span></span><br />
<span data-ttu-id="6a4c1-228">FK_TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="6a4c1-228">FK_TABLE_SCHEMA</span></span><br />
<span data-ttu-id="6a4c1-229">FK_TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="6a4c1-229">FK_TABLE_NAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6a4c1-230"><strong>adSchemaHierarchies</strong></span><span class="sxs-lookup"><span data-stu-id="6a4c1-230"><strong>adSchemaHierarchies</strong></span></span></p></td>
<td><p><span data-ttu-id="6a4c1-231">34</span><span class="sxs-lookup"><span data-stu-id="6a4c1-231">34</span></span></p></td>
<td><p><span data-ttu-id="6a4c1-232">Retorna informações sobre as hierarquias disponíveis em uma dimensão.</span><span class="sxs-lookup"><span data-stu-id="6a4c1-232">Returns information about the hierarchies available in a dimension.</span></span> <span data-ttu-id="6a4c1-233">(Conjunto de linhas HIERARCHIES\*)</span><span class="sxs-lookup"><span data-stu-id="6a4c1-233">(HIERARCHIES Rowset \*)</span></span></p></td>
<td><p><span data-ttu-id="6a4c1-234">CATALOG_NAME</span><span class="sxs-lookup"><span data-stu-id="6a4c1-234">CATALOG_NAME</span></span><br />
<span data-ttu-id="6a4c1-235">SCHEMA_NAME</span><span class="sxs-lookup"><span data-stu-id="6a4c1-235">SCHEMA_NAME</span></span><br />
<span data-ttu-id="6a4c1-236">CUBE_NAME</span><span class="sxs-lookup"><span data-stu-id="6a4c1-236">CUBE_NAME</span></span><br />
<span data-ttu-id="6a4c1-237">DIMENSION_UNIQUE_NAME</span><span class="sxs-lookup"><span data-stu-id="6a4c1-237">DIMENSION_UNIQUE_NAME</span></span><br />
<span data-ttu-id="6a4c1-238">HIERARCHY_NAME</span><span class="sxs-lookup"><span data-stu-id="6a4c1-238">HIERARCHY_NAME</span></span><br />
<span data-ttu-id="6a4c1-239">HIERARCHY_UNIQUE_NAME</span><span class="sxs-lookup"><span data-stu-id="6a4c1-239">HIERARCHY_UNIQUE_NAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6a4c1-240"><strong>adSchemaIndexes</strong></span><span class="sxs-lookup"><span data-stu-id="6a4c1-240"><strong>adSchemaIndexes</strong></span></span></p></td>
<td><p><span data-ttu-id="6a4c1-241">3,6</span><span class="sxs-lookup"><span data-stu-id="6a4c1-241">12</span></span></p></td>
<td><p><span data-ttu-id="6a4c1-242">Retorna os índices definidos no catálogo, pertencentes a um usuário específico.</span><span class="sxs-lookup"><span data-stu-id="6a4c1-242">Returns the indexes defined in the catalog that are owned by a given user.</span></span> <span data-ttu-id="6a4c1-243">(Conjunto de linhas INDEXES)</span><span class="sxs-lookup"><span data-stu-id="6a4c1-243">(INDEXES Rowset)</span></span></p></td>
<td><p><span data-ttu-id="6a4c1-244">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="6a4c1-244">TABLE_CATALOG</span></span><br />
<span data-ttu-id="6a4c1-245">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="6a4c1-245">TABLE_SCHEMA</span></span><br />
<span data-ttu-id="6a4c1-246">INDEX_NAME</span><span class="sxs-lookup"><span data-stu-id="6a4c1-246">INDEX_NAME</span></span><br />
<span data-ttu-id="6a4c1-247">Escreva</span><span class="sxs-lookup"><span data-stu-id="6a4c1-247">TYPE</span></span><br />
<span data-ttu-id="6a4c1-248">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="6a4c1-248">TABLE_NAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6a4c1-249"><strong>adSchemaKeyColumnUsage</strong></span><span class="sxs-lookup"><span data-stu-id="6a4c1-249"><strong>adSchemaKeyColumnUsage</strong></span></span></p></td>
<td><p><span data-ttu-id="6a4c1-250">8</span><span class="sxs-lookup"><span data-stu-id="6a4c1-250">8</span></span></p></td>
<td><p><span data-ttu-id="6a4c1-251">Retorna as colunas definidas no catálogo, restritas a chaves por um usuário específico.</span><span class="sxs-lookup"><span data-stu-id="6a4c1-251">Returns the columns defined in the catalog that are constrained as keys by a given user.</span></span> <span data-ttu-id="6a4c1-252">(Conjunto de linhas KEY_COLUMN_USAGE)</span><span class="sxs-lookup"><span data-stu-id="6a4c1-252">(KEY_COLUMN_USAGE Rowset)</span></span></p></td>
<td><p><span data-ttu-id="6a4c1-253">CONSTRAINT_CATALOG</span><span class="sxs-lookup"><span data-stu-id="6a4c1-253">CONSTRAINT_CATALOG</span></span><br />
<span data-ttu-id="6a4c1-254">CONSTRAINT_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="6a4c1-254">CONSTRAINT_SCHEMA</span></span><br />
<span data-ttu-id="6a4c1-255">CONSTRAINT_NAME</span><span class="sxs-lookup"><span data-stu-id="6a4c1-255">CONSTRAINT_NAME</span></span><br />
<span data-ttu-id="6a4c1-256">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="6a4c1-256">TABLE_CATALOG</span></span><br />
<span data-ttu-id="6a4c1-257">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="6a4c1-257">TABLE_SCHEMA</span></span><br />
<span data-ttu-id="6a4c1-258">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="6a4c1-258">TABLE_NAME</span></span><br />
<span data-ttu-id="6a4c1-259">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="6a4c1-259">COLUMN_NAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6a4c1-260"><strong>adSchemaLevels</strong></span><span class="sxs-lookup"><span data-stu-id="6a4c1-260"><strong>adSchemaLevels</strong></span></span></p></td>
<td><p><span data-ttu-id="6a4c1-261">35</span><span class="sxs-lookup"><span data-stu-id="6a4c1-261">35</span></span></p></td>
<td><p><span data-ttu-id="6a4c1-262">Retorna informações sobre os níveis disponíveis em uma dimensão.</span><span class="sxs-lookup"><span data-stu-id="6a4c1-262">Returns information about the levels available in a dimension.</span></span> <span data-ttu-id="6a4c1-263">(Conjunto de linhas LEVELS\*)</span><span class="sxs-lookup"><span data-stu-id="6a4c1-263">(LEVELS Rowset\*)</span></span></p></td>
<td><p><span data-ttu-id="6a4c1-264">CATALOG_NAME</span><span class="sxs-lookup"><span data-stu-id="6a4c1-264">CATALOG_NAME</span></span><br />
<span data-ttu-id="6a4c1-265">SCHEMA_NAME</span><span class="sxs-lookup"><span data-stu-id="6a4c1-265">SCHEMA_NAME</span></span><br />
<span data-ttu-id="6a4c1-266">CUBE_NAME</span><span class="sxs-lookup"><span data-stu-id="6a4c1-266">CUBE_NAME</span></span><br />
<span data-ttu-id="6a4c1-267">DIMENSION_UNIQUE_NAME</span><span class="sxs-lookup"><span data-stu-id="6a4c1-267">DIMENSION_UNIQUE_NAME</span></span><br />
<span data-ttu-id="6a4c1-268">HIERARCHY_UNIQUE_NAME</span><span class="sxs-lookup"><span data-stu-id="6a4c1-268">HIERARCHY_UNIQUE_NAME</span></span><br />
<span data-ttu-id="6a4c1-269">LEVEL_NAME</span><span class="sxs-lookup"><span data-stu-id="6a4c1-269">LEVEL_NAME</span></span><br />
<span data-ttu-id="6a4c1-270">LEVEL_UNIQUE_NAME</span><span class="sxs-lookup"><span data-stu-id="6a4c1-270">LEVEL_UNIQUE_NAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6a4c1-271"><strong>adSchemaMeasures</strong></span><span class="sxs-lookup"><span data-stu-id="6a4c1-271"><strong>adSchemaMeasures</strong></span></span></p></td>
<td><p><span data-ttu-id="6a4c1-272">36</span><span class="sxs-lookup"><span data-stu-id="6a4c1-272">36</span></span></p></td>
<td><p><span data-ttu-id="6a4c1-273">Retorna informações sobre as medidas disponíveis.</span><span class="sxs-lookup"><span data-stu-id="6a4c1-273">Returns information about the available measures.</span></span> <span data-ttu-id="6a4c1-274">(Conjunto de linhas MEASURES\*)</span><span class="sxs-lookup"><span data-stu-id="6a4c1-274">(MEASURES Rowset \*)</span></span></p></td>
<td><p><span data-ttu-id="6a4c1-275">CATALOG_NAME</span><span class="sxs-lookup"><span data-stu-id="6a4c1-275">CATALOG_NAME</span></span><br />
<span data-ttu-id="6a4c1-276">SCHEMA_NAME</span><span class="sxs-lookup"><span data-stu-id="6a4c1-276">SCHEMA_NAME</span></span><br />
<span data-ttu-id="6a4c1-277">CUBE_NAME</span><span class="sxs-lookup"><span data-stu-id="6a4c1-277">CUBE_NAME</span></span><br />
<span data-ttu-id="6a4c1-278">MEASURE_NAME</span><span class="sxs-lookup"><span data-stu-id="6a4c1-278">MEASURE_NAME</span></span><br />
<span data-ttu-id="6a4c1-279">MEASURE_UNIQUE_NAME</span><span class="sxs-lookup"><span data-stu-id="6a4c1-279">MEASURE_UNIQUE_NAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6a4c1-280"><strong>adSchemaMembers</strong></span><span class="sxs-lookup"><span data-stu-id="6a4c1-280"><strong>adSchemaMembers</strong></span></span></p></td>
<td><p><span data-ttu-id="6a4c1-281">38</span><span class="sxs-lookup"><span data-stu-id="6a4c1-281">38</span></span></p></td>
<td><p><span data-ttu-id="6a4c1-282">Retorna informações sobre os membros disponíveis.</span><span class="sxs-lookup"><span data-stu-id="6a4c1-282">Returns information about the available members.</span></span> <span data-ttu-id="6a4c1-283">(Conjunto de linhas MEMBERS\*)</span><span class="sxs-lookup"><span data-stu-id="6a4c1-283">(MEMBERS Rowset \*)</span></span></p></td>
<td><p><span data-ttu-id="6a4c1-284">CATALOG_NAME</span><span class="sxs-lookup"><span data-stu-id="6a4c1-284">CATALOG_NAME</span></span><br />
<span data-ttu-id="6a4c1-285">SCHEMA_NAME</span><span class="sxs-lookup"><span data-stu-id="6a4c1-285">SCHEMA_NAME</span></span><br />
<span data-ttu-id="6a4c1-286">CUBE_NAME</span><span class="sxs-lookup"><span data-stu-id="6a4c1-286">CUBE_NAME</span></span><br />
<span data-ttu-id="6a4c1-287">DIMENSION_UNIQUE_NAME</span><span class="sxs-lookup"><span data-stu-id="6a4c1-287">DIMENSION_UNIQUE_NAME</span></span><br />
<span data-ttu-id="6a4c1-288">HIERARCHY_UNIQUE_NAME</span><span class="sxs-lookup"><span data-stu-id="6a4c1-288">HIERARCHY_UNIQUE_NAME</span></span><br />
<span data-ttu-id="6a4c1-289">LEVEL_UNIQUE_NAME</span><span class="sxs-lookup"><span data-stu-id="6a4c1-289">LEVEL_UNIQUE_NAME</span></span><br />
<span data-ttu-id="6a4c1-290">LEVEL_NUMBER</span><span class="sxs-lookup"><span data-stu-id="6a4c1-290">LEVEL_NUMBER</span></span><br />
<span data-ttu-id="6a4c1-291">MEMBER_NAME</span><span class="sxs-lookup"><span data-stu-id="6a4c1-291">MEMBER_NAME</span></span><br />
<span data-ttu-id="6a4c1-292">MEMBER_UNIQUE_NAME</span><span class="sxs-lookup"><span data-stu-id="6a4c1-292">MEMBER_UNIQUE_NAME</span></span><br />
<span data-ttu-id="6a4c1-293">MEMBER_CAPTION</span><span class="sxs-lookup"><span data-stu-id="6a4c1-293">MEMBER_CAPTION</span></span><br />
<span data-ttu-id="6a4c1-294">MEMBER_TYPE</span><span class="sxs-lookup"><span data-stu-id="6a4c1-294">MEMBER_TYPE</span></span><br />
<span data-ttu-id="6a4c1-295">Operador Tree (para obter mais informações, consulte a documentação do OLE DB para OLAP).</span><span class="sxs-lookup"><span data-stu-id="6a4c1-295">Tree operator (For more information, see the OLE DB for OLAP documentation.)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6a4c1-296"><strong>adSchemaPrimaryKeys</strong></span><span class="sxs-lookup"><span data-stu-id="6a4c1-296"><strong>adSchemaPrimaryKeys</strong></span></span></p></td>
<td><p><span data-ttu-id="6a4c1-297">28</span><span class="sxs-lookup"><span data-stu-id="6a4c1-297">28</span></span></p></td>
<td><p><span data-ttu-id="6a4c1-298">Retorna as colunas de chave principal definidas no catálogo por um determinado usuário.</span><span class="sxs-lookup"><span data-stu-id="6a4c1-298">Returns the primary key columns defined in the catalog by a given user.</span></span> <span data-ttu-id="6a4c1-299">(Conjunto de linhas PRIMARY_KEYS)</span><span class="sxs-lookup"><span data-stu-id="6a4c1-299">(PRIMARY_KEYS Rowset)</span></span></p></td>
<td><p><span data-ttu-id="6a4c1-300">PK_TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="6a4c1-300">PK_TABLE_CATALOG</span></span><br />
<span data-ttu-id="6a4c1-301">PK_TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="6a4c1-301">PK_TABLE_SCHEMA</span></span><br />
<span data-ttu-id="6a4c1-302">PK_TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="6a4c1-302">PK_TABLE_NAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6a4c1-303"><strong>adSchemaProcedureColumns</strong></span><span class="sxs-lookup"><span data-stu-id="6a4c1-303"><strong>adSchemaProcedureColumns</strong></span></span></p></td>
<td><p><span data-ttu-id="6a4c1-304">anos</span><span class="sxs-lookup"><span data-stu-id="6a4c1-304">29</span></span></p></td>
<td><p><span data-ttu-id="6a4c1-305">Retorna informações sobre as colunas de conjuntos de linhas por procedimentos.</span><span class="sxs-lookup"><span data-stu-id="6a4c1-305">Returns information about the columns of rowsets returned by procedures.</span></span> <span data-ttu-id="6a4c1-306">(Conjunto de linhas PROCEDURE_COLUMNS)</span><span class="sxs-lookup"><span data-stu-id="6a4c1-306">(PROCEDURE_COLUMNS Rowset)</span></span></p></td>
<td><p><span data-ttu-id="6a4c1-307">PROCEDURE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="6a4c1-307">PROCEDURE_CATALOG</span></span><br />
<span data-ttu-id="6a4c1-308">PROCEDURE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="6a4c1-308">PROCEDURE_SCHEMA</span></span><br />
<span data-ttu-id="6a4c1-309">PROCEDURE_NAME</span><span class="sxs-lookup"><span data-stu-id="6a4c1-309">PROCEDURE_NAME</span></span><br />
<span data-ttu-id="6a4c1-310">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="6a4c1-310">COLUMN_NAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6a4c1-311"><strong>adSchemaProcedureParameters</strong></span><span class="sxs-lookup"><span data-stu-id="6a4c1-311"><strong>adSchemaProcedureParameters</strong></span></span></p></td>
<td><p><span data-ttu-id="6a4c1-312">660</span><span class="sxs-lookup"><span data-stu-id="6a4c1-312">26</span></span></p></td>
<td><p><span data-ttu-id="6a4c1-313">Retorna informações sobre parâmetros e códigos de retorno de procedimentos.</span><span class="sxs-lookup"><span data-stu-id="6a4c1-313">Returns information about the parameters and return codes of procedures.</span></span> <span data-ttu-id="6a4c1-314">(Conjunto de linhas PROCEDURE_PARAMETERS)</span><span class="sxs-lookup"><span data-stu-id="6a4c1-314">(PROCEDURE_PARAMETERS Rowset)</span></span></p></td>
<td><p><span data-ttu-id="6a4c1-315">PROCEDURE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="6a4c1-315">PROCEDURE_CATALOG</span></span><br />
<span data-ttu-id="6a4c1-316">PROCEDURE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="6a4c1-316">PROCEDURE_SCHEMA</span></span><br />
<span data-ttu-id="6a4c1-317">PROCEDURE_NAME</span><span class="sxs-lookup"><span data-stu-id="6a4c1-317">PROCEDURE_NAME</span></span><br />
<span data-ttu-id="6a4c1-318">PARAMETER_NAME</span><span class="sxs-lookup"><span data-stu-id="6a4c1-318">PARAMETER_NAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6a4c1-319"><strong>adSchemaProcedures</strong></span><span class="sxs-lookup"><span data-stu-id="6a4c1-319"><strong>adSchemaProcedures</strong></span></span></p></td>
<td><p><span data-ttu-id="6a4c1-320">dezesseis</span><span class="sxs-lookup"><span data-stu-id="6a4c1-320">16</span></span></p></td>
<td><p><span data-ttu-id="6a4c1-321">Retorna os procedimentos definidos no catálogo, pertencentes a um usuário específico.</span><span class="sxs-lookup"><span data-stu-id="6a4c1-321">Returns the procedures defined in the catalog that are owned by a given user.</span></span> <span data-ttu-id="6a4c1-322">(Conjunto de linhas PROCEDURES)</span><span class="sxs-lookup"><span data-stu-id="6a4c1-322">(PROCEDURES Rowset)</span></span></p></td>
<td><p><span data-ttu-id="6a4c1-323">PROCEDURE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="6a4c1-323">PROCEDURE_CATALOG</span></span><br />
<span data-ttu-id="6a4c1-324">PROCEDURE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="6a4c1-324">PROCEDURE_SCHEMA</span></span><br />
<span data-ttu-id="6a4c1-325">PROCEDURE_NAME</span><span class="sxs-lookup"><span data-stu-id="6a4c1-325">PROCEDURE_NAME</span></span><br />
<span data-ttu-id="6a4c1-326">PROCEDURE_TYPE</span><span class="sxs-lookup"><span data-stu-id="6a4c1-326">PROCEDURE_TYPE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6a4c1-327"><strong>adSchemaProperties</strong></span><span class="sxs-lookup"><span data-stu-id="6a4c1-327"><strong>adSchemaProperties</strong></span></span></p></td>
<td><p><span data-ttu-id="6a4c1-328">37</span><span class="sxs-lookup"><span data-stu-id="6a4c1-328">37</span></span></p></td>
<td><p><span data-ttu-id="6a4c1-329">Retorna informações sobre as propriedades disponíveis para cada nível de dimensão.</span><span class="sxs-lookup"><span data-stu-id="6a4c1-329">Returns information about the available properties for each level of the dimension.</span></span> <span data-ttu-id="6a4c1-330">(Conjunto de linhas PROPERTIES\*)</span><span class="sxs-lookup"><span data-stu-id="6a4c1-330">(PROPERTIES Rowset \*)</span></span></p></td>
<td><p><span data-ttu-id="6a4c1-331">CATALOG_NAME</span><span class="sxs-lookup"><span data-stu-id="6a4c1-331">CATALOG_NAME</span></span><br />
<span data-ttu-id="6a4c1-332">SCHEMA_NAME</span><span class="sxs-lookup"><span data-stu-id="6a4c1-332">SCHEMA_NAME</span></span><br />
<span data-ttu-id="6a4c1-333">CUBE_NAME</span><span class="sxs-lookup"><span data-stu-id="6a4c1-333">CUBE_NAME</span></span><br />
<span data-ttu-id="6a4c1-334">DIMENSION_UNIQUE_NAME</span><span class="sxs-lookup"><span data-stu-id="6a4c1-334">DIMENSION_UNIQUE_NAME</span></span><br />
<span data-ttu-id="6a4c1-335">HIERARCHY_UNIQUE_NAME</span><span class="sxs-lookup"><span data-stu-id="6a4c1-335">HIERARCHY_UNIQUE_NAME</span></span><br />
<span data-ttu-id="6a4c1-336">LEVEL_UNIQUE_NAME</span><span class="sxs-lookup"><span data-stu-id="6a4c1-336">LEVEL_UNIQUE_NAME</span></span><br />
<span data-ttu-id="6a4c1-337">MEMBER_UNIQUE_NAME</span><span class="sxs-lookup"><span data-stu-id="6a4c1-337">MEMBER_UNIQUE_NAME</span></span><br />
<span data-ttu-id="6a4c1-338">PROPERTY_TYPE</span><span class="sxs-lookup"><span data-stu-id="6a4c1-338">PROPERTY_TYPE</span></span><br />
<span data-ttu-id="6a4c1-339">PROPERTY_NAME</span><span class="sxs-lookup"><span data-stu-id="6a4c1-339">PROPERTY_NAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6a4c1-340"><strong>adSchemaProviderSpecific</strong></span><span class="sxs-lookup"><span data-stu-id="6a4c1-340"><strong>adSchemaProviderSpecific</strong></span></span></p></td>
<td><p><span data-ttu-id="6a4c1-341">-1</span><span class="sxs-lookup"><span data-stu-id="6a4c1-341">-1</span></span></p></td>
<td><p><span data-ttu-id="6a4c1-342">Utilizada se o provedor define suas próprias consultas de esquema não padrão.</span><span class="sxs-lookup"><span data-stu-id="6a4c1-342">Used if the provider defines its own nonstandard schema queries.</span></span></p></td>
<td><p><span data-ttu-id="6a4c1-343">&lt;Específico do provedor&gt;</span><span class="sxs-lookup"><span data-stu-id="6a4c1-343">&lt;Provider specific&gt;</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6a4c1-344"><strong>adSchemaProviderTypes</strong></span><span class="sxs-lookup"><span data-stu-id="6a4c1-344"><strong>adSchemaProviderTypes</strong></span></span></p></td>
<td><p><span data-ttu-id="6a4c1-345">22</span><span class="sxs-lookup"><span data-stu-id="6a4c1-345">22</span></span></p></td>
<td><p><span data-ttu-id="6a4c1-346">Retorna os tipos de dados (base) aceitos pelo provedor de dados.</span><span class="sxs-lookup"><span data-stu-id="6a4c1-346">Returns the (base) data types supported by the data provider.</span></span> <span data-ttu-id="6a4c1-347">(Conjunto de linhas PROVIDER_TYPES)</span><span class="sxs-lookup"><span data-stu-id="6a4c1-347">(PROVIDER_TYPES Rowset)</span></span></p></td>
<td><p><span data-ttu-id="6a4c1-348">DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="6a4c1-348">DATA_TYPE</span></span><br />
<span data-ttu-id="6a4c1-349">BEST_MATCH</span><span class="sxs-lookup"><span data-stu-id="6a4c1-349">BEST_MATCH</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6a4c1-350"><strong>AdSchemaReferentialConstraints</strong></span><span class="sxs-lookup"><span data-stu-id="6a4c1-350"><strong>AdSchemaReferentialConstraints</strong></span></span></p></td>
<td><p><span data-ttu-id="6a4c1-351">241</span><span class="sxs-lookup"><span data-stu-id="6a4c1-351">9</span></span></p></td>
<td><p><span data-ttu-id="6a4c1-352">Retorna as restrições de referência definidas no catálogo, pertencentes a um usuário específico.</span><span class="sxs-lookup"><span data-stu-id="6a4c1-352">Returns the referential constraints defined in the catalog that are owned by a given user.</span></span> <span data-ttu-id="6a4c1-353">(Conjunto de linhas REFERENTIAL_CONSTRAINTS)</span><span class="sxs-lookup"><span data-stu-id="6a4c1-353">(REFERENTIAL_CONSTRAINTS Rowset)</span></span></p></td>
<td><p><span data-ttu-id="6a4c1-354">CONSTRAINT_CATALOG</span><span class="sxs-lookup"><span data-stu-id="6a4c1-354">CONSTRAINT_CATALOG</span></span><br />
<span data-ttu-id="6a4c1-355">CONSTRAINT_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="6a4c1-355">CONSTRAINT_SCHEMA</span></span><br />
<span data-ttu-id="6a4c1-356">CONSTRAINT_NAME</span><span class="sxs-lookup"><span data-stu-id="6a4c1-356">CONSTRAINT_NAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6a4c1-357"><strong>adSchemaSchemata</strong></span><span class="sxs-lookup"><span data-stu-id="6a4c1-357"><strong>adSchemaSchemata</strong></span></span></p></td>
<td><p><span data-ttu-id="6a4c1-358">17.07.06</span><span class="sxs-lookup"><span data-stu-id="6a4c1-358">17</span></span></p></td>
<td><p><span data-ttu-id="6a4c1-359">Retorna os esquemas (objetos de banco de dados) pertencentes a um usuário específico.</span><span class="sxs-lookup"><span data-stu-id="6a4c1-359">Returns the schemas (database objects) that are owned by a given user.</span></span> <span data-ttu-id="6a4c1-360">(Conjunto de linhas SCHEMATA)</span><span class="sxs-lookup"><span data-stu-id="6a4c1-360">(SCHEMATA Rowset)</span></span></p></td>
<td><p><span data-ttu-id="6a4c1-361">CATALOG_NAME</span><span class="sxs-lookup"><span data-stu-id="6a4c1-361">CATALOG_NAME</span></span><br />
<span data-ttu-id="6a4c1-362">SCHEMA_NAME</span><span class="sxs-lookup"><span data-stu-id="6a4c1-362">SCHEMA_NAME</span></span><br />
<span data-ttu-id="6a4c1-363">SCHEMA_OWNER</span><span class="sxs-lookup"><span data-stu-id="6a4c1-363">SCHEMA_OWNER</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6a4c1-364"><strong>adSchemaSQLLanguages</strong></span><span class="sxs-lookup"><span data-stu-id="6a4c1-364"><strong>adSchemaSQLLanguages</strong></span></span></p></td>
<td><p><span data-ttu-id="6a4c1-365">anos</span><span class="sxs-lookup"><span data-stu-id="6a4c1-365">18</span></span></p></td>
<td><p><span data-ttu-id="6a4c1-366">Retorna os níveis, as opções e os dialetos de conformidade aceitos pelos dados de processamento de implementação do SQL definidos no catálogo.</span><span class="sxs-lookup"><span data-stu-id="6a4c1-366">Returns the conformance levels, options, and dialects supported by the SQL-implementation processing data defined in the catalog.</span></span> <span data-ttu-id="6a4c1-367">(Conjunto de linhas SQL_LANGUAGES)</span><span class="sxs-lookup"><span data-stu-id="6a4c1-367">(SQL_LANGUAGES Rowset)</span></span></p></td>
<td><p><span data-ttu-id="6a4c1-368">&lt;Nenhum&gt;</span><span class="sxs-lookup"><span data-stu-id="6a4c1-368">&lt;None&gt;</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6a4c1-369"><strong>adSchemaStatistics</strong></span><span class="sxs-lookup"><span data-stu-id="6a4c1-369"><strong>adSchemaStatistics</strong></span></span></p></td>
<td><p><span data-ttu-id="6a4c1-370">19</span><span class="sxs-lookup"><span data-stu-id="6a4c1-370">19</span></span></p></td>
<td><p><span data-ttu-id="6a4c1-371">Retorna as estatísticas definidas no catálogo, pertencentes a um usuário específico.</span><span class="sxs-lookup"><span data-stu-id="6a4c1-371">Returns the statistics defined in the catalog that are owned by a given user.</span></span> <span data-ttu-id="6a4c1-372">(Conjunto de linhas STATISTICS)</span><span class="sxs-lookup"><span data-stu-id="6a4c1-372">(STATISTICS Rowset)</span></span></p></td>
<td><p><span data-ttu-id="6a4c1-373">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="6a4c1-373">TABLE_CATALOG</span></span><br />
<span data-ttu-id="6a4c1-374">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="6a4c1-374">TABLE_SCHEMA</span></span><br />
<span data-ttu-id="6a4c1-375">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="6a4c1-375">TABLE_NAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6a4c1-376"><strong>adSchemaTableConstraints</strong></span><span class="sxs-lookup"><span data-stu-id="6a4c1-376"><strong>adSchemaTableConstraints</strong></span></span></p></td>
<td><p><span data-ttu-id="6a4c1-377">254</span><span class="sxs-lookup"><span data-stu-id="6a4c1-377">10</span></span></p></td>
<td><p><span data-ttu-id="6a4c1-378">Retorna as restrições de tabela definidas no catálogo, pertencentes a um usuário específico.</span><span class="sxs-lookup"><span data-stu-id="6a4c1-378">Returns the table constraints defined in the catalog that are owned by a given user.</span></span> <span data-ttu-id="6a4c1-379">(Conjunto de linha TABLE_CONSTRAINTS)</span><span class="sxs-lookup"><span data-stu-id="6a4c1-379">(TABLE_CONSTRAINTS Rowset)</span></span></p></td>
<td><p><span data-ttu-id="6a4c1-380">CONSTRAINT_CATALOG</span><span class="sxs-lookup"><span data-stu-id="6a4c1-380">CONSTRAINT_CATALOG</span></span><br />
<span data-ttu-id="6a4c1-381">CONSTRAINT_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="6a4c1-381">CONSTRAINT_SCHEMA</span></span><br />
<span data-ttu-id="6a4c1-382">CONSTRAINT_NAME</span><span class="sxs-lookup"><span data-stu-id="6a4c1-382">CONSTRAINT_NAME</span></span><br />
<span data-ttu-id="6a4c1-383">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="6a4c1-383">TABLE_CATALOG</span></span><br />
<span data-ttu-id="6a4c1-384">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="6a4c1-384">TABLE_SCHEMA</span></span><br />
<span data-ttu-id="6a4c1-385">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="6a4c1-385">TABLE_NAME</span></span><br />
<span data-ttu-id="6a4c1-386">CONSTRAINT_TYPE</span><span class="sxs-lookup"><span data-stu-id="6a4c1-386">CONSTRAINT_TYPE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6a4c1-387"><strong>adSchemaTablePrivileges</strong></span><span class="sxs-lookup"><span data-stu-id="6a4c1-387"><strong>adSchemaTablePrivileges</strong></span></span></p></td>
<td><p><span data-ttu-id="6a4c1-388">14</span><span class="sxs-lookup"><span data-stu-id="6a4c1-388">14</span></span></p></td>
<td><p><span data-ttu-id="6a4c1-389">Retorna, nas tabelas definidas no catálogo, os privilégios que estão disponíveis para um determinado usuário ou foram concedidos a ele.</span><span class="sxs-lookup"><span data-stu-id="6a4c1-389">Returns the privileges on tables defined in the catalog that are available to, or granted by, a given user.</span></span> <span data-ttu-id="6a4c1-390">(Conjunto de linhas TABLE_PRIVILEGES)</span><span class="sxs-lookup"><span data-stu-id="6a4c1-390">(TABLE_PRIVILEGES Rowset)</span></span></p></td>
<td><p><span data-ttu-id="6a4c1-391">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="6a4c1-391">TABLE_CATALOG</span></span><br />
<span data-ttu-id="6a4c1-392">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="6a4c1-392">TABLE_SCHEMA</span></span><br />
<span data-ttu-id="6a4c1-393">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="6a4c1-393">TABLE_NAME</span></span><br />
<span data-ttu-id="6a4c1-394">CESSO</span><span class="sxs-lookup"><span data-stu-id="6a4c1-394">GRANTOR</span></span><br />
<span data-ttu-id="6a4c1-395">GRANTEE</span><span class="sxs-lookup"><span data-stu-id="6a4c1-395">GRANTEE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6a4c1-396"><strong>adSchemaTables</strong></span><span class="sxs-lookup"><span data-stu-id="6a4c1-396"><strong>adSchemaTables</strong></span></span></p></td>
<td><p><span data-ttu-id="6a4c1-397">508</span><span class="sxs-lookup"><span data-stu-id="6a4c1-397">20</span></span></p></td>
<td><p><span data-ttu-id="6a4c1-398">Retorna as tabelas (inclusive as exibições) definidas no catálogo que estão acessíveis para um determinado usuário.</span><span class="sxs-lookup"><span data-stu-id="6a4c1-398">Returns the tables (including views) defined in the catalog that are accessible to a given user.</span></span> <span data-ttu-id="6a4c1-399">(Conjunto de linhas TABLES)</span><span class="sxs-lookup"><span data-stu-id="6a4c1-399">(TABLES Rowset)</span></span></p></td>
<td><p><span data-ttu-id="6a4c1-400">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="6a4c1-400">TABLE_CATALOG</span></span><br />
<span data-ttu-id="6a4c1-401">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="6a4c1-401">TABLE_SCHEMA</span></span><br />
<span data-ttu-id="6a4c1-402">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="6a4c1-402">TABLE_NAME</span></span><br />
<span data-ttu-id="6a4c1-403">TABLE_TYPE</span><span class="sxs-lookup"><span data-stu-id="6a4c1-403">TABLE_TYPE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6a4c1-404"><strong>adSchemaTranslations</strong></span><span class="sxs-lookup"><span data-stu-id="6a4c1-404"><strong>adSchemaTranslations</strong></span></span></p></td>
<td><p><span data-ttu-id="6a4c1-405">21</span><span class="sxs-lookup"><span data-stu-id="6a4c1-405">21</span></span></p></td>
<td><p><span data-ttu-id="6a4c1-406">Retorna as conversões de caracteres definidas no catálogo que estão acessíveis para um usuário específico.</span><span class="sxs-lookup"><span data-stu-id="6a4c1-406">Returns the character translations defined in the catalog that are accessible to a given user.</span></span> <span data-ttu-id="6a4c1-407">(Conjunto de linhas TRANSLATIONS)</span><span class="sxs-lookup"><span data-stu-id="6a4c1-407">(TRANSLATIONS Rowset)</span></span></p></td>
<td><p><span data-ttu-id="6a4c1-408">TRANSLATION_CATALOG</span><span class="sxs-lookup"><span data-stu-id="6a4c1-408">TRANSLATION_CATALOG</span></span><br />
<span data-ttu-id="6a4c1-409">TRANSLATION_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="6a4c1-409">TRANSLATION_SCHEMA</span></span><br />
<span data-ttu-id="6a4c1-410">TRANSLATION_NAME</span><span class="sxs-lookup"><span data-stu-id="6a4c1-410">TRANSLATION_NAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6a4c1-411"><strong>adSchemaTrustees</strong></span><span class="sxs-lookup"><span data-stu-id="6a4c1-411"><strong>adSchemaTrustees</strong></span></span></p></td>
<td><p><span data-ttu-id="6a4c1-412">39</span><span class="sxs-lookup"><span data-stu-id="6a4c1-412">39</span></span></p></td>
<td><p><span data-ttu-id="6a4c1-413">Reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="6a4c1-413">Reserved for future use.</span></span></p></td>
<td><p><br />
</p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6a4c1-414"><strong>adSchemaUsagePrivileges</strong></span><span class="sxs-lookup"><span data-stu-id="6a4c1-414"><strong>adSchemaUsagePrivileges</strong></span></span></p></td>
<td><p><span data-ttu-id="6a4c1-415">15</span><span class="sxs-lookup"><span data-stu-id="6a4c1-415">15</span></span></p></td>
<td><p><span data-ttu-id="6a4c1-416">Retorna, nos objetos definidos no catálogo, os privilégios USAGE que estão disponíveis para um determinado usuário ou foram concedidos a ele.</span><span class="sxs-lookup"><span data-stu-id="6a4c1-416">Returns the USAGE privileges on objects defined in the catalog that are available to, or granted by, a given user.</span></span> <span data-ttu-id="6a4c1-417">(Conjunto de linhas USAGE_PRIVILEGES)</span><span class="sxs-lookup"><span data-stu-id="6a4c1-417">(USAGE_PRIVILEGES Rowset)</span></span></p></td>
<td><p><span data-ttu-id="6a4c1-418">OBJECT_CATALOG</span><span class="sxs-lookup"><span data-stu-id="6a4c1-418">OBJECT_CATALOG</span></span><br />
<span data-ttu-id="6a4c1-419">OBJECT_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="6a4c1-419">OBJECT_SCHEMA</span></span><br />
<span data-ttu-id="6a4c1-420">OBJECT_NAME</span><span class="sxs-lookup"><span data-stu-id="6a4c1-420">OBJECT_NAME</span></span><br />
<span data-ttu-id="6a4c1-421">OBJECT_TYPE</span><span class="sxs-lookup"><span data-stu-id="6a4c1-421">OBJECT_TYPE</span></span><br />
<span data-ttu-id="6a4c1-422">CESSO</span><span class="sxs-lookup"><span data-stu-id="6a4c1-422">GRANTOR</span></span><br />
<span data-ttu-id="6a4c1-423">GRANTEE</span><span class="sxs-lookup"><span data-stu-id="6a4c1-423">GRANTEE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6a4c1-424"><strong>adSchemaViewColumnUsage</strong></span><span class="sxs-lookup"><span data-stu-id="6a4c1-424"><strong>adSchemaViewColumnUsage</strong></span></span></p></td>
<td><p><span data-ttu-id="6a4c1-425">dia</span><span class="sxs-lookup"><span data-stu-id="6a4c1-425">24</span></span></p></td>
<td><p><span data-ttu-id="6a4c1-426">Retorna as colunas das quais as tabelas exibidas, definidas no catálogo e pertencentes a um usuário específico, são dependentes.</span><span class="sxs-lookup"><span data-stu-id="6a4c1-426">Returns the columns on which viewed tables, defined in the catalog and owned by a given user, are dependent.</span></span> <span data-ttu-id="6a4c1-427">(Conjunto de linhas VIEW_COLUMN_USAGE)</span><span class="sxs-lookup"><span data-stu-id="6a4c1-427">(VIEW_COLUMN_USAGE Rowset)</span></span></p></td>
<td><p><span data-ttu-id="6a4c1-428">VIEW_CATALOG</span><span class="sxs-lookup"><span data-stu-id="6a4c1-428">VIEW_CATALOG</span></span><br />
<span data-ttu-id="6a4c1-429">VIEW_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="6a4c1-429">VIEW_SCHEMA</span></span><br />
<span data-ttu-id="6a4c1-430">VIEW_NAME</span><span class="sxs-lookup"><span data-stu-id="6a4c1-430">VIEW_NAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6a4c1-431"><strong>adSchemaViews</strong></span><span class="sxs-lookup"><span data-stu-id="6a4c1-431"><strong>adSchemaViews</strong></span></span></p></td>
<td><p><span data-ttu-id="6a4c1-432">23</span><span class="sxs-lookup"><span data-stu-id="6a4c1-432">23</span></span></p></td>
<td><p><span data-ttu-id="6a4c1-433">Retorna as exibições definidas no catálogo que estão acessíveis para um determinado usuário.</span><span class="sxs-lookup"><span data-stu-id="6a4c1-433">Returns the views defined in the catalog that are accessible to a given user.</span></span> <span data-ttu-id="6a4c1-434">(Conjunto de linhas VIEWS)</span><span class="sxs-lookup"><span data-stu-id="6a4c1-434">(VIEWS Rowset)</span></span></p></td>
<td><p><span data-ttu-id="6a4c1-435">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="6a4c1-435">TABLE_CATALOG</span></span><br />
<span data-ttu-id="6a4c1-436">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="6a4c1-436">TABLE_SCHEMA</span></span><br />
<span data-ttu-id="6a4c1-437">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="6a4c1-437">TABLE_NAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6a4c1-438"><strong>adSchemaViewTableUsage</strong></span><span class="sxs-lookup"><span data-stu-id="6a4c1-438"><strong>adSchemaViewTableUsage</strong></span></span></p></td>
<td><p><span data-ttu-id="6a4c1-439">25</span><span class="sxs-lookup"><span data-stu-id="6a4c1-439">25</span></span></p></td>
<td><p><span data-ttu-id="6a4c1-440">Retorna as tabelas das quais as tabelas exibidas, definidas no catálogo e pertencentes a um usuário específico, são dependentes.</span><span class="sxs-lookup"><span data-stu-id="6a4c1-440">Returns the tables on which viewed tables, defined in the catalog and owned by a given user, are dependent.</span></span> <span data-ttu-id="6a4c1-441">(Conjunto de linhas VIEW_TABLE_USAGE)</span><span class="sxs-lookup"><span data-stu-id="6a4c1-441">(VIEW_TABLE_USAGE Rowset)</span></span></p></td>
<td><p><span data-ttu-id="6a4c1-442">VIEW_CATALOG</span><span class="sxs-lookup"><span data-stu-id="6a4c1-442">VIEW_CATALOG</span></span><br />
<span data-ttu-id="6a4c1-443">VIEW_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="6a4c1-443">VIEW_SCHEMA</span></span><br />
<span data-ttu-id="6a4c1-444">VIEW_NAME</span><span class="sxs-lookup"><span data-stu-id="6a4c1-444">VIEW_NAME</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="6a4c1-445">Equivalente do ADO/WFC</span><span class="sxs-lookup"><span data-stu-id="6a4c1-445">ADO/WFC equivalent</span></span>

<span data-ttu-id="6a4c1-446">Pacote: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="6a4c1-446">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="6a4c1-447">Constant</span><span class="sxs-lookup"><span data-stu-id="6a4c1-447">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6a4c1-448">AdoEnums. Schema. ASSERTs</span><span class="sxs-lookup"><span data-stu-id="6a4c1-448">AdoEnums.Schema.ASSERTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6a4c1-449">AdoEnums. Schema. CATALOGs</span><span class="sxs-lookup"><span data-stu-id="6a4c1-449">AdoEnums.Schema.CATALOGS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6a4c1-450">AdoEnums. Schema. CHARACTERSETS</span><span class="sxs-lookup"><span data-stu-id="6a4c1-450">AdoEnums.Schema.CHARACTERSETS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6a4c1-451">AdoEnums. Schema. CHECKCONSTRAINTS</span><span class="sxs-lookup"><span data-stu-id="6a4c1-451">AdoEnums.Schema.CHECKCONSTRAINTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6a4c1-452">AdoEnums. Schema. COLLATIONs</span><span class="sxs-lookup"><span data-stu-id="6a4c1-452">AdoEnums.Schema.COLLATIONS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6a4c1-453">AdoEnums. Schema. COLUMNPRIVILEGES</span><span class="sxs-lookup"><span data-stu-id="6a4c1-453">AdoEnums.Schema.COLUMNPRIVILEGES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6a4c1-454">AdoEnums. Schema. COLUMNS</span><span class="sxs-lookup"><span data-stu-id="6a4c1-454">AdoEnums.Schema.COLUMNS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6a4c1-455">AdoEnums. Schema. COLUMNSDOMAINUSAGE</span><span class="sxs-lookup"><span data-stu-id="6a4c1-455">AdoEnums.Schema.COLUMNSDOMAINUSAGE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6a4c1-456">AdoEnums. Schema. CONSTRAINTCOLUMNUSAGE</span><span class="sxs-lookup"><span data-stu-id="6a4c1-456">AdoEnums.Schema.CONSTRAINTCOLUMNUSAGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6a4c1-457">AdoEnums. Schema. CONSTRAINTTABLEUSAGE</span><span class="sxs-lookup"><span data-stu-id="6a4c1-457">AdoEnums.Schema.CONSTRAINTTABLEUSAGE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6a4c1-458">AdoEnums. Schema. CUBEs</span><span class="sxs-lookup"><span data-stu-id="6a4c1-458">AdoEnums.Schema.CUBES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6a4c1-459">AdoEnums. Schema. DBINFOKEYWORDS</span><span class="sxs-lookup"><span data-stu-id="6a4c1-459">AdoEnums.Schema.DBINFOKEYWORDS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6a4c1-460">AdoEnums. Schema. DBINFOLITERALS</span><span class="sxs-lookup"><span data-stu-id="6a4c1-460">AdoEnums.Schema.DBINFOLITERALS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6a4c1-461">AdoEnums. Schema. DIMENSIONs</span><span class="sxs-lookup"><span data-stu-id="6a4c1-461">AdoEnums.Schema.DIMENSIONS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6a4c1-462">AdoEnums. Schema. FOREIGNKEYS</span><span class="sxs-lookup"><span data-stu-id="6a4c1-462">AdoEnums.Schema.FOREIGNKEYS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6a4c1-463">AdoEnums. Schema. HIERARQUIAs</span><span class="sxs-lookup"><span data-stu-id="6a4c1-463">AdoEnums.Schema.HIERARCHIES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6a4c1-464">AdoEnums. Schema. Indexes</span><span class="sxs-lookup"><span data-stu-id="6a4c1-464">AdoEnums.Schema.INDEXES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6a4c1-465">AdoEnums. Schema. KEYCOLUMNUSAGE</span><span class="sxs-lookup"><span data-stu-id="6a4c1-465">AdoEnums.Schema.KEYCOLUMNUSAGE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6a4c1-466">AdoEnums. Schema. LEVELs</span><span class="sxs-lookup"><span data-stu-id="6a4c1-466">AdoEnums.Schema.LEVELS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6a4c1-467">AdoEnums. Schema. MEASUREs</span><span class="sxs-lookup"><span data-stu-id="6a4c1-467">AdoEnums.Schema.MEASURES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6a4c1-468">AdoEnums. Schema. MEMBERs</span><span class="sxs-lookup"><span data-stu-id="6a4c1-468">AdoEnums.Schema.MEMBERS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6a4c1-469">AdoEnums. Schema. PRIMARYKEY</span><span class="sxs-lookup"><span data-stu-id="6a4c1-469">AdoEnums.Schema.PRIMARYKEYS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6a4c1-470">AdoEnums. Schema. PROCEDURECOLUMNS</span><span class="sxs-lookup"><span data-stu-id="6a4c1-470">AdoEnums.Schema.PROCEDURECOLUMNS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6a4c1-471">AdoEnums. Schema. PROCEDUREparameters</span><span class="sxs-lookup"><span data-stu-id="6a4c1-471">AdoEnums.Schema.PROCEDUREPARAMETERS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6a4c1-472">AdoEnums. Schema. PROCEDUREs</span><span class="sxs-lookup"><span data-stu-id="6a4c1-472">AdoEnums.Schema.PROCEDURES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6a4c1-473">AdoEnums. Schema. PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="6a4c1-473">AdoEnums.Schema.PROPERTIES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6a4c1-474">AdoEnums. Schema. PROVIDERSPECIFIC</span><span class="sxs-lookup"><span data-stu-id="6a4c1-474">AdoEnums.Schema.PROVIDERSPECIFIC</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6a4c1-475">AdoEnums. Schema. PROVIDERTYPES</span><span class="sxs-lookup"><span data-stu-id="6a4c1-475">AdoEnums.Schema.PROVIDERTYPES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6a4c1-476">AdoEnums. Schema. REFERENTIALCONTRAINTS</span><span class="sxs-lookup"><span data-stu-id="6a4c1-476">AdoEnums.Schema.REFERENTIALCONTRAINTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6a4c1-477">AdoEnums. Schema. SCHEMATA</span><span class="sxs-lookup"><span data-stu-id="6a4c1-477">AdoEnums.Schema.SCHEMATA</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6a4c1-478">Idiomas AdoEnums. Schema.</span><span class="sxs-lookup"><span data-stu-id="6a4c1-478">AdoEnums.Schema.SQLLANGUAGES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6a4c1-479">AdoEnums. Schema. STATISTICs</span><span class="sxs-lookup"><span data-stu-id="6a4c1-479">AdoEnums.Schema.STATISTICS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6a4c1-480">AdoEnums. Schema. TABLECONSTRAINTS</span><span class="sxs-lookup"><span data-stu-id="6a4c1-480">AdoEnums.Schema.TABLECONSTRAINTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6a4c1-481">AdoEnums. Schema. TABLEPRIVILEGES</span><span class="sxs-lookup"><span data-stu-id="6a4c1-481">AdoEnums.Schema.TABLEPRIVILEGES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6a4c1-482">AdoEnums. Schema. TABLEs</span><span class="sxs-lookup"><span data-stu-id="6a4c1-482">AdoEnums.Schema.TABLES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6a4c1-483">AdoEnums. Schema. TRANSLATIONs</span><span class="sxs-lookup"><span data-stu-id="6a4c1-483">AdoEnums.Schema.TRANSLATIONS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6a4c1-484">AdoEnums. Schema. TRUSTers</span><span class="sxs-lookup"><span data-stu-id="6a4c1-484">AdoEnums.Schema.TRUSTEES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6a4c1-485">AdoEnums. Schema. USAGEPRIVILEGES</span><span class="sxs-lookup"><span data-stu-id="6a4c1-485">AdoEnums.Schema.USAGEPRIVILEGES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6a4c1-486">AdoEnums. Schema. VIEWCOLUMNUSAGE</span><span class="sxs-lookup"><span data-stu-id="6a4c1-486">AdoEnums.Schema.VIEWCOLUMNUSAGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6a4c1-487">AdoEnums. Schema. views</span><span class="sxs-lookup"><span data-stu-id="6a4c1-487">AdoEnums.Schema.VIEWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6a4c1-488">AdoEnums. Schema. VIEWTABLEUSAGE</span><span class="sxs-lookup"><span data-stu-id="6a4c1-488">AdoEnums.Schema.VIEWTABLEUSAGE</span></span></p></td>
</tr>
</tbody>
</table>

