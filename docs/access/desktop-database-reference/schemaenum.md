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
# <a name="schemaenum"></a>SchemaEnum

**Aplica-se ao:** Access 2013, Office 2013

Especifica o tipo de esquema do **Recordset** que o método [OpenSchema](openschema-method-ado.md) recupera.

## <a name="remarks"></a>Comentários

Informações adicionais sobre a função e as colunas retornadas para cada constante do ADO podem ser encontradas nos tópicos do Apêndice B do manual *OLE DB Programmers Reference (Referência para programadores do OLE DB)*. O nome de cada tópico está listado entre parênteses na seção Descrição da tabela a seguir.

Informações adicionais sobre a função e as colunas retornadas para cada constante do ADO MD podem ser encontradas nos tópicos do Capítulo 23 da documentação *OLE DB for OLAP (OLE DB para OLAP)*. O nome de cada tópico está listado entre parênteses e marcado com um asterisco (\*) na coluna Descrição da tabela a seguir.

Converta os tipos de dados das colunas na documentação OLE DB para tipos de dados do ADO, consultando a coluna Descrição do tópico ADO [DataTypeEnum](datatypeenum.md). Por exemplo, um tipo de dados OLE DB **de\_DbType WSTR** é equivalente a um tipo de dados do ADO de **adWChar**.

O ADO gera resultados como esquema para as constantes **adSchemaDBInfoKeywords** e **adSchemaDBInfoLiterals**. O ADO cria um **Recordset**e, em seguida, preenche cada linha com os valores retornados respectivamente pelos métodos **IDBInfo::** GetKeywords e **IDBInfo:: GetLiteralInfo** . Informações adicionais sobre esses métodos podem ser encontradas na seção IDBInfo da *referência do programador do OLE DB*.

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
<th><p>Constant</p></th>
<th><p>Valor</p></th>
<th><p>Descrição</p></th>
<th><p>Colunas de restrição</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>adSchemaAsserts</strong></p></td>
<td><p>,0</p></td>
<td><p>Retorna as asserções definidas no catálogo, pertencentes a um usuário específico. (Conjunto de linhas ASSERTIONS)</p></td>
<td><p>CONSTRAINT_CATALOG<br />
CONSTRAINT_SCHEMA<br />
CONSTRAINT_NAME</p></td>
</tr>
<tr class="even">
<td><p><strong>adSchemaCatalogs</strong></p></td>
<td><p>1</p></td>
<td><p>Retorna os atributos físicos associados aos catálogos acessíveis do DBMS. (Conjunto de linhas CATALOGS)</p></td>
<td><p>CATALOG_NAME</p></td>
</tr>
<tr class="odd">
<td><p><strong>adSchemaCharacterSets</strong></p></td>
<td><p>duas</p></td>
<td><p>Retorna os conjuntos de caracteres definidos no catálogo que estão acessíveis para um determinado usuário. (Conjunto de linhas CHARACTER_SETS)</p></td>
<td><p>CHARACTER_SET_CATALOG<br />
CHARACTER_SET_SCHEMA<br />
CHARACTER_SET_NAME</p></td>
</tr>
<tr class="even">
<td><p><strong>adSchemaCheckConstraints</strong></p></td>
<td><p>0,5</p></td>
<td><p>Retorna as restrições de verificação definidas no catálogo, pertencentes a um usuário específico. (Conjunto de linhas CHECK_CONSTRAINTS)</p></td>
<td><p>CONSTRAINT_CATALOG<br />
CONSTRAINT_SCHEMA<br />
CONSTRAINT_NAME</p></td>
</tr>
<tr class="odd">
<td><p><strong>adSchemaCollations</strong></p></td>
<td><p>3D</p></td>
<td><p>Retorna as coleções de caracteres definidas no catálogo que estão acessíveis para um determinado usuário. (Conjunto de linhas COLLATIONS)</p></td>
<td><p>COLLATION_CATALOG<br />
COLLATION_SCHEMA<br />
COLLATION_NAME</p></td>
</tr>
<tr class="even">
<td><p><strong>adSchemaColumnPrivileges</strong></p></td>
<td><p>Treze</p></td>
<td><p>Retorna, nas colunas das tabelas definidas no catálogo, os privilégios que estão disponíveis para um determinado usuário ou foram concedidos a ele. (Conjunto de linhas COLUMN_PRIVILEGES)</p></td>
<td><p>TABLE_CATALOG<br />
TABLE_SCHEMA<br />
TABLE_NAME<br />
COLUMN_NAME<br />
CESSO<br />
GRANTEE</p></td>
</tr>
<tr class="odd">
<td><p><strong>adSchemaColumns</strong></p></td>
<td><p>quatro</p></td>
<td><p>Retorna as colunas das tabelas (inclusive as exibições) definidas no catálogo que estão acessíveis para um determinado usuário. (Conjunto de linhas COLUMNS)</p></td>
<td><p>TABLE_CATALOG<br />
TABLE_SCHEMA<br />
TABLE_NAME<br />
COLUMN_NAME</p></td>
</tr>
<tr class="even">
<td><p><strong>adSchemaColumnsDomainUsage</strong></p></td>
<td><p>11</p></td>
<td><p>Retorna as colunas definidas no catálogo que são dependentes de um domínio definido no catálogo e pertencem a um determinado usuário. (Conjunto de linhas COLUMN_DOMAIN_USAGE)</p></td>
<td><p>DOMAIN_CATALOG<br />
DOMAIN_SCHEMA<br />
\<br />
COLUMN_NAME</p></td>
</tr>
<tr class="odd">
<td><p><strong>adSchemaConstraintColumnUsage</strong></p></td>
<td><p>6</p></td>
<td><p>Retorna as colunas usadas por restrições de referência, restrições exclusivas, restrições de verificação e asserções, definidas no catálogo e pertencentes a um usuário específico. (Conjunto de linhas CONSTRAINT_COLUMN_USAGE)</p></td>
<td><p>TABLE_CATALOG<br />
TABLE_SCHEMA<br />
TABLE_NAME<br />
COLUMN_NAME</p></td>
</tr>
<tr class="even">
<td><p><strong>adSchemaConstraintTableUsage</strong></p></td>
<td><p>178</p></td>
<td><p>Retorna as tabelas usadas por restrições de referência, restrições exclusivas, restrições de verificação e asserções, definidas no catálogo e pertencentes a um usuário específico. (Conjunto de linhas CONSTRAINT_TABLE_USAGE)</p></td>
<td><p>TABLE_CATALOG<br />
TABLE_SCHEMA<br />
TABLE_NAME</p></td>
</tr>
<tr class="odd">
<td><p><strong>adSchemaCubes</strong></p></td>
<td><p>32</p></td>
<td><p>Retorna informações sobre os cubos disponíveis em um esquema (ou o catálogo se o provedor não oferecer suporte a esquemas). (Conjunto de linhas CUBES*)</p></td>
<td><p>CATALOG_NAME<br />
SCHEMA_NAME<br />
CUBE_NAME</p></td>
</tr>
<tr class="even">
<td><p><strong>adSchemaDBInfoKeywords</strong></p></td>
<td><p>até</p></td>
<td><p>Retorna uma lista de palavras-chave específicas do provedor. (IDBInfo:: getKeywords *)</p></td>
<td><p>&lt;Nenhum&gt;</p></td>
</tr>
<tr class="odd">
<td><p><strong>adSchemaDBInfoLiterals</strong></p></td>
<td><p>31</p></td>
<td><p>Retorna uma lista de literais específicos do provedor utilizados em comandos de texto. (IDBInfo:: GetLiteralInfo *)</p></td>
<td><p>&lt;Nenhum&gt;</p></td>
</tr>
<tr class="even">
<td><p><strong>adSchemaDimensions</strong></p></td>
<td><p>33</p></td>
<td><p>Retorna informações sobre as dimensões em um determinado cubo. Ele tem uma linha para cada dimensão. (Conjunto de linhas DIMENSIONS*)</p></td>
<td><p>CATALOG_NAME<br />
SCHEMA_NAME<br />
CUBE_NAME<br />
DIMENSION_NAME<br />
DIMENSION_UNIQUE_NAME</p></td>
</tr>
<tr class="odd">
<td><p><strong>adSchemaForeignKeys</strong></p></td>
<td><p>27</p></td>
<td><p>Retorna as colunas de chave estrangeira definidas no catálogo por um determinado usuário. (Conjunto de linhas FOREIGN_KEYS)</p></td>
<td><p>PK_TABLE_CATALOG<br />
PK_TABLE_SCHEMA<br />
PK_TABLE_NAME<br />
FK_TABLE_CATALOG<br />
FK_TABLE_SCHEMA<br />
FK_TABLE_NAME</p></td>
</tr>
<tr class="even">
<td><p><strong>adSchemaHierarchies</strong></p></td>
<td><p>34</p></td>
<td><p>Retorna informações sobre as hierarquias disponíveis em uma dimensão. (Conjunto de linhas HIERARCHIES*)</p></td>
<td><p>CATALOG_NAME<br />
SCHEMA_NAME<br />
CUBE_NAME<br />
DIMENSION_UNIQUE_NAME<br />
HIERARCHY_NAME<br />
HIERARCHY_UNIQUE_NAME</p></td>
</tr>
<tr class="odd">
<td><p><strong>adSchemaIndexes</strong></p></td>
<td><p>3,6</p></td>
<td><p>Retorna os índices definidos no catálogo, pertencentes a um usuário específico. (Conjunto de linhas INDEXES)</p></td>
<td><p>TABLE_CATALOG<br />
TABLE_SCHEMA<br />
INDEX_NAME<br />
Escreva<br />
TABLE_NAME</p></td>
</tr>
<tr class="even">
<td><p><strong>adSchemaKeyColumnUsage</strong></p></td>
<td><p>8</p></td>
<td><p>Retorna as colunas definidas no catálogo, restritas a chaves por um usuário específico. (Conjunto de linhas KEY_COLUMN_USAGE)</p></td>
<td><p>CONSTRAINT_CATALOG<br />
CONSTRAINT_SCHEMA<br />
CONSTRAINT_NAME<br />
TABLE_CATALOG<br />
TABLE_SCHEMA<br />
TABLE_NAME<br />
COLUMN_NAME</p></td>
</tr>
<tr class="odd">
<td><p><strong>adSchemaLevels</strong></p></td>
<td><p>35</p></td>
<td><p>Retorna informações sobre os níveis disponíveis em uma dimensão. (Conjunto de linhas LEVELS*)</p></td>
<td><p>CATALOG_NAME<br />
SCHEMA_NAME<br />
CUBE_NAME<br />
DIMENSION_UNIQUE_NAME<br />
HIERARCHY_UNIQUE_NAME<br />
LEVEL_NAME<br />
LEVEL_UNIQUE_NAME</p></td>
</tr>
<tr class="even">
<td><p><strong>adSchemaMeasures</strong></p></td>
<td><p>36</p></td>
<td><p>Retorna informações sobre as medidas disponíveis. (Conjunto de linhas MEASURES*)</p></td>
<td><p>CATALOG_NAME<br />
SCHEMA_NAME<br />
CUBE_NAME<br />
MEASURE_NAME<br />
MEASURE_UNIQUE_NAME</p></td>
</tr>
<tr class="odd">
<td><p><strong>adSchemaMembers</strong></p></td>
<td><p>38</p></td>
<td><p>Retorna informações sobre os membros disponíveis. (Conjunto de linhas MEMBERS*)</p></td>
<td><p>CATALOG_NAME<br />
SCHEMA_NAME<br />
CUBE_NAME<br />
DIMENSION_UNIQUE_NAME<br />
HIERARCHY_UNIQUE_NAME<br />
LEVEL_UNIQUE_NAME<br />
LEVEL_NUMBER<br />
MEMBER_NAME<br />
MEMBER_UNIQUE_NAME<br />
MEMBER_CAPTION<br />
MEMBER_TYPE<br />
Operador Tree (para obter mais informações, consulte a documentação do OLE DB para OLAP).</p></td>
</tr>
<tr class="even">
<td><p><strong>adSchemaPrimaryKeys</strong></p></td>
<td><p>28</p></td>
<td><p>Retorna as colunas de chave principal definidas no catálogo por um determinado usuário. (Conjunto de linhas PRIMARY_KEYS)</p></td>
<td><p>PK_TABLE_CATALOG<br />
PK_TABLE_SCHEMA<br />
PK_TABLE_NAME</p></td>
</tr>
<tr class="odd">
<td><p><strong>adSchemaProcedureColumns</strong></p></td>
<td><p>anos</p></td>
<td><p>Retorna informações sobre as colunas de conjuntos de linhas por procedimentos. (Conjunto de linhas PROCEDURE_COLUMNS)</p></td>
<td><p>PROCEDURE_CATALOG<br />
PROCEDURE_SCHEMA<br />
PROCEDURE_NAME<br />
COLUMN_NAME</p></td>
</tr>
<tr class="even">
<td><p><strong>adSchemaProcedureParameters</strong></p></td>
<td><p>660</p></td>
<td><p>Retorna informações sobre parâmetros e códigos de retorno de procedimentos. (Conjunto de linhas PROCEDURE_PARAMETERS)</p></td>
<td><p>PROCEDURE_CATALOG<br />
PROCEDURE_SCHEMA<br />
PROCEDURE_NAME<br />
PARAMETER_NAME</p></td>
</tr>
<tr class="odd">
<td><p><strong>adSchemaProcedures</strong></p></td>
<td><p>dezesseis</p></td>
<td><p>Retorna os procedimentos definidos no catálogo, pertencentes a um usuário específico. (Conjunto de linhas PROCEDURES)</p></td>
<td><p>PROCEDURE_CATALOG<br />
PROCEDURE_SCHEMA<br />
PROCEDURE_NAME<br />
PROCEDURE_TYPE</p></td>
</tr>
<tr class="even">
<td><p><strong>adSchemaProperties</strong></p></td>
<td><p>37</p></td>
<td><p>Retorna informações sobre as propriedades disponíveis para cada nível de dimensão. (Conjunto de linhas PROPERTIES*)</p></td>
<td><p>CATALOG_NAME<br />
SCHEMA_NAME<br />
CUBE_NAME<br />
DIMENSION_UNIQUE_NAME<br />
HIERARCHY_UNIQUE_NAME<br />
LEVEL_UNIQUE_NAME<br />
MEMBER_UNIQUE_NAME<br />
PROPERTY_TYPE<br />
PROPERTY_NAME</p></td>
</tr>
<tr class="odd">
<td><p><strong>adSchemaProviderSpecific</strong></p></td>
<td><p>-1</p></td>
<td><p>Utilizada se o provedor define suas próprias consultas de esquema não padrão.</p></td>
<td><p>&lt;Específico do provedor&gt;</p></td>
</tr>
<tr class="even">
<td><p><strong>adSchemaProviderTypes</strong></p></td>
<td><p>22</p></td>
<td><p>Retorna os tipos de dados (base) aceitos pelo provedor de dados. (Conjunto de linhas PROVIDER_TYPES)</p></td>
<td><p>DATA_TYPE<br />
BEST_MATCH</p></td>
</tr>
<tr class="odd">
<td><p><strong>AdSchemaReferentialConstraints</strong></p></td>
<td><p>241</p></td>
<td><p>Retorna as restrições de referência definidas no catálogo, pertencentes a um usuário específico. (Conjunto de linhas REFERENTIAL_CONSTRAINTS)</p></td>
<td><p>CONSTRAINT_CATALOG<br />
CONSTRAINT_SCHEMA<br />
CONSTRAINT_NAME</p></td>
</tr>
<tr class="even">
<td><p><strong>adSchemaSchemata</strong></p></td>
<td><p>17.07.06</p></td>
<td><p>Retorna os esquemas (objetos de banco de dados) pertencentes a um usuário específico. (Conjunto de linhas SCHEMATA)</p></td>
<td><p>CATALOG_NAME<br />
SCHEMA_NAME<br />
SCHEMA_OWNER</p></td>
</tr>
<tr class="odd">
<td><p><strong>adSchemaSQLLanguages</strong></p></td>
<td><p>anos</p></td>
<td><p>Retorna os níveis, as opções e os dialetos de conformidade aceitos pelos dados de processamento de implementação do SQL definidos no catálogo. (Conjunto de linhas SQL_LANGUAGES)</p></td>
<td><p>&lt;Nenhum&gt;</p></td>
</tr>
<tr class="even">
<td><p><strong>adSchemaStatistics</strong></p></td>
<td><p>19</p></td>
<td><p>Retorna as estatísticas definidas no catálogo, pertencentes a um usuário específico. (Conjunto de linhas STATISTICS)</p></td>
<td><p>TABLE_CATALOG<br />
TABLE_SCHEMA<br />
TABLE_NAME</p></td>
</tr>
<tr class="odd">
<td><p><strong>adSchemaTableConstraints</strong></p></td>
<td><p>254</p></td>
<td><p>Retorna as restrições de tabela definidas no catálogo, pertencentes a um usuário específico. (Conjunto de linha TABLE_CONSTRAINTS)</p></td>
<td><p>CONSTRAINT_CATALOG<br />
CONSTRAINT_SCHEMA<br />
CONSTRAINT_NAME<br />
TABLE_CATALOG<br />
TABLE_SCHEMA<br />
TABLE_NAME<br />
CONSTRAINT_TYPE</p></td>
</tr>
<tr class="even">
<td><p><strong>adSchemaTablePrivileges</strong></p></td>
<td><p>14</p></td>
<td><p>Retorna, nas tabelas definidas no catálogo, os privilégios que estão disponíveis para um determinado usuário ou foram concedidos a ele. (Conjunto de linhas TABLE_PRIVILEGES)</p></td>
<td><p>TABLE_CATALOG<br />
TABLE_SCHEMA<br />
TABLE_NAME<br />
CESSO<br />
GRANTEE</p></td>
</tr>
<tr class="odd">
<td><p><strong>adSchemaTables</strong></p></td>
<td><p>508</p></td>
<td><p>Retorna as tabelas (inclusive as exibições) definidas no catálogo que estão acessíveis para um determinado usuário. (Conjunto de linhas TABLES)</p></td>
<td><p>TABLE_CATALOG<br />
TABLE_SCHEMA<br />
TABLE_NAME<br />
TABLE_TYPE</p></td>
</tr>
<tr class="even">
<td><p><strong>adSchemaTranslations</strong></p></td>
<td><p>21</p></td>
<td><p>Retorna as conversões de caracteres definidas no catálogo que estão acessíveis para um usuário específico. (Conjunto de linhas TRANSLATIONS)</p></td>
<td><p>TRANSLATION_CATALOG<br />
TRANSLATION_SCHEMA<br />
TRANSLATION_NAME</p></td>
</tr>
<tr class="odd">
<td><p><strong>adSchemaTrustees</strong></p></td>
<td><p>39</p></td>
<td><p>Reservado para uso futuro.</p></td>
<td><p><br />
</p></td>
</tr>
<tr class="even">
<td><p><strong>adSchemaUsagePrivileges</strong></p></td>
<td><p>15</p></td>
<td><p>Retorna, nos objetos definidos no catálogo, os privilégios USAGE que estão disponíveis para um determinado usuário ou foram concedidos a ele. (Conjunto de linhas USAGE_PRIVILEGES)</p></td>
<td><p>OBJECT_CATALOG<br />
OBJECT_SCHEMA<br />
OBJECT_NAME<br />
OBJECT_TYPE<br />
CESSO<br />
GRANTEE</p></td>
</tr>
<tr class="odd">
<td><p><strong>adSchemaViewColumnUsage</strong></p></td>
<td><p>dia</p></td>
<td><p>Retorna as colunas das quais as tabelas exibidas, definidas no catálogo e pertencentes a um usuário específico, são dependentes. (Conjunto de linhas VIEW_COLUMN_USAGE)</p></td>
<td><p>VIEW_CATALOG<br />
VIEW_SCHEMA<br />
VIEW_NAME</p></td>
</tr>
<tr class="even">
<td><p><strong>adSchemaViews</strong></p></td>
<td><p>23</p></td>
<td><p>Retorna as exibições definidas no catálogo que estão acessíveis para um determinado usuário. (Conjunto de linhas VIEWS)</p></td>
<td><p>TABLE_CATALOG<br />
TABLE_SCHEMA<br />
TABLE_NAME</p></td>
</tr>
<tr class="odd">
<td><p><strong>adSchemaViewTableUsage</strong></p></td>
<td><p>25</p></td>
<td><p>Retorna as tabelas das quais as tabelas exibidas, definidas no catálogo e pertencentes a um usuário específico, são dependentes. (Conjunto de linhas VIEW_TABLE_USAGE)</p></td>
<td><p>VIEW_CATALOG<br />
VIEW_SCHEMA<br />
VIEW_NAME</p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a>Equivalente do ADO/WFC

Pacote: **com.ms.wfc.data**

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Constant</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>AdoEnums. Schema. ASSERTs</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums. Schema. CATALOGs</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums. Schema. CHARACTERSETS</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums. Schema. CHECKCONSTRAINTS</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums. Schema. COLLATIONs</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums. Schema. COLUMNPRIVILEGES</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums. Schema. COLUMNS</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums. Schema. COLUMNSDOMAINUSAGE</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums. Schema. CONSTRAINTCOLUMNUSAGE</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums. Schema. CONSTRAINTTABLEUSAGE</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums. Schema. CUBEs</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums. Schema. DBINFOKEYWORDS</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums. Schema. DBINFOLITERALS</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums. Schema. DIMENSIONs</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums. Schema. FOREIGNKEYS</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums. Schema. HIERARQUIAs</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums. Schema. Indexes</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums. Schema. KEYCOLUMNUSAGE</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums. Schema. LEVELs</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums. Schema. MEASUREs</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums. Schema. MEMBERs</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums. Schema. PRIMARYKEY</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums. Schema. PROCEDURECOLUMNS</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums. Schema. PROCEDUREparameters</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums. Schema. PROCEDUREs</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums. Schema. PROPERTIES</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums. Schema. PROVIDERSPECIFIC</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums. Schema. PROVIDERTYPES</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums. Schema. REFERENTIALCONTRAINTS</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums. Schema. SCHEMATA</p></td>
</tr>
<tr class="odd">
<td><p>Idiomas AdoEnums. Schema.</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums. Schema. STATISTICs</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums. Schema. TABLECONSTRAINTS</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums. Schema. TABLEPRIVILEGES</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums. Schema. TABLEs</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums. Schema. TRANSLATIONs</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums. Schema. TRUSTers</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums. Schema. USAGEPRIVILEGES</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums. Schema. VIEWCOLUMNUSAGE</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums. Schema. views</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums. Schema. VIEWTABLEUSAGE</p></td>
</tr>
</tbody>
</table>

