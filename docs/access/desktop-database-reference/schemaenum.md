---
title: SchemaEnum (referência do banco de dados da área de trabalho do Access)
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
# <a name="schemaenum"></a><span data-ttu-id="d7f3a-102">SchemaEnum</span><span class="sxs-lookup"><span data-stu-id="d7f3a-102">SchemaEnum</span></span>

<span data-ttu-id="d7f3a-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="d7f3a-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="d7f3a-104">Especifica o tipo de esquema do **Recordset** que o método [OpenSchema](openschema-method-ado.md) recupera.</span><span class="sxs-lookup"><span data-stu-id="d7f3a-104">Specifies the type of schema **Recordset** that the [OpenSchema](openschema-method-ado.md) method retrieves.</span></span>

## <a name="remarks"></a><span data-ttu-id="d7f3a-105">Comentários</span><span class="sxs-lookup"><span data-stu-id="d7f3a-105">Remarks</span></span>

<span data-ttu-id="d7f3a-106">Informações adicionais sobre a função e as colunas retornadas para cada constante do ADO podem ser encontradas nos tópicos do Apêndice B do manual *OLE DB Programmers Reference (Referência para programadores do OLE DB)*.</span><span class="sxs-lookup"><span data-stu-id="d7f3a-106">Additional information about the function and columns returned for each ADO constant can be found in topics of Appendix B of the *OLE DB Programmers Reference*.</span></span> <span data-ttu-id="d7f3a-107">O nome de cada tópico está listado entre parênteses na seção Descrição da tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="d7f3a-107">The name of each topic is listed in parentheses in the Description section of the following table.</span></span>

<span data-ttu-id="d7f3a-108">Informações adicionais sobre a função e as colunas retornadas para cada constante do ADO MD podem ser encontradas nos tópicos do Capítulo 23 da documentação *OLE DB for OLAP (OLE DB para OLAP)*.</span><span class="sxs-lookup"><span data-stu-id="d7f3a-108">Additional information about the function and columns returned for each ADO MD constant can be found in topics of Chapter 23 of the *OLE DB for OLAP* documentation.</span></span> <span data-ttu-id="d7f3a-109">O nome de cada tópico é listado entre parênteses e marcado com um asterisco ( ) na coluna Descrição \* da tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="d7f3a-109">The name of each topic is listed in parentheses and marked with an asterisk (\*) in the Description column of the following table.</span></span>

<span data-ttu-id="d7f3a-110">Converta os tipos de dados das colunas na documentação OLE DB para tipos de dados do ADO, consultando a coluna Descrição do tópico ADO [DataTypeEnum](datatypeenum.md).</span><span class="sxs-lookup"><span data-stu-id="d7f3a-110">Translate the data types of columns in the OLE DB documentation to ADO data types by referring to the Description column of the ADO [DataTypeEnum](datatypeenum.md) topic.</span></span> <span data-ttu-id="d7f3a-111">Por exemplo, um tipo de dados OLE DB **de DBTYPE \_ WSTR** é equivalente a um tipo de dados do ADO de **adWChar**.</span><span class="sxs-lookup"><span data-stu-id="d7f3a-111">For example, an OLE DB data type of **DBTYPE\_WSTR** is equivalent to an ADO data type of **adWChar**.</span></span>

<span data-ttu-id="d7f3a-112">O ADO gera resultados como esquema para as constantes **adSchemaDBInfoKeywords** e **adSchemaDBInfoLiterals**.</span><span class="sxs-lookup"><span data-stu-id="d7f3a-112">ADO generates schema-like results for the constants, **adSchemaDBInfoKeywords** and **adSchemaDBInfoLiterals**.</span></span> <span data-ttu-id="d7f3a-113">O ADO cria um **Recordset** e preenche cada linha com os valores retornados respectivamente pelos métodos **IDBInfo::GetKeywords** e **IDBInfo::GetLiteralInfo.**</span><span class="sxs-lookup"><span data-stu-id="d7f3a-113">ADO creates a **Recordset**, and then fills each row with the values returned respectively by the **IDBInfo::GetKeywords** and **IDBInfo::GetLiteralInfo** methods.</span></span> <span data-ttu-id="d7f3a-114">Informações adicionais sobre esses métodos podem ser encontradas na seção IDBInfo da Referência do programador *do OLE DB.*</span><span class="sxs-lookup"><span data-stu-id="d7f3a-114">Additional information about these methods can be found in the IDBInfo section of the *OLE DB Programmer's Reference*.</span></span>

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
<th><p><span data-ttu-id="d7f3a-115">Constant</span><span class="sxs-lookup"><span data-stu-id="d7f3a-115">Constant</span></span></p></th>
<th><p><span data-ttu-id="d7f3a-116">Valor</span><span class="sxs-lookup"><span data-stu-id="d7f3a-116">Value</span></span></p></th>
<th><p><span data-ttu-id="d7f3a-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="d7f3a-117">Description</span></span></p></th>
<th><p><span data-ttu-id="d7f3a-118">Colunas de restrição</span><span class="sxs-lookup"><span data-stu-id="d7f3a-118">Constraint columns</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d7f3a-119"><strong>adSchemaAsserts</strong></span><span class="sxs-lookup"><span data-stu-id="d7f3a-119"><strong>adSchemaAsserts</strong></span></span></p></td>
<td><p><span data-ttu-id="d7f3a-120">0</span><span class="sxs-lookup"><span data-stu-id="d7f3a-120">0</span></span></p></td>
<td><p><span data-ttu-id="d7f3a-121">Retorna as asserções definidas no catálogo, pertencentes a um usuário específico.</span><span class="sxs-lookup"><span data-stu-id="d7f3a-121">Returns the assertions defined in the catalog that are owned by a given user.</span></span> <span data-ttu-id="d7f3a-122">(Conjunto de linhas ASSERTIONS)</span><span class="sxs-lookup"><span data-stu-id="d7f3a-122">(ASSERTIONS Rowset)</span></span></p></td>
<td><p><span data-ttu-id="d7f3a-123">CONSTRAINT_CATALOG</span><span class="sxs-lookup"><span data-stu-id="d7f3a-123">CONSTRAINT_CATALOG</span></span><br />
<span data-ttu-id="d7f3a-124">CONSTRAINT_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="d7f3a-124">CONSTRAINT_SCHEMA</span></span><br />
<span data-ttu-id="d7f3a-125">CONSTRAINT_NAME</span><span class="sxs-lookup"><span data-stu-id="d7f3a-125">CONSTRAINT_NAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d7f3a-126"><strong>adSchemaCatalogs</strong></span><span class="sxs-lookup"><span data-stu-id="d7f3a-126"><strong>adSchemaCatalogs</strong></span></span></p></td>
<td><p><span data-ttu-id="d7f3a-127">1 </span><span class="sxs-lookup"><span data-stu-id="d7f3a-127">1</span></span></p></td>
<td><p><span data-ttu-id="d7f3a-128">Retorna os atributos físicos associados aos catálogos acessíveis do DBMS.</span><span class="sxs-lookup"><span data-stu-id="d7f3a-128">Returns the physical attributes associated with catalogs accessible from the DBMS.</span></span> <span data-ttu-id="d7f3a-129">(Conjunto de linhas CATALOGS)</span><span class="sxs-lookup"><span data-stu-id="d7f3a-129">(CATALOGS Rowset)</span></span></p></td>
<td><p><span data-ttu-id="d7f3a-130">CATALOG_NAME</span><span class="sxs-lookup"><span data-stu-id="d7f3a-130">CATALOG_NAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d7f3a-131"><strong>adSchemaCharacterSets</strong></span><span class="sxs-lookup"><span data-stu-id="d7f3a-131"><strong>adSchemaCharacterSets</strong></span></span></p></td>
<td><p><span data-ttu-id="d7f3a-132">2 </span><span class="sxs-lookup"><span data-stu-id="d7f3a-132">2</span></span></p></td>
<td><p><span data-ttu-id="d7f3a-133">Retorna os conjuntos de caracteres definidos no catálogo que estão acessíveis para um determinado usuário.</span><span class="sxs-lookup"><span data-stu-id="d7f3a-133">Returns the character sets defined in the catalog that are accessible to a given user.</span></span> <span data-ttu-id="d7f3a-134">(Conjunto de linhas CHARACTER_SETS)</span><span class="sxs-lookup"><span data-stu-id="d7f3a-134">(CHARACTER_SETS Rowset)</span></span></p></td>
<td><p><span data-ttu-id="d7f3a-135">CHARACTER_SET_CATALOG</span><span class="sxs-lookup"><span data-stu-id="d7f3a-135">CHARACTER_SET_CATALOG</span></span><br />
<span data-ttu-id="d7f3a-136">CHARACTER_SET_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="d7f3a-136">CHARACTER_SET_SCHEMA</span></span><br />
<span data-ttu-id="d7f3a-137">CHARACTER_SET_NAME</span><span class="sxs-lookup"><span data-stu-id="d7f3a-137">CHARACTER_SET_NAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d7f3a-138"><strong>adSchemaCheckConstraints</strong></span><span class="sxs-lookup"><span data-stu-id="d7f3a-138"><strong>adSchemaCheckConstraints</strong></span></span></p></td>
<td><p><span data-ttu-id="d7f3a-139">5 </span><span class="sxs-lookup"><span data-stu-id="d7f3a-139">5</span></span></p></td>
<td><p><span data-ttu-id="d7f3a-140">Retorna as restrições de verificação definidas no catálogo, pertencentes a um usuário específico.</span><span class="sxs-lookup"><span data-stu-id="d7f3a-140">Returns the check constraints defined in the catalog that are owned by a given user.</span></span> <span data-ttu-id="d7f3a-141">(Conjunto de linhas CHECK_CONSTRAINTS)</span><span class="sxs-lookup"><span data-stu-id="d7f3a-141">(CHECK_CONSTRAINTS Rowset)</span></span></p></td>
<td><p><span data-ttu-id="d7f3a-142">CONSTRAINT_CATALOG</span><span class="sxs-lookup"><span data-stu-id="d7f3a-142">CONSTRAINT_CATALOG</span></span><br />
<span data-ttu-id="d7f3a-143">CONSTRAINT_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="d7f3a-143">CONSTRAINT_SCHEMA</span></span><br />
<span data-ttu-id="d7f3a-144">CONSTRAINT_NAME</span><span class="sxs-lookup"><span data-stu-id="d7f3a-144">CONSTRAINT_NAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d7f3a-145"><strong>adSchemaCollations</strong></span><span class="sxs-lookup"><span data-stu-id="d7f3a-145"><strong>adSchemaCollations</strong></span></span></p></td>
<td><p><span data-ttu-id="d7f3a-146">3 </span><span class="sxs-lookup"><span data-stu-id="d7f3a-146">3</span></span></p></td>
<td><p><span data-ttu-id="d7f3a-147">Retorna as coleções de caracteres definidas no catálogo que estão acessíveis para um determinado usuário.</span><span class="sxs-lookup"><span data-stu-id="d7f3a-147">Returns the character collations defined in the catalog that are accessible to a given user.</span></span> <span data-ttu-id="d7f3a-148">(Conjunto de linhas COLLATIONS)</span><span class="sxs-lookup"><span data-stu-id="d7f3a-148">(COLLATIONS Rowset)</span></span></p></td>
<td><p><span data-ttu-id="d7f3a-149">COLLATION_CATALOG</span><span class="sxs-lookup"><span data-stu-id="d7f3a-149">COLLATION_CATALOG</span></span><br />
<span data-ttu-id="d7f3a-150">COLLATION_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="d7f3a-150">COLLATION_SCHEMA</span></span><br />
<span data-ttu-id="d7f3a-151">COLLATION_NAME</span><span class="sxs-lookup"><span data-stu-id="d7f3a-151">COLLATION_NAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d7f3a-152"><strong>adSchemaColumnPrivileges</strong></span><span class="sxs-lookup"><span data-stu-id="d7f3a-152"><strong>adSchemaColumnPrivileges</strong></span></span></p></td>
<td><p><span data-ttu-id="d7f3a-153">13 </span><span class="sxs-lookup"><span data-stu-id="d7f3a-153">13</span></span></p></td>
<td><p><span data-ttu-id="d7f3a-154">Retorna, nas colunas das tabelas definidas no catálogo, os privilégios que estão disponíveis para um determinado usuário ou foram concedidos a ele.</span><span class="sxs-lookup"><span data-stu-id="d7f3a-154">Returns the privileges on columns of tables defined in the catalog that are available to, or granted by, a given user.</span></span> <span data-ttu-id="d7f3a-155">(Conjunto de linhas COLUMN_PRIVILEGES)</span><span class="sxs-lookup"><span data-stu-id="d7f3a-155">(COLUMN_PRIVILEGES Rowset)</span></span></p></td>
<td><p><span data-ttu-id="d7f3a-156">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="d7f3a-156">TABLE_CATALOG</span></span><br />
<span data-ttu-id="d7f3a-157">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="d7f3a-157">TABLE_SCHEMA</span></span><br />
<span data-ttu-id="d7f3a-158">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="d7f3a-158">TABLE_NAME</span></span><br />
<span data-ttu-id="d7f3a-159">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="d7f3a-159">COLUMN_NAME</span></span><br />
<span data-ttu-id="d7f3a-160">GRANTOR</span><span class="sxs-lookup"><span data-stu-id="d7f3a-160">GRANTOR</span></span><br />
<span data-ttu-id="d7f3a-161">GRANTEE</span><span class="sxs-lookup"><span data-stu-id="d7f3a-161">GRANTEE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d7f3a-162"><strong>adSchemaColumns</strong></span><span class="sxs-lookup"><span data-stu-id="d7f3a-162"><strong>adSchemaColumns</strong></span></span></p></td>
<td><p><span data-ttu-id="d7f3a-163">4 </span><span class="sxs-lookup"><span data-stu-id="d7f3a-163">4</span></span></p></td>
<td><p><span data-ttu-id="d7f3a-164">Retorna as colunas das tabelas (inclusive as exibições) definidas no catálogo que estão acessíveis para um determinado usuário.</span><span class="sxs-lookup"><span data-stu-id="d7f3a-164">Returns the columns of tables (including views) defined in the catalog that are accessible to a given user.</span></span> <span data-ttu-id="d7f3a-165">(Conjunto de linhas COLUMNS)</span><span class="sxs-lookup"><span data-stu-id="d7f3a-165">(COLUMNS Rowset)</span></span></p></td>
<td><p><span data-ttu-id="d7f3a-166">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="d7f3a-166">TABLE_CATALOG</span></span><br />
<span data-ttu-id="d7f3a-167">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="d7f3a-167">TABLE_SCHEMA</span></span><br />
<span data-ttu-id="d7f3a-168">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="d7f3a-168">TABLE_NAME</span></span><br />
<span data-ttu-id="d7f3a-169">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="d7f3a-169">COLUMN_NAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d7f3a-170"><strong>adSchemaColumnsDomainUsage</strong></span><span class="sxs-lookup"><span data-stu-id="d7f3a-170"><strong>adSchemaColumnsDomainUsage</strong></span></span></p></td>
<td><p><span data-ttu-id="d7f3a-171">11</span><span class="sxs-lookup"><span data-stu-id="d7f3a-171">11</span></span></p></td>
<td><p><span data-ttu-id="d7f3a-172">Retorna as colunas definidas no catálogo que são dependentes de um domínio definido no catálogo e pertencem a um determinado usuário.</span><span class="sxs-lookup"><span data-stu-id="d7f3a-172">Returns the columns defined in the catalog that are dependent on a domain defined in the catalog and owned by a given user.</span></span> <span data-ttu-id="d7f3a-173">(Conjunto de linhas COLUMN_DOMAIN_USAGE)</span><span class="sxs-lookup"><span data-stu-id="d7f3a-173">(COLUMN_DOMAIN_USAGE Rowset)</span></span></p></td>
<td><p><span data-ttu-id="d7f3a-174">DOMAIN_CATALOG</span><span class="sxs-lookup"><span data-stu-id="d7f3a-174">DOMAIN_CATALOG</span></span><br />
<span data-ttu-id="d7f3a-175">DOMAIN_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="d7f3a-175">DOMAIN_SCHEMA</span></span><br />
<span data-ttu-id="d7f3a-176">DOMAIN_NAME</span><span class="sxs-lookup"><span data-stu-id="d7f3a-176">DOMAIN_NAME</span></span><br />
<span data-ttu-id="d7f3a-177">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="d7f3a-177">COLUMN_NAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d7f3a-178"><strong>adSchemaConstraintColumnUsage</strong></span><span class="sxs-lookup"><span data-stu-id="d7f3a-178"><strong>adSchemaConstraintColumnUsage</strong></span></span></p></td>
<td><p><span data-ttu-id="d7f3a-179">6 </span><span class="sxs-lookup"><span data-stu-id="d7f3a-179">6</span></span></p></td>
<td><p><span data-ttu-id="d7f3a-180">Retorna as colunas usadas por restrições de referência, restrições exclusivas, restrições de verificação e asserções, definidas no catálogo e pertencentes a um usuário específico.</span><span class="sxs-lookup"><span data-stu-id="d7f3a-180">Returns the columns used by referential constraints, unique constraints, check constraints, and assertions, defined in the catalog and owned by a given user.</span></span> <span data-ttu-id="d7f3a-181">(Conjunto de linhas CONSTRAINT_COLUMN_USAGE)</span><span class="sxs-lookup"><span data-stu-id="d7f3a-181">(CONSTRAINT_COLUMN_USAGE Rowset)</span></span></p></td>
<td><p><span data-ttu-id="d7f3a-182">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="d7f3a-182">TABLE_CATALOG</span></span><br />
<span data-ttu-id="d7f3a-183">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="d7f3a-183">TABLE_SCHEMA</span></span><br />
<span data-ttu-id="d7f3a-184">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="d7f3a-184">TABLE_NAME</span></span><br />
<span data-ttu-id="d7f3a-185">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="d7f3a-185">COLUMN_NAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d7f3a-186"><strong>adSchemaConstraintTableUsage</strong></span><span class="sxs-lookup"><span data-stu-id="d7f3a-186"><strong>adSchemaConstraintTableUsage</strong></span></span></p></td>
<td><p><span data-ttu-id="d7f3a-187">7 </span><span class="sxs-lookup"><span data-stu-id="d7f3a-187">7</span></span></p></td>
<td><p><span data-ttu-id="d7f3a-188">Retorna as tabelas usadas por restrições de referência, restrições exclusivas, restrições de verificação e asserções, definidas no catálogo e pertencentes a um usuário específico.</span><span class="sxs-lookup"><span data-stu-id="d7f3a-188">Returns the tables that are used by referential constraints, unique constraints, check constraints, and assertions defined in the catalog and owned by a given user.</span></span> <span data-ttu-id="d7f3a-189">(Conjunto de linhas CONSTRAINT_TABLE_USAGE)</span><span class="sxs-lookup"><span data-stu-id="d7f3a-189">(CONSTRAINT_TABLE_USAGE Rowset)</span></span></p></td>
<td><p><span data-ttu-id="d7f3a-190">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="d7f3a-190">TABLE_CATALOG</span></span><br />
<span data-ttu-id="d7f3a-191">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="d7f3a-191">TABLE_SCHEMA</span></span><br />
<span data-ttu-id="d7f3a-192">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="d7f3a-192">TABLE_NAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d7f3a-193"><strong>adSchemaCubes</strong></span><span class="sxs-lookup"><span data-stu-id="d7f3a-193"><strong>adSchemaCubes</strong></span></span></p></td>
<td><p><span data-ttu-id="d7f3a-194">32</span><span class="sxs-lookup"><span data-stu-id="d7f3a-194">32</span></span></p></td>
<td><p><span data-ttu-id="d7f3a-195">Retorna informações sobre os cubos disponíveis em um esquema (ou o catálogo se o provedor não oferecer suporte a esquemas).</span><span class="sxs-lookup"><span data-stu-id="d7f3a-195">Returns information about the available cubes in a schema (or the catalog, if the provider does not support schemas).</span></span> <span data-ttu-id="d7f3a-196">(Conjunto de linhas CUBES\*)</span><span class="sxs-lookup"><span data-stu-id="d7f3a-196">(CUBES Rowset\*)</span></span></p></td>
<td><p><span data-ttu-id="d7f3a-197">CATALOG_NAME</span><span class="sxs-lookup"><span data-stu-id="d7f3a-197">CATALOG_NAME</span></span><br />
<span data-ttu-id="d7f3a-198">SCHEMA_NAME</span><span class="sxs-lookup"><span data-stu-id="d7f3a-198">SCHEMA_NAME</span></span><br />
<span data-ttu-id="d7f3a-199">CUBE_NAME</span><span class="sxs-lookup"><span data-stu-id="d7f3a-199">CUBE_NAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d7f3a-200"><strong>adSchemaDBInfoKeywords</strong></span><span class="sxs-lookup"><span data-stu-id="d7f3a-200"><strong>adSchemaDBInfoKeywords</strong></span></span></p></td>
<td><p><span data-ttu-id="d7f3a-201">30</span><span class="sxs-lookup"><span data-stu-id="d7f3a-201">30</span></span></p></td>
<td><p><span data-ttu-id="d7f3a-202">Retorna uma lista de palavras-chave específicas do provedor.</span><span class="sxs-lookup"><span data-stu-id="d7f3a-202">Returns a list of provider-specific keywords.</span></span> <span data-ttu-id="d7f3a-203">(IDBInfo::GetKeywords \*)</span><span class="sxs-lookup"><span data-stu-id="d7f3a-203">(IDBInfo::GetKeywords \*)</span></span></p></td>
<td><p><span data-ttu-id="d7f3a-204">&lt;Nenhum&gt;</span><span class="sxs-lookup"><span data-stu-id="d7f3a-204">&lt;None&gt;</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d7f3a-205"><strong>adSchemaDBInfoLiterals</strong></span><span class="sxs-lookup"><span data-stu-id="d7f3a-205"><strong>adSchemaDBInfoLiterals</strong></span></span></p></td>
<td><p><span data-ttu-id="d7f3a-206">31</span><span class="sxs-lookup"><span data-stu-id="d7f3a-206">31</span></span></p></td>
<td><p><span data-ttu-id="d7f3a-207">Retorna uma lista de literais específicos do provedor utilizados em comandos de texto.</span><span class="sxs-lookup"><span data-stu-id="d7f3a-207">Returns a list of provider-specific literals used in text commands.</span></span> <span data-ttu-id="d7f3a-208">(IDBInfo::GetLiteralInfo \*)</span><span class="sxs-lookup"><span data-stu-id="d7f3a-208">(IDBInfo::GetLiteralInfo \*)</span></span></p></td>
<td><p><span data-ttu-id="d7f3a-209">&lt;Nenhum&gt;</span><span class="sxs-lookup"><span data-stu-id="d7f3a-209">&lt;None&gt;</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d7f3a-210"><strong>adSchemaDimensions</strong></span><span class="sxs-lookup"><span data-stu-id="d7f3a-210"><strong>adSchemaDimensions</strong></span></span></p></td>
<td><p><span data-ttu-id="d7f3a-211">33</span><span class="sxs-lookup"><span data-stu-id="d7f3a-211">33</span></span></p></td>
<td><p><span data-ttu-id="d7f3a-212">Retorna informações sobre as dimensões em um determinado cubo.</span><span class="sxs-lookup"><span data-stu-id="d7f3a-212">Returns information about the dimensions in a given cube.</span></span> <span data-ttu-id="d7f3a-213">Ele tem uma linha para cada dimensão.</span><span class="sxs-lookup"><span data-stu-id="d7f3a-213">It has one row for each dimension.</span></span> <span data-ttu-id="d7f3a-214">(Conjunto de linhas DIMENSIONS\*)</span><span class="sxs-lookup"><span data-stu-id="d7f3a-214">(DIMENSIONS Rowset \*)</span></span></p></td>
<td><p><span data-ttu-id="d7f3a-215">CATALOG_NAME</span><span class="sxs-lookup"><span data-stu-id="d7f3a-215">CATALOG_NAME</span></span><br />
<span data-ttu-id="d7f3a-216">SCHEMA_NAME</span><span class="sxs-lookup"><span data-stu-id="d7f3a-216">SCHEMA_NAME</span></span><br />
<span data-ttu-id="d7f3a-217">CUBE_NAME</span><span class="sxs-lookup"><span data-stu-id="d7f3a-217">CUBE_NAME</span></span><br />
<span data-ttu-id="d7f3a-218">DIMENSION_NAME</span><span class="sxs-lookup"><span data-stu-id="d7f3a-218">DIMENSION_NAME</span></span><br />
<span data-ttu-id="d7f3a-219">DIMENSION_UNIQUE_NAME</span><span class="sxs-lookup"><span data-stu-id="d7f3a-219">DIMENSION_UNIQUE_NAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d7f3a-220"><strong>adSchemaForeignKeys</strong></span><span class="sxs-lookup"><span data-stu-id="d7f3a-220"><strong>adSchemaForeignKeys</strong></span></span></p></td>
<td><p><span data-ttu-id="d7f3a-221">27</span><span class="sxs-lookup"><span data-stu-id="d7f3a-221">27</span></span></p></td>
<td><p><span data-ttu-id="d7f3a-222">Retorna as colunas de chave estrangeira definidas no catálogo por um determinado usuário.</span><span class="sxs-lookup"><span data-stu-id="d7f3a-222">Returns the foreign key columns defined in the catalog by a given user.</span></span> <span data-ttu-id="d7f3a-223">(Conjunto de linhas FOREIGN_KEYS)</span><span class="sxs-lookup"><span data-stu-id="d7f3a-223">(FOREIGN_KEYS Rowset)</span></span></p></td>
<td><p><span data-ttu-id="d7f3a-224">PK_TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="d7f3a-224">PK_TABLE_CATALOG</span></span><br />
<span data-ttu-id="d7f3a-225">PK_TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="d7f3a-225">PK_TABLE_SCHEMA</span></span><br />
<span data-ttu-id="d7f3a-226">PK_TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="d7f3a-226">PK_TABLE_NAME</span></span><br />
<span data-ttu-id="d7f3a-227">FK_TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="d7f3a-227">FK_TABLE_CATALOG</span></span><br />
<span data-ttu-id="d7f3a-228">FK_TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="d7f3a-228">FK_TABLE_SCHEMA</span></span><br />
<span data-ttu-id="d7f3a-229">FK_TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="d7f3a-229">FK_TABLE_NAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d7f3a-230"><strong>adSchemaHierarchies</strong></span><span class="sxs-lookup"><span data-stu-id="d7f3a-230"><strong>adSchemaHierarchies</strong></span></span></p></td>
<td><p><span data-ttu-id="d7f3a-231">34</span><span class="sxs-lookup"><span data-stu-id="d7f3a-231">34</span></span></p></td>
<td><p><span data-ttu-id="d7f3a-232">Retorna informações sobre as hierarquias disponíveis em uma dimensão.</span><span class="sxs-lookup"><span data-stu-id="d7f3a-232">Returns information about the hierarchies available in a dimension.</span></span> <span data-ttu-id="d7f3a-233">(Conjunto de linhas HIERARCHIES\*)</span><span class="sxs-lookup"><span data-stu-id="d7f3a-233">(HIERARCHIES Rowset \*)</span></span></p></td>
<td><p><span data-ttu-id="d7f3a-234">CATALOG_NAME</span><span class="sxs-lookup"><span data-stu-id="d7f3a-234">CATALOG_NAME</span></span><br />
<span data-ttu-id="d7f3a-235">SCHEMA_NAME</span><span class="sxs-lookup"><span data-stu-id="d7f3a-235">SCHEMA_NAME</span></span><br />
<span data-ttu-id="d7f3a-236">CUBE_NAME</span><span class="sxs-lookup"><span data-stu-id="d7f3a-236">CUBE_NAME</span></span><br />
<span data-ttu-id="d7f3a-237">DIMENSION_UNIQUE_NAME</span><span class="sxs-lookup"><span data-stu-id="d7f3a-237">DIMENSION_UNIQUE_NAME</span></span><br />
<span data-ttu-id="d7f3a-238">HIERARCHY_NAME</span><span class="sxs-lookup"><span data-stu-id="d7f3a-238">HIERARCHY_NAME</span></span><br />
<span data-ttu-id="d7f3a-239">HIERARCHY_UNIQUE_NAME</span><span class="sxs-lookup"><span data-stu-id="d7f3a-239">HIERARCHY_UNIQUE_NAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d7f3a-240"><strong>adSchemaIndexes</strong></span><span class="sxs-lookup"><span data-stu-id="d7f3a-240"><strong>adSchemaIndexes</strong></span></span></p></td>
<td><p><span data-ttu-id="d7f3a-241">12 </span><span class="sxs-lookup"><span data-stu-id="d7f3a-241">12</span></span></p></td>
<td><p><span data-ttu-id="d7f3a-242">Retorna os índices definidos no catálogo, pertencentes a um usuário específico.</span><span class="sxs-lookup"><span data-stu-id="d7f3a-242">Returns the indexes defined in the catalog that are owned by a given user.</span></span> <span data-ttu-id="d7f3a-243">(Conjunto de linhas INDEXES)</span><span class="sxs-lookup"><span data-stu-id="d7f3a-243">(INDEXES Rowset)</span></span></p></td>
<td><p><span data-ttu-id="d7f3a-244">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="d7f3a-244">TABLE_CATALOG</span></span><br />
<span data-ttu-id="d7f3a-245">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="d7f3a-245">TABLE_SCHEMA</span></span><br />
<span data-ttu-id="d7f3a-246">INDEX_NAME</span><span class="sxs-lookup"><span data-stu-id="d7f3a-246">INDEX_NAME</span></span><br />
<span data-ttu-id="d7f3a-247">TYPE</span><span class="sxs-lookup"><span data-stu-id="d7f3a-247">TYPE</span></span><br />
<span data-ttu-id="d7f3a-248">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="d7f3a-248">TABLE_NAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d7f3a-249"><strong>adSchemaKeyColumnUsage</strong></span><span class="sxs-lookup"><span data-stu-id="d7f3a-249"><strong>adSchemaKeyColumnUsage</strong></span></span></p></td>
<td><p><span data-ttu-id="d7f3a-250">8 </span><span class="sxs-lookup"><span data-stu-id="d7f3a-250">8</span></span></p></td>
<td><p><span data-ttu-id="d7f3a-251">Retorna as colunas definidas no catálogo, restritas a chaves por um usuário específico.</span><span class="sxs-lookup"><span data-stu-id="d7f3a-251">Returns the columns defined in the catalog that are constrained as keys by a given user.</span></span> <span data-ttu-id="d7f3a-252">(Conjunto de linhas KEY_COLUMN_USAGE)</span><span class="sxs-lookup"><span data-stu-id="d7f3a-252">(KEY_COLUMN_USAGE Rowset)</span></span></p></td>
<td><p><span data-ttu-id="d7f3a-253">CONSTRAINT_CATALOG</span><span class="sxs-lookup"><span data-stu-id="d7f3a-253">CONSTRAINT_CATALOG</span></span><br />
<span data-ttu-id="d7f3a-254">CONSTRAINT_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="d7f3a-254">CONSTRAINT_SCHEMA</span></span><br />
<span data-ttu-id="d7f3a-255">CONSTRAINT_NAME</span><span class="sxs-lookup"><span data-stu-id="d7f3a-255">CONSTRAINT_NAME</span></span><br />
<span data-ttu-id="d7f3a-256">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="d7f3a-256">TABLE_CATALOG</span></span><br />
<span data-ttu-id="d7f3a-257">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="d7f3a-257">TABLE_SCHEMA</span></span><br />
<span data-ttu-id="d7f3a-258">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="d7f3a-258">TABLE_NAME</span></span><br />
<span data-ttu-id="d7f3a-259">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="d7f3a-259">COLUMN_NAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d7f3a-260"><strong>adSchemaLevels</strong></span><span class="sxs-lookup"><span data-stu-id="d7f3a-260"><strong>adSchemaLevels</strong></span></span></p></td>
<td><p><span data-ttu-id="d7f3a-261">35</span><span class="sxs-lookup"><span data-stu-id="d7f3a-261">35</span></span></p></td>
<td><p><span data-ttu-id="d7f3a-262">Retorna informações sobre os níveis disponíveis em uma dimensão.</span><span class="sxs-lookup"><span data-stu-id="d7f3a-262">Returns information about the levels available in a dimension.</span></span> <span data-ttu-id="d7f3a-263">(Conjunto de linhas LEVELS\*)</span><span class="sxs-lookup"><span data-stu-id="d7f3a-263">(LEVELS Rowset\*)</span></span></p></td>
<td><p><span data-ttu-id="d7f3a-264">CATALOG_NAME</span><span class="sxs-lookup"><span data-stu-id="d7f3a-264">CATALOG_NAME</span></span><br />
<span data-ttu-id="d7f3a-265">SCHEMA_NAME</span><span class="sxs-lookup"><span data-stu-id="d7f3a-265">SCHEMA_NAME</span></span><br />
<span data-ttu-id="d7f3a-266">CUBE_NAME</span><span class="sxs-lookup"><span data-stu-id="d7f3a-266">CUBE_NAME</span></span><br />
<span data-ttu-id="d7f3a-267">DIMENSION_UNIQUE_NAME</span><span class="sxs-lookup"><span data-stu-id="d7f3a-267">DIMENSION_UNIQUE_NAME</span></span><br />
<span data-ttu-id="d7f3a-268">HIERARCHY_UNIQUE_NAME</span><span class="sxs-lookup"><span data-stu-id="d7f3a-268">HIERARCHY_UNIQUE_NAME</span></span><br />
<span data-ttu-id="d7f3a-269">LEVEL_NAME</span><span class="sxs-lookup"><span data-stu-id="d7f3a-269">LEVEL_NAME</span></span><br />
<span data-ttu-id="d7f3a-270">LEVEL_UNIQUE_NAME</span><span class="sxs-lookup"><span data-stu-id="d7f3a-270">LEVEL_UNIQUE_NAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d7f3a-271"><strong>adSchemaMeasures</strong></span><span class="sxs-lookup"><span data-stu-id="d7f3a-271"><strong>adSchemaMeasures</strong></span></span></p></td>
<td><p><span data-ttu-id="d7f3a-272">36</span><span class="sxs-lookup"><span data-stu-id="d7f3a-272">36</span></span></p></td>
<td><p><span data-ttu-id="d7f3a-273">Retorna informações sobre as medidas disponíveis.</span><span class="sxs-lookup"><span data-stu-id="d7f3a-273">Returns information about the available measures.</span></span> <span data-ttu-id="d7f3a-274">(Conjunto de linhas MEASURES\*)</span><span class="sxs-lookup"><span data-stu-id="d7f3a-274">(MEASURES Rowset \*)</span></span></p></td>
<td><p><span data-ttu-id="d7f3a-275">CATALOG_NAME</span><span class="sxs-lookup"><span data-stu-id="d7f3a-275">CATALOG_NAME</span></span><br />
<span data-ttu-id="d7f3a-276">SCHEMA_NAME</span><span class="sxs-lookup"><span data-stu-id="d7f3a-276">SCHEMA_NAME</span></span><br />
<span data-ttu-id="d7f3a-277">CUBE_NAME</span><span class="sxs-lookup"><span data-stu-id="d7f3a-277">CUBE_NAME</span></span><br />
<span data-ttu-id="d7f3a-278">MEASURE_NAME</span><span class="sxs-lookup"><span data-stu-id="d7f3a-278">MEASURE_NAME</span></span><br />
<span data-ttu-id="d7f3a-279">MEASURE_UNIQUE_NAME</span><span class="sxs-lookup"><span data-stu-id="d7f3a-279">MEASURE_UNIQUE_NAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d7f3a-280"><strong>adSchemaMembers</strong></span><span class="sxs-lookup"><span data-stu-id="d7f3a-280"><strong>adSchemaMembers</strong></span></span></p></td>
<td><p><span data-ttu-id="d7f3a-281">38</span><span class="sxs-lookup"><span data-stu-id="d7f3a-281">38</span></span></p></td>
<td><p><span data-ttu-id="d7f3a-282">Retorna informações sobre os membros disponíveis.</span><span class="sxs-lookup"><span data-stu-id="d7f3a-282">Returns information about the available members.</span></span> <span data-ttu-id="d7f3a-283">(Conjunto de linhas MEMBERS\*)</span><span class="sxs-lookup"><span data-stu-id="d7f3a-283">(MEMBERS Rowset \*)</span></span></p></td>
<td><p><span data-ttu-id="d7f3a-284">CATALOG_NAME</span><span class="sxs-lookup"><span data-stu-id="d7f3a-284">CATALOG_NAME</span></span><br />
<span data-ttu-id="d7f3a-285">SCHEMA_NAME</span><span class="sxs-lookup"><span data-stu-id="d7f3a-285">SCHEMA_NAME</span></span><br />
<span data-ttu-id="d7f3a-286">CUBE_NAME</span><span class="sxs-lookup"><span data-stu-id="d7f3a-286">CUBE_NAME</span></span><br />
<span data-ttu-id="d7f3a-287">DIMENSION_UNIQUE_NAME</span><span class="sxs-lookup"><span data-stu-id="d7f3a-287">DIMENSION_UNIQUE_NAME</span></span><br />
<span data-ttu-id="d7f3a-288">HIERARCHY_UNIQUE_NAME</span><span class="sxs-lookup"><span data-stu-id="d7f3a-288">HIERARCHY_UNIQUE_NAME</span></span><br />
<span data-ttu-id="d7f3a-289">LEVEL_UNIQUE_NAME</span><span class="sxs-lookup"><span data-stu-id="d7f3a-289">LEVEL_UNIQUE_NAME</span></span><br />
<span data-ttu-id="d7f3a-290">LEVEL_NUMBER</span><span class="sxs-lookup"><span data-stu-id="d7f3a-290">LEVEL_NUMBER</span></span><br />
<span data-ttu-id="d7f3a-291">MEMBER_NAME</span><span class="sxs-lookup"><span data-stu-id="d7f3a-291">MEMBER_NAME</span></span><br />
<span data-ttu-id="d7f3a-292">MEMBER_UNIQUE_NAME</span><span class="sxs-lookup"><span data-stu-id="d7f3a-292">MEMBER_UNIQUE_NAME</span></span><br />
<span data-ttu-id="d7f3a-293">MEMBER_CAPTION</span><span class="sxs-lookup"><span data-stu-id="d7f3a-293">MEMBER_CAPTION</span></span><br />
<span data-ttu-id="d7f3a-294">MEMBER_TYPE</span><span class="sxs-lookup"><span data-stu-id="d7f3a-294">MEMBER_TYPE</span></span><br />
<span data-ttu-id="d7f3a-295">Operador de árvore (Para obter mais informações, consulte a documentação do OLE DB para OLAP.)</span><span class="sxs-lookup"><span data-stu-id="d7f3a-295">Tree operator (For more information, see the OLE DB for OLAP documentation.)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d7f3a-296"><strong>adSchemaPrimaryKeys</strong></span><span class="sxs-lookup"><span data-stu-id="d7f3a-296"><strong>adSchemaPrimaryKeys</strong></span></span></p></td>
<td><p><span data-ttu-id="d7f3a-297">28</span><span class="sxs-lookup"><span data-stu-id="d7f3a-297">28</span></span></p></td>
<td><p><span data-ttu-id="d7f3a-298">Retorna as colunas de chave principal definidas no catálogo por um determinado usuário.</span><span class="sxs-lookup"><span data-stu-id="d7f3a-298">Returns the primary key columns defined in the catalog by a given user.</span></span> <span data-ttu-id="d7f3a-299">(Conjunto de linhas PRIMARY_KEYS)</span><span class="sxs-lookup"><span data-stu-id="d7f3a-299">(PRIMARY_KEYS Rowset)</span></span></p></td>
<td><p><span data-ttu-id="d7f3a-300">PK_TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="d7f3a-300">PK_TABLE_CATALOG</span></span><br />
<span data-ttu-id="d7f3a-301">PK_TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="d7f3a-301">PK_TABLE_SCHEMA</span></span><br />
<span data-ttu-id="d7f3a-302">PK_TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="d7f3a-302">PK_TABLE_NAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d7f3a-303"><strong>adSchemaProcedureColumns</strong></span><span class="sxs-lookup"><span data-stu-id="d7f3a-303"><strong>adSchemaProcedureColumns</strong></span></span></p></td>
<td><p><span data-ttu-id="d7f3a-304">29</span><span class="sxs-lookup"><span data-stu-id="d7f3a-304">29</span></span></p></td>
<td><p><span data-ttu-id="d7f3a-305">Retorna informações sobre as colunas de conjuntos de linhas por procedimentos.</span><span class="sxs-lookup"><span data-stu-id="d7f3a-305">Returns information about the columns of rowsets returned by procedures.</span></span> <span data-ttu-id="d7f3a-306">(Conjunto de linhas PROCEDURE_COLUMNS)</span><span class="sxs-lookup"><span data-stu-id="d7f3a-306">(PROCEDURE_COLUMNS Rowset)</span></span></p></td>
<td><p><span data-ttu-id="d7f3a-307">PROCEDURE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="d7f3a-307">PROCEDURE_CATALOG</span></span><br />
<span data-ttu-id="d7f3a-308">PROCEDURE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="d7f3a-308">PROCEDURE_SCHEMA</span></span><br />
<span data-ttu-id="d7f3a-309">PROCEDURE_NAME</span><span class="sxs-lookup"><span data-stu-id="d7f3a-309">PROCEDURE_NAME</span></span><br />
<span data-ttu-id="d7f3a-310">COLUMN_NAME</span><span class="sxs-lookup"><span data-stu-id="d7f3a-310">COLUMN_NAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d7f3a-311"><strong>adSchemaProcedureParameters</strong></span><span class="sxs-lookup"><span data-stu-id="d7f3a-311"><strong>adSchemaProcedureParameters</strong></span></span></p></td>
<td><p><span data-ttu-id="d7f3a-312">26</span><span class="sxs-lookup"><span data-stu-id="d7f3a-312">26</span></span></p></td>
<td><p><span data-ttu-id="d7f3a-313">Retorna informações sobre parâmetros e códigos de retorno de procedimentos.</span><span class="sxs-lookup"><span data-stu-id="d7f3a-313">Returns information about the parameters and return codes of procedures.</span></span> <span data-ttu-id="d7f3a-314">(Conjunto de linhas PROCEDURE_PARAMETERS)</span><span class="sxs-lookup"><span data-stu-id="d7f3a-314">(PROCEDURE_PARAMETERS Rowset)</span></span></p></td>
<td><p><span data-ttu-id="d7f3a-315">PROCEDURE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="d7f3a-315">PROCEDURE_CATALOG</span></span><br />
<span data-ttu-id="d7f3a-316">PROCEDURE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="d7f3a-316">PROCEDURE_SCHEMA</span></span><br />
<span data-ttu-id="d7f3a-317">PROCEDURE_NAME</span><span class="sxs-lookup"><span data-stu-id="d7f3a-317">PROCEDURE_NAME</span></span><br />
<span data-ttu-id="d7f3a-318">PARAMETER_NAME</span><span class="sxs-lookup"><span data-stu-id="d7f3a-318">PARAMETER_NAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d7f3a-319"><strong>adSchemaProcedures</strong></span><span class="sxs-lookup"><span data-stu-id="d7f3a-319"><strong>adSchemaProcedures</strong></span></span></p></td>
<td><p><span data-ttu-id="d7f3a-320">16 </span><span class="sxs-lookup"><span data-stu-id="d7f3a-320">16</span></span></p></td>
<td><p><span data-ttu-id="d7f3a-321">Retorna os procedimentos definidos no catálogo, pertencentes a um usuário específico.</span><span class="sxs-lookup"><span data-stu-id="d7f3a-321">Returns the procedures defined in the catalog that are owned by a given user.</span></span> <span data-ttu-id="d7f3a-322">(Conjunto de linhas PROCEDURES)</span><span class="sxs-lookup"><span data-stu-id="d7f3a-322">(PROCEDURES Rowset)</span></span></p></td>
<td><p><span data-ttu-id="d7f3a-323">PROCEDURE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="d7f3a-323">PROCEDURE_CATALOG</span></span><br />
<span data-ttu-id="d7f3a-324">PROCEDURE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="d7f3a-324">PROCEDURE_SCHEMA</span></span><br />
<span data-ttu-id="d7f3a-325">PROCEDURE_NAME</span><span class="sxs-lookup"><span data-stu-id="d7f3a-325">PROCEDURE_NAME</span></span><br />
<span data-ttu-id="d7f3a-326">PROCEDURE_TYPE</span><span class="sxs-lookup"><span data-stu-id="d7f3a-326">PROCEDURE_TYPE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d7f3a-327"><strong>adSchemaProperties</strong></span><span class="sxs-lookup"><span data-stu-id="d7f3a-327"><strong>adSchemaProperties</strong></span></span></p></td>
<td><p><span data-ttu-id="d7f3a-328">37</span><span class="sxs-lookup"><span data-stu-id="d7f3a-328">37</span></span></p></td>
<td><p><span data-ttu-id="d7f3a-329">Retorna informações sobre as propriedades disponíveis para cada nível de dimensão.</span><span class="sxs-lookup"><span data-stu-id="d7f3a-329">Returns information about the available properties for each level of the dimension.</span></span> <span data-ttu-id="d7f3a-330">(Conjunto de linhas PROPERTIES\*)</span><span class="sxs-lookup"><span data-stu-id="d7f3a-330">(PROPERTIES Rowset \*)</span></span></p></td>
<td><p><span data-ttu-id="d7f3a-331">CATALOG_NAME</span><span class="sxs-lookup"><span data-stu-id="d7f3a-331">CATALOG_NAME</span></span><br />
<span data-ttu-id="d7f3a-332">SCHEMA_NAME</span><span class="sxs-lookup"><span data-stu-id="d7f3a-332">SCHEMA_NAME</span></span><br />
<span data-ttu-id="d7f3a-333">CUBE_NAME</span><span class="sxs-lookup"><span data-stu-id="d7f3a-333">CUBE_NAME</span></span><br />
<span data-ttu-id="d7f3a-334">DIMENSION_UNIQUE_NAME</span><span class="sxs-lookup"><span data-stu-id="d7f3a-334">DIMENSION_UNIQUE_NAME</span></span><br />
<span data-ttu-id="d7f3a-335">HIERARCHY_UNIQUE_NAME</span><span class="sxs-lookup"><span data-stu-id="d7f3a-335">HIERARCHY_UNIQUE_NAME</span></span><br />
<span data-ttu-id="d7f3a-336">LEVEL_UNIQUE_NAME</span><span class="sxs-lookup"><span data-stu-id="d7f3a-336">LEVEL_UNIQUE_NAME</span></span><br />
<span data-ttu-id="d7f3a-337">MEMBER_UNIQUE_NAME</span><span class="sxs-lookup"><span data-stu-id="d7f3a-337">MEMBER_UNIQUE_NAME</span></span><br />
<span data-ttu-id="d7f3a-338">PROPERTY_TYPE</span><span class="sxs-lookup"><span data-stu-id="d7f3a-338">PROPERTY_TYPE</span></span><br />
<span data-ttu-id="d7f3a-339">PROPERTY_NAME</span><span class="sxs-lookup"><span data-stu-id="d7f3a-339">PROPERTY_NAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d7f3a-340"><strong>adSchemaProviderSpecific</strong></span><span class="sxs-lookup"><span data-stu-id="d7f3a-340"><strong>adSchemaProviderSpecific</strong></span></span></p></td>
<td><p><span data-ttu-id="d7f3a-341">-1</span><span class="sxs-lookup"><span data-stu-id="d7f3a-341">-1</span></span></p></td>
<td><p><span data-ttu-id="d7f3a-342">Utilizada se o provedor define suas próprias consultas de esquema não padrão.</span><span class="sxs-lookup"><span data-stu-id="d7f3a-342">Used if the provider defines its own nonstandard schema queries.</span></span></p></td>
<td><p><span data-ttu-id="d7f3a-343">&lt;Específico do provedor&gt;</span><span class="sxs-lookup"><span data-stu-id="d7f3a-343">&lt;Provider specific&gt;</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d7f3a-344"><strong>adSchemaProviderTypes</strong></span><span class="sxs-lookup"><span data-stu-id="d7f3a-344"><strong>adSchemaProviderTypes</strong></span></span></p></td>
<td><p><span data-ttu-id="d7f3a-345">22</span><span class="sxs-lookup"><span data-stu-id="d7f3a-345">22</span></span></p></td>
<td><p><span data-ttu-id="d7f3a-346">Retorna os tipos de dados (base) aceitos pelo provedor de dados.</span><span class="sxs-lookup"><span data-stu-id="d7f3a-346">Returns the (base) data types supported by the data provider.</span></span> <span data-ttu-id="d7f3a-347">(Conjunto de linhas PROVIDER_TYPES)</span><span class="sxs-lookup"><span data-stu-id="d7f3a-347">(PROVIDER_TYPES Rowset)</span></span></p></td>
<td><p><span data-ttu-id="d7f3a-348">DATA_TYPE</span><span class="sxs-lookup"><span data-stu-id="d7f3a-348">DATA_TYPE</span></span><br />
<span data-ttu-id="d7f3a-349">BEST_MATCH</span><span class="sxs-lookup"><span data-stu-id="d7f3a-349">BEST_MATCH</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d7f3a-350"><strong>AdSchemaReferentialConstraints</strong></span><span class="sxs-lookup"><span data-stu-id="d7f3a-350"><strong>AdSchemaReferentialConstraints</strong></span></span></p></td>
<td><p><span data-ttu-id="d7f3a-351">9 </span><span class="sxs-lookup"><span data-stu-id="d7f3a-351">9</span></span></p></td>
<td><p><span data-ttu-id="d7f3a-352">Retorna as restrições de referência definidas no catálogo, pertencentes a um usuário específico.</span><span class="sxs-lookup"><span data-stu-id="d7f3a-352">Returns the referential constraints defined in the catalog that are owned by a given user.</span></span> <span data-ttu-id="d7f3a-353">(Conjunto de linhas REFERENTIAL_CONSTRAINTS)</span><span class="sxs-lookup"><span data-stu-id="d7f3a-353">(REFERENTIAL_CONSTRAINTS Rowset)</span></span></p></td>
<td><p><span data-ttu-id="d7f3a-354">CONSTRAINT_CATALOG</span><span class="sxs-lookup"><span data-stu-id="d7f3a-354">CONSTRAINT_CATALOG</span></span><br />
<span data-ttu-id="d7f3a-355">CONSTRAINT_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="d7f3a-355">CONSTRAINT_SCHEMA</span></span><br />
<span data-ttu-id="d7f3a-356">CONSTRAINT_NAME</span><span class="sxs-lookup"><span data-stu-id="d7f3a-356">CONSTRAINT_NAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d7f3a-357"><strong>adSchemaSchemata</strong></span><span class="sxs-lookup"><span data-stu-id="d7f3a-357"><strong>adSchemaSchemata</strong></span></span></p></td>
<td><p><span data-ttu-id="d7f3a-358">17 </span><span class="sxs-lookup"><span data-stu-id="d7f3a-358">17</span></span></p></td>
<td><p><span data-ttu-id="d7f3a-359">Retorna os esquemas (objetos de banco de dados) pertencentes a um usuário específico.</span><span class="sxs-lookup"><span data-stu-id="d7f3a-359">Returns the schemas (database objects) that are owned by a given user.</span></span> <span data-ttu-id="d7f3a-360">(Conjunto de linhas SCHEMATA)</span><span class="sxs-lookup"><span data-stu-id="d7f3a-360">(SCHEMATA Rowset)</span></span></p></td>
<td><p><span data-ttu-id="d7f3a-361">CATALOG_NAME</span><span class="sxs-lookup"><span data-stu-id="d7f3a-361">CATALOG_NAME</span></span><br />
<span data-ttu-id="d7f3a-362">SCHEMA_NAME</span><span class="sxs-lookup"><span data-stu-id="d7f3a-362">SCHEMA_NAME</span></span><br />
<span data-ttu-id="d7f3a-363">SCHEMA_OWNER</span><span class="sxs-lookup"><span data-stu-id="d7f3a-363">SCHEMA_OWNER</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d7f3a-364"><strong>adSchemaSQLLanguages</strong></span><span class="sxs-lookup"><span data-stu-id="d7f3a-364"><strong>adSchemaSQLLanguages</strong></span></span></p></td>
<td><p><span data-ttu-id="d7f3a-365">18 </span><span class="sxs-lookup"><span data-stu-id="d7f3a-365">18</span></span></p></td>
<td><p><span data-ttu-id="d7f3a-366">Retorna os níveis, as opções e os dialetos de conformidade aceitos pelos dados de processamento de implementação do SQL definidos no catálogo.</span><span class="sxs-lookup"><span data-stu-id="d7f3a-366">Returns the conformance levels, options, and dialects supported by the SQL-implementation processing data defined in the catalog.</span></span> <span data-ttu-id="d7f3a-367">(Conjunto de linhas SQL_LANGUAGES)</span><span class="sxs-lookup"><span data-stu-id="d7f3a-367">(SQL_LANGUAGES Rowset)</span></span></p></td>
<td><p><span data-ttu-id="d7f3a-368">&lt;Nenhum&gt;</span><span class="sxs-lookup"><span data-stu-id="d7f3a-368">&lt;None&gt;</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d7f3a-369"><strong>adSchemaStatistics</strong></span><span class="sxs-lookup"><span data-stu-id="d7f3a-369"><strong>adSchemaStatistics</strong></span></span></p></td>
<td><p><span data-ttu-id="d7f3a-370">19</span><span class="sxs-lookup"><span data-stu-id="d7f3a-370">19</span></span></p></td>
<td><p><span data-ttu-id="d7f3a-371">Retorna as estatísticas definidas no catálogo, pertencentes a um usuário específico.</span><span class="sxs-lookup"><span data-stu-id="d7f3a-371">Returns the statistics defined in the catalog that are owned by a given user.</span></span> <span data-ttu-id="d7f3a-372">(Conjunto de linhas STATISTICS)</span><span class="sxs-lookup"><span data-stu-id="d7f3a-372">(STATISTICS Rowset)</span></span></p></td>
<td><p><span data-ttu-id="d7f3a-373">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="d7f3a-373">TABLE_CATALOG</span></span><br />
<span data-ttu-id="d7f3a-374">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="d7f3a-374">TABLE_SCHEMA</span></span><br />
<span data-ttu-id="d7f3a-375">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="d7f3a-375">TABLE_NAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d7f3a-376"><strong>adSchemaTableConstraints</strong></span><span class="sxs-lookup"><span data-stu-id="d7f3a-376"><strong>adSchemaTableConstraints</strong></span></span></p></td>
<td><p><span data-ttu-id="d7f3a-377">10 </span><span class="sxs-lookup"><span data-stu-id="d7f3a-377">10</span></span></p></td>
<td><p><span data-ttu-id="d7f3a-378">Retorna as restrições de tabela definidas no catálogo, pertencentes a um usuário específico.</span><span class="sxs-lookup"><span data-stu-id="d7f3a-378">Returns the table constraints defined in the catalog that are owned by a given user.</span></span> <span data-ttu-id="d7f3a-379">(Conjunto de linha TABLE_CONSTRAINTS)</span><span class="sxs-lookup"><span data-stu-id="d7f3a-379">(TABLE_CONSTRAINTS Rowset)</span></span></p></td>
<td><p><span data-ttu-id="d7f3a-380">CONSTRAINT_CATALOG</span><span class="sxs-lookup"><span data-stu-id="d7f3a-380">CONSTRAINT_CATALOG</span></span><br />
<span data-ttu-id="d7f3a-381">CONSTRAINT_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="d7f3a-381">CONSTRAINT_SCHEMA</span></span><br />
<span data-ttu-id="d7f3a-382">CONSTRAINT_NAME</span><span class="sxs-lookup"><span data-stu-id="d7f3a-382">CONSTRAINT_NAME</span></span><br />
<span data-ttu-id="d7f3a-383">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="d7f3a-383">TABLE_CATALOG</span></span><br />
<span data-ttu-id="d7f3a-384">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="d7f3a-384">TABLE_SCHEMA</span></span><br />
<span data-ttu-id="d7f3a-385">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="d7f3a-385">TABLE_NAME</span></span><br />
<span data-ttu-id="d7f3a-386">CONSTRAINT_TYPE</span><span class="sxs-lookup"><span data-stu-id="d7f3a-386">CONSTRAINT_TYPE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d7f3a-387"><strong>adSchemaTablePrivileges</strong></span><span class="sxs-lookup"><span data-stu-id="d7f3a-387"><strong>adSchemaTablePrivileges</strong></span></span></p></td>
<td><p><span data-ttu-id="d7f3a-388">14 </span><span class="sxs-lookup"><span data-stu-id="d7f3a-388">14</span></span></p></td>
<td><p><span data-ttu-id="d7f3a-389">Retorna, nas tabelas definidas no catálogo, os privilégios que estão disponíveis para um determinado usuário ou foram concedidos a ele.</span><span class="sxs-lookup"><span data-stu-id="d7f3a-389">Returns the privileges on tables defined in the catalog that are available to, or granted by, a given user.</span></span> <span data-ttu-id="d7f3a-390">(Conjunto de linhas TABLE_PRIVILEGES)</span><span class="sxs-lookup"><span data-stu-id="d7f3a-390">(TABLE_PRIVILEGES Rowset)</span></span></p></td>
<td><p><span data-ttu-id="d7f3a-391">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="d7f3a-391">TABLE_CATALOG</span></span><br />
<span data-ttu-id="d7f3a-392">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="d7f3a-392">TABLE_SCHEMA</span></span><br />
<span data-ttu-id="d7f3a-393">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="d7f3a-393">TABLE_NAME</span></span><br />
<span data-ttu-id="d7f3a-394">GRANTOR</span><span class="sxs-lookup"><span data-stu-id="d7f3a-394">GRANTOR</span></span><br />
<span data-ttu-id="d7f3a-395">GRANTEE</span><span class="sxs-lookup"><span data-stu-id="d7f3a-395">GRANTEE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d7f3a-396"><strong>adSchemaTables</strong></span><span class="sxs-lookup"><span data-stu-id="d7f3a-396"><strong>adSchemaTables</strong></span></span></p></td>
<td><p><span data-ttu-id="d7f3a-397">20</span><span class="sxs-lookup"><span data-stu-id="d7f3a-397">20</span></span></p></td>
<td><p><span data-ttu-id="d7f3a-398">Retorna as tabelas (inclusive as exibições) definidas no catálogo que estão acessíveis para um determinado usuário.</span><span class="sxs-lookup"><span data-stu-id="d7f3a-398">Returns the tables (including views) defined in the catalog that are accessible to a given user.</span></span> <span data-ttu-id="d7f3a-399">(Conjunto de linhas TABLES)</span><span class="sxs-lookup"><span data-stu-id="d7f3a-399">(TABLES Rowset)</span></span></p></td>
<td><p><span data-ttu-id="d7f3a-400">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="d7f3a-400">TABLE_CATALOG</span></span><br />
<span data-ttu-id="d7f3a-401">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="d7f3a-401">TABLE_SCHEMA</span></span><br />
<span data-ttu-id="d7f3a-402">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="d7f3a-402">TABLE_NAME</span></span><br />
<span data-ttu-id="d7f3a-403">TABLE_TYPE</span><span class="sxs-lookup"><span data-stu-id="d7f3a-403">TABLE_TYPE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d7f3a-404"><strong>adSchemaTranslations</strong></span><span class="sxs-lookup"><span data-stu-id="d7f3a-404"><strong>adSchemaTranslations</strong></span></span></p></td>
<td><p><span data-ttu-id="d7f3a-405"> 21 </span><span class="sxs-lookup"><span data-stu-id="d7f3a-405">21</span></span></p></td>
<td><p><span data-ttu-id="d7f3a-406">Retorna as conversões de caracteres definidas no catálogo que estão acessíveis para um usuário específico.</span><span class="sxs-lookup"><span data-stu-id="d7f3a-406">Returns the character translations defined in the catalog that are accessible to a given user.</span></span> <span data-ttu-id="d7f3a-407">(Conjunto de linhas TRANSLATIONS)</span><span class="sxs-lookup"><span data-stu-id="d7f3a-407">(TRANSLATIONS Rowset)</span></span></p></td>
<td><p><span data-ttu-id="d7f3a-408">TRANSLATION_CATALOG</span><span class="sxs-lookup"><span data-stu-id="d7f3a-408">TRANSLATION_CATALOG</span></span><br />
<span data-ttu-id="d7f3a-409">TRANSLATION_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="d7f3a-409">TRANSLATION_SCHEMA</span></span><br />
<span data-ttu-id="d7f3a-410">TRANSLATION_NAME</span><span class="sxs-lookup"><span data-stu-id="d7f3a-410">TRANSLATION_NAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d7f3a-411"><strong>adSchemaTrustees</strong></span><span class="sxs-lookup"><span data-stu-id="d7f3a-411"><strong>adSchemaTrustees</strong></span></span></p></td>
<td><p><span data-ttu-id="d7f3a-412">39</span><span class="sxs-lookup"><span data-stu-id="d7f3a-412">39</span></span></p></td>
<td><p><span data-ttu-id="d7f3a-413">Reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="d7f3a-413">Reserved for future use.</span></span></p></td>
<td><p><br />
</p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d7f3a-414"><strong>adSchemaUsagePrivileges</strong></span><span class="sxs-lookup"><span data-stu-id="d7f3a-414"><strong>adSchemaUsagePrivileges</strong></span></span></p></td>
<td><p><span data-ttu-id="d7f3a-415">15 </span><span class="sxs-lookup"><span data-stu-id="d7f3a-415">15</span></span></p></td>
<td><p><span data-ttu-id="d7f3a-416">Retorna, nos objetos definidos no catálogo, os privilégios USAGE que estão disponíveis para um determinado usuário ou foram concedidos a ele.</span><span class="sxs-lookup"><span data-stu-id="d7f3a-416">Returns the USAGE privileges on objects defined in the catalog that are available to, or granted by, a given user.</span></span> <span data-ttu-id="d7f3a-417">(Conjunto de linhas USAGE_PRIVILEGES)</span><span class="sxs-lookup"><span data-stu-id="d7f3a-417">(USAGE_PRIVILEGES Rowset)</span></span></p></td>
<td><p><span data-ttu-id="d7f3a-418">OBJECT_CATALOG</span><span class="sxs-lookup"><span data-stu-id="d7f3a-418">OBJECT_CATALOG</span></span><br />
<span data-ttu-id="d7f3a-419">OBJECT_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="d7f3a-419">OBJECT_SCHEMA</span></span><br />
<span data-ttu-id="d7f3a-420">OBJECT_NAME</span><span class="sxs-lookup"><span data-stu-id="d7f3a-420">OBJECT_NAME</span></span><br />
<span data-ttu-id="d7f3a-421">OBJECT_TYPE</span><span class="sxs-lookup"><span data-stu-id="d7f3a-421">OBJECT_TYPE</span></span><br />
<span data-ttu-id="d7f3a-422">GRANTOR</span><span class="sxs-lookup"><span data-stu-id="d7f3a-422">GRANTOR</span></span><br />
<span data-ttu-id="d7f3a-423">GRANTEE</span><span class="sxs-lookup"><span data-stu-id="d7f3a-423">GRANTEE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d7f3a-424"><strong>adSchemaViewColumnUsage</strong></span><span class="sxs-lookup"><span data-stu-id="d7f3a-424"><strong>adSchemaViewColumnUsage</strong></span></span></p></td>
<td><p><span data-ttu-id="d7f3a-425">24</span><span class="sxs-lookup"><span data-stu-id="d7f3a-425">24</span></span></p></td>
<td><p><span data-ttu-id="d7f3a-426">Retorna as colunas das quais as tabelas exibidas, definidas no catálogo e pertencentes a um usuário específico, são dependentes.</span><span class="sxs-lookup"><span data-stu-id="d7f3a-426">Returns the columns on which viewed tables, defined in the catalog and owned by a given user, are dependent.</span></span> <span data-ttu-id="d7f3a-427">(Conjunto de linhas VIEW_COLUMN_USAGE)</span><span class="sxs-lookup"><span data-stu-id="d7f3a-427">(VIEW_COLUMN_USAGE Rowset)</span></span></p></td>
<td><p><span data-ttu-id="d7f3a-428">VIEW_CATALOG</span><span class="sxs-lookup"><span data-stu-id="d7f3a-428">VIEW_CATALOG</span></span><br />
<span data-ttu-id="d7f3a-429">VIEW_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="d7f3a-429">VIEW_SCHEMA</span></span><br />
<span data-ttu-id="d7f3a-430">VIEW_NAME</span><span class="sxs-lookup"><span data-stu-id="d7f3a-430">VIEW_NAME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d7f3a-431"><strong>adSchemaViews</strong></span><span class="sxs-lookup"><span data-stu-id="d7f3a-431"><strong>adSchemaViews</strong></span></span></p></td>
<td><p><span data-ttu-id="d7f3a-432">23</span><span class="sxs-lookup"><span data-stu-id="d7f3a-432">23</span></span></p></td>
<td><p><span data-ttu-id="d7f3a-433">Retorna as exibições definidas no catálogo que estão acessíveis para um determinado usuário.</span><span class="sxs-lookup"><span data-stu-id="d7f3a-433">Returns the views defined in the catalog that are accessible to a given user.</span></span> <span data-ttu-id="d7f3a-434">(Conjunto de linhas VIEWS)</span><span class="sxs-lookup"><span data-stu-id="d7f3a-434">(VIEWS Rowset)</span></span></p></td>
<td><p><span data-ttu-id="d7f3a-435">TABLE_CATALOG</span><span class="sxs-lookup"><span data-stu-id="d7f3a-435">TABLE_CATALOG</span></span><br />
<span data-ttu-id="d7f3a-436">TABLE_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="d7f3a-436">TABLE_SCHEMA</span></span><br />
<span data-ttu-id="d7f3a-437">TABLE_NAME</span><span class="sxs-lookup"><span data-stu-id="d7f3a-437">TABLE_NAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d7f3a-438"><strong>adSchemaViewTableUsage</strong></span><span class="sxs-lookup"><span data-stu-id="d7f3a-438"><strong>adSchemaViewTableUsage</strong></span></span></p></td>
<td><p><span data-ttu-id="d7f3a-439">25</span><span class="sxs-lookup"><span data-stu-id="d7f3a-439">25</span></span></p></td>
<td><p><span data-ttu-id="d7f3a-440">Retorna as tabelas das quais as tabelas exibidas, definidas no catálogo e pertencentes a um usuário específico, são dependentes.</span><span class="sxs-lookup"><span data-stu-id="d7f3a-440">Returns the tables on which viewed tables, defined in the catalog and owned by a given user, are dependent.</span></span> <span data-ttu-id="d7f3a-441">(Conjunto de linhas VIEW_TABLE_USAGE)</span><span class="sxs-lookup"><span data-stu-id="d7f3a-441">(VIEW_TABLE_USAGE Rowset)</span></span></p></td>
<td><p><span data-ttu-id="d7f3a-442">VIEW_CATALOG</span><span class="sxs-lookup"><span data-stu-id="d7f3a-442">VIEW_CATALOG</span></span><br />
<span data-ttu-id="d7f3a-443">VIEW_SCHEMA</span><span class="sxs-lookup"><span data-stu-id="d7f3a-443">VIEW_SCHEMA</span></span><br />
<span data-ttu-id="d7f3a-444">VIEW_NAME</span><span class="sxs-lookup"><span data-stu-id="d7f3a-444">VIEW_NAME</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="d7f3a-445">Equivalente do ADO/WFC</span><span class="sxs-lookup"><span data-stu-id="d7f3a-445">ADO/WFC equivalent</span></span>

<span data-ttu-id="d7f3a-446">Pacote: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="d7f3a-446">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="d7f3a-447">Constant</span><span class="sxs-lookup"><span data-stu-id="d7f3a-447">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d7f3a-448">AdoEnums.Schema.ASSERTS</span><span class="sxs-lookup"><span data-stu-id="d7f3a-448">AdoEnums.Schema.ASSERTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d7f3a-449">AdoEnums.Schema.CATALOGS</span><span class="sxs-lookup"><span data-stu-id="d7f3a-449">AdoEnums.Schema.CATALOGS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d7f3a-450">AdoEnums.Schema.CHARACTERSETS</span><span class="sxs-lookup"><span data-stu-id="d7f3a-450">AdoEnums.Schema.CHARACTERSETS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d7f3a-451">AdoEnums.Schema.CHECKCONSTRAINTS</span><span class="sxs-lookup"><span data-stu-id="d7f3a-451">AdoEnums.Schema.CHECKCONSTRAINTS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d7f3a-452">AdoEnums.Schema.COLLATIONS</span><span class="sxs-lookup"><span data-stu-id="d7f3a-452">AdoEnums.Schema.COLLATIONS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d7f3a-453">AdoEnums.Schema.COLUMNPRIVILEGES</span><span class="sxs-lookup"><span data-stu-id="d7f3a-453">AdoEnums.Schema.COLUMNPRIVILEGES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d7f3a-454">AdoEnums.Schema.COLUMNS</span><span class="sxs-lookup"><span data-stu-id="d7f3a-454">AdoEnums.Schema.COLUMNS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d7f3a-455">AdoEnums.Schema.COLUMNSDOMAINUSAGE</span><span class="sxs-lookup"><span data-stu-id="d7f3a-455">AdoEnums.Schema.COLUMNSDOMAINUSAGE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d7f3a-456">AdoEnums.Schema.CONSTRAINTCOLUMNUSAGE</span><span class="sxs-lookup"><span data-stu-id="d7f3a-456">AdoEnums.Schema.CONSTRAINTCOLUMNUSAGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d7f3a-457">AdoEnums.Schema.CONSTRAINTTABLEUSAGE</span><span class="sxs-lookup"><span data-stu-id="d7f3a-457">AdoEnums.Schema.CONSTRAINTTABLEUSAGE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d7f3a-458">AdoEnums.Schema.CUBES</span><span class="sxs-lookup"><span data-stu-id="d7f3a-458">AdoEnums.Schema.CUBES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d7f3a-459">AdoEnums.Schema.DBINFOKEYWORDS</span><span class="sxs-lookup"><span data-stu-id="d7f3a-459">AdoEnums.Schema.DBINFOKEYWORDS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d7f3a-460">AdoEnums.Schema.DBINFOLITERALS</span><span class="sxs-lookup"><span data-stu-id="d7f3a-460">AdoEnums.Schema.DBINFOLITERALS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d7f3a-461">AdoEnums.Schema.DIMENSIONS</span><span class="sxs-lookup"><span data-stu-id="d7f3a-461">AdoEnums.Schema.DIMENSIONS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d7f3a-462">AdoEnums.Schema.FOREIGNKEYS</span><span class="sxs-lookup"><span data-stu-id="d7f3a-462">AdoEnums.Schema.FOREIGNKEYS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d7f3a-463">AdoEnums.Schema.HIERARCHIES</span><span class="sxs-lookup"><span data-stu-id="d7f3a-463">AdoEnums.Schema.HIERARCHIES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d7f3a-464">AdoEnums.Schema.INDEXES</span><span class="sxs-lookup"><span data-stu-id="d7f3a-464">AdoEnums.Schema.INDEXES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d7f3a-465">AdoEnums.Schema.KEYCOLUMNUSAGE</span><span class="sxs-lookup"><span data-stu-id="d7f3a-465">AdoEnums.Schema.KEYCOLUMNUSAGE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d7f3a-466">AdoEnums.Schema.LEVELS</span><span class="sxs-lookup"><span data-stu-id="d7f3a-466">AdoEnums.Schema.LEVELS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d7f3a-467">AdoEnums.Schema.MEASURES</span><span class="sxs-lookup"><span data-stu-id="d7f3a-467">AdoEnums.Schema.MEASURES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d7f3a-468">AdoEnums.Schema.MEMBERS</span><span class="sxs-lookup"><span data-stu-id="d7f3a-468">AdoEnums.Schema.MEMBERS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d7f3a-469">AdoEnums.Schema.PRIMARYKEYS</span><span class="sxs-lookup"><span data-stu-id="d7f3a-469">AdoEnums.Schema.PRIMARYKEYS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d7f3a-470">AdoEnums.Schema.PROCEDURECOLUMNS</span><span class="sxs-lookup"><span data-stu-id="d7f3a-470">AdoEnums.Schema.PROCEDURECOLUMNS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d7f3a-471">AdoEnums.Schema.PROCEDUREPARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d7f3a-471">AdoEnums.Schema.PROCEDUREPARAMETERS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d7f3a-472">AdoEnums.Schema.PROCEDURES</span><span class="sxs-lookup"><span data-stu-id="d7f3a-472">AdoEnums.Schema.PROCEDURES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d7f3a-473">AdoEnums.Schema.PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="d7f3a-473">AdoEnums.Schema.PROPERTIES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d7f3a-474">AdoEnums.Schema.PROVIDERSPECIFIC</span><span class="sxs-lookup"><span data-stu-id="d7f3a-474">AdoEnums.Schema.PROVIDERSPECIFIC</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d7f3a-475">AdoEnums.Schema.PROVIDERTYPES</span><span class="sxs-lookup"><span data-stu-id="d7f3a-475">AdoEnums.Schema.PROVIDERTYPES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d7f3a-476">AdoEnums.Schema.REFERENTIALCONTRAINTS</span><span class="sxs-lookup"><span data-stu-id="d7f3a-476">AdoEnums.Schema.REFERENTIALCONTRAINTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d7f3a-477">AdoEnums.Schema.SCHEMATA</span><span class="sxs-lookup"><span data-stu-id="d7f3a-477">AdoEnums.Schema.SCHEMATA</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d7f3a-478">AdoEnums.Schema.SQLLANGUAGES</span><span class="sxs-lookup"><span data-stu-id="d7f3a-478">AdoEnums.Schema.SQLLANGUAGES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d7f3a-479">AdoEnums.Schema.STATISTICS</span><span class="sxs-lookup"><span data-stu-id="d7f3a-479">AdoEnums.Schema.STATISTICS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d7f3a-480">AdoEnums.Schema.TABLECONSTRAINTS</span><span class="sxs-lookup"><span data-stu-id="d7f3a-480">AdoEnums.Schema.TABLECONSTRAINTS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d7f3a-481">AdoEnums.Schema.TABLEPRIVILEGES</span><span class="sxs-lookup"><span data-stu-id="d7f3a-481">AdoEnums.Schema.TABLEPRIVILEGES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d7f3a-482">AdoEnums.Schema.TABLES</span><span class="sxs-lookup"><span data-stu-id="d7f3a-482">AdoEnums.Schema.TABLES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d7f3a-483">AdoEnums.Schema.TRANSLATIONS</span><span class="sxs-lookup"><span data-stu-id="d7f3a-483">AdoEnums.Schema.TRANSLATIONS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d7f3a-484">AdoEnums.Schema.TRUSTEES</span><span class="sxs-lookup"><span data-stu-id="d7f3a-484">AdoEnums.Schema.TRUSTEES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d7f3a-485">AdoEnums.Schema.USAGEPRIVILEGES</span><span class="sxs-lookup"><span data-stu-id="d7f3a-485">AdoEnums.Schema.USAGEPRIVILEGES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d7f3a-486">AdoEnums.Schema.VIEWCOLUMNUSAGE</span><span class="sxs-lookup"><span data-stu-id="d7f3a-486">AdoEnums.Schema.VIEWCOLUMNUSAGE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d7f3a-487">AdoEnums.Schema.VIEWS</span><span class="sxs-lookup"><span data-stu-id="d7f3a-487">AdoEnums.Schema.VIEWS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d7f3a-488">AdoEnums.Schema.VIEWTABLEUSAGE</span><span class="sxs-lookup"><span data-stu-id="d7f3a-488">AdoEnums.Schema.VIEWTABLEUSAGE</span></span></p></td>
</tr>
</tbody>
</table>

