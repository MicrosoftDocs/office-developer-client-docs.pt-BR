---
title: SchemaEnum (referência de banco de dados da área de trabalho do Access)
TOCTitle: SchemaEnum
ms:assetid: 6147b682-3c4f-ea91-fff6-ac73107d206d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249359(v=office.15)
ms:contentKeyID: 48545208
ms.date: 10/18/2018
mtps_version: v=office.15
ms.openlocfilehash: a6f1e174253904adf7392aa7ae19786103e55843
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25863350"
---
# <a name="schemaenum"></a>SchemaEnum

**Aplica-se a**: Access 2013 | Office 2013

Especifica o tipo de esquema do **Recordset** que o método [OpenSchema](openschema-method-ado.md) recupera.

## <a name="remarks"></a>Comentários

Informações adicionais sobre a função e colunas retornadas para cada constante ADO pode ser encontrado nos tópicos do Apêndice B do *OLE DB programadores referência*. O nome de cada tópico é listado entre parênteses na seção descrição da tabela a seguir.

Informações adicionais sobre a função e colunas retornadas para cada constante do ADO MD podem ser encontradas nos tópicos de 23 de capítulo da documentação do *OLE DB para OLAP* . O nome de cada tópico é listado entre parênteses e marcado com um asterisco (\*) na coluna Descrição da tabela a seguir.

Converta os tipos de dados das colunas na documentação OLE DB para tipos de dados do ADO, consultando a coluna Descrição do tópico ADO [DataTypeEnum](datatypeenum.md). Por exemplo, um tipo de dados OLE DB do **DBTYPE\_WSTR** é equivalente a um tipo de dados de ADO do **adWChar**.

O ADO gera resultados como esquema para as constantes **adSchemaDBInfoKeywords** e **adSchemaDBInfoLiterals**. ADO cria um **Recordset**e, em seguida, preenche cada linha com os valores retornados respectivamente pelos métodos **IDBInfo::GetKeywords** e **IDBInfo::GetLiteralInfo** . Informações adicionais sobre esses métodos podem ser encontradas na seção da *referência do programador do OLE DB do*IDBInfo.

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
<td><p>0</p></td>
<td><p>Retorna as asserções definidas no catálogo, pertencentes a um usuário específico.
 (Conjunto de linhas ASSERTIONS)</p></td>
<td><p>CONSTRAINT_CATALOG<br />
CONSTRAINT_SCHEMA<br />
CONSTRAINT_NAME</p></td>
</tr>
<tr class="even">
<td><p><strong>adSchemaCatalogs</strong></p></td>
<td><p>1</p></td>
<td><p>Retorna os atributos físicos associados aos catálogos acessíveis do DBMS.
 (Conjunto de linhas CATALOGS)</p></td>
<td><p>CATALOG_NAME</p></td>
</tr>
<tr class="odd">
<td><p><strong>adSchemaCharacterSets</strong></p></td>
<td><p>2</p></td>
<td><p>Retorna os conjuntos de caracteres definidos no catálogo que estão acessíveis para um determinado usuário.
 (Conjunto de linhas CHARACTER_SETS)</p></td>
<td><p>CHARACTER_SET_CATALOG<br />
CHARACTER_SET_SCHEMA<br />
CHARACTER_SET_NAME</p></td>
</tr>
<tr class="even">
<td><p><strong>adSchemaCheckConstraints</strong></p></td>
<td><p>5</p></td>
<td><p>Retorna as restrições de verificação definidas no catálogo, pertencentes a um usuário específico.
 (Conjunto de linhas CHECK_CONSTRAINTS)</p></td>
<td><p>CONSTRAINT_CATALOG<br />
CONSTRAINT_SCHEMA<br />
CONSTRAINT_NAME</p></td>
</tr>
<tr class="odd">
<td><p><strong>adSchemaCollations</strong></p></td>
<td><p>3</p></td>
<td><p>Retorna as coleções de caracteres definidas no catálogo que estão acessíveis para um determinado usuário.
 (Conjunto de linhas COLLATIONS)</p></td>
<td><p>COLLATION_CATALOG<br />
COLLATION_SCHEMA<br />
COLLATION_NAME</p></td>
</tr>
<tr class="even">
<td><p><strong>adSchemaColumnPrivileges</strong></p></td>
<td><p>13</p></td>
<td><p>Retorna, nas colunas das tabelas definidas no catálogo, os privilégios que estão disponíveis para um determinado usuário ou foram concedidos a ele.
 (Conjunto de linhas COLUMN_PRIVILEGES)</p></td>
<td><p>TABLE_CATALOG<br />
TABLE_SCHEMA<br />
TABLE_NAME<br />
NOME DA COLUNA<br />
CONCEDEROU<br />
RECEBEDOR DA PERMISSÃO</p></td>
</tr>
<tr class="odd">
<td><p><strong>adSchemaColumns</strong></p></td>
<td><p>4</p></td>
<td><p>Retorna as colunas das tabelas (inclusive as exibições) definidas no catálogo que estão acessíveis para um determinado usuário.
 (Conjunto de linhas COLUMNS)</p></td>
<td><p>TABLE_CATALOG<br />
TABLE_SCHEMA<br />
TABLE_NAME<br />
NOME DA COLUNA</p></td>
</tr>
<tr class="even">
<td><p><strong>adSchemaColumnsDomainUsage</strong></p></td>
<td><p>11</p></td>
<td><p>Retorna as colunas definidas no catálogo que são dependentes de um domínio definido no catálogo e pertencem a um determinado usuário.
 (Conjunto de linhas COLUMN_DOMAIN_USAGE)</p></td>
<td><p>DOMAIN_CATALOG<br />
DOMAIN_SCHEMA<br />
NOME_DO_DOMÍNIO<br />
NOME DA COLUNA</p></td>
</tr>
<tr class="odd">
<td><p><strong>adSchemaConstraintColumnUsage</strong></p></td>
<td><p>6</p></td>
<td><p>Retorna as colunas usadas por restrições de referência, restrições exclusivas, restrições de verificação e asserções, definidas no catálogo e pertencentes a um usuário específico.
 (Conjunto de linhas CONSTRAINT_COLUMN_USAGE)</p></td>
<td><p>TABLE_CATALOG<br />
TABLE_SCHEMA<br />
TABLE_NAME<br />
NOME DA COLUNA</p></td>
</tr>
<tr class="even">
<td><p><strong>adSchemaConstraintTableUsage</strong></p></td>
<td><p>7</p></td>
<td><p>Retorna as tabelas usadas por restrições de referência, restrições exclusivas, restrições de verificação e asserções, definidas no catálogo e pertencentes a um usuário específico.
 (Conjunto de linhas CONSTRAINT_TABLE_USAGE)</p></td>
<td><p>TABLE_CATALOG<br />
TABLE_SCHEMA<br />
TABLE_NAME</p></td>
</tr>
<tr class="odd">
<td><p><strong>adSchemaCubes</strong></p></td>
<td><p>32</p></td>
<td><p>Retorna informações sobre os cubos disponíveis em um esquema (ou o catálogo se o provedor não oferecer suporte a esquemas).
 (Conjunto de linhas CUBES*)</p></td>
<td><p>CATALOG_NAME<br />
SCHEMA_NAME<br />
CUBE_NAME</p></td>
</tr>
<tr class="even">
<td><p><strong>adSchemaDBInfoKeywords</strong></p></td>
<td><p>30</p></td>
<td><p>Retorna uma lista de palavras-chave específicas do provedor.
 (IDBInfo::GetKeywords *)</p></td>
<td><p>&lt;Nenhum&gt;</p></td>
</tr>
<tr class="odd">
<td><p><strong>adSchemaDBInfoLiterals</strong></p></td>
<td><p>31</p></td>
<td><p>Retorna uma lista de literais específicos do provedor utilizados em comandos de texto.
 (IDBInfo::GetLiteralInfo *)</p></td>
<td><p>&lt;Nenhum&gt;</p></td>
</tr>
<tr class="even">
<td><p><strong>adSchemaDimensions</strong></p></td>
<td><p>33</p></td>
<td><p>Retorna informações sobre as dimensões em um cubo específico. Ele tem uma linha para cada dimensão. (Conjunto de linhas DIMENSIONS*)</p></td>
<td><p>CATALOG_NAME<br />
SCHEMA_NAME<br />
CUBE_NAME<br />
DIMENSION_NAME<br />
DIMENSION_UNIQUE_NAME</p></td>
</tr>
<tr class="odd">
<td><p><strong>adSchemaForeignKeys</strong></p></td>
<td><p>27</p></td>
<td><p>Retorna as colunas de chave estrangeira definidas no catálogo por um determinado usuário.
 (Conjunto de linhas FOREIGN_KEYS)</p></td>
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
<td><p>Retorna informações sobre as hierarquias disponíveis em uma dimensão.
 (Conjunto de linhas HIERARCHIES*)</p></td>
<td><p>CATALOG_NAME<br />
SCHEMA_NAME<br />
CUBE_NAME<br />
DIMENSION_UNIQUE_NAME<br />
HIERARCHY_NAME<br />
HIERARCHY_UNIQUE_NAME</p></td>
</tr>
<tr class="odd">
<td><p><strong>adSchemaIndexes</strong></p></td>
<td><p>12</p></td>
<td><p>Retorna os índices definidos no catálogo, pertencentes a um usuário específico.
 (Conjunto de linhas INDEXES)</p></td>
<td><p>TABLE_CATALOG<br />
TABLE_SCHEMA<br />
INDEX_NAME<br />
TIPO<br />
TABLE_NAME</p></td>
</tr>
<tr class="even">
<td><p><strong>adSchemaKeyColumnUsage</strong></p></td>
<td><p>8</p></td>
<td><p>Retorna as colunas definidas no catálogo, restritas a chaves por um usuário específico.
 (Conjunto de linhas KEY_COLUMN_USAGE)</p></td>
<td><p>CONSTRAINT_CATALOG<br />
CONSTRAINT_SCHEMA<br />
CONSTRAINT_NAME<br />
TABLE_CATALOG<br />
TABLE_SCHEMA<br />
TABLE_NAME<br />
NOME DA COLUNA</p></td>
</tr>
<tr class="odd">
<td><p><strong>adSchemaLevels</strong></p></td>
<td><p>35</p></td>
<td><p>Retorna informações sobre os níveis disponíveis em uma dimensão.
 (Conjunto de linhas LEVELS*)</p></td>
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
<td><p>Retorna informações sobre as medidas disponíveis.
 (Conjunto de linhas MEASURES*)</p></td>
<td><p>CATALOG_NAME<br />
SCHEMA_NAME<br />
CUBE_NAME<br />
MEASURE_NAME<br />
MEASURE_UNIQUE_NAME</p></td>
</tr>
<tr class="odd">
<td><p><strong>adSchemaMembers</strong></p></td>
<td><p>38</p></td>
<td><p>Retorna informações sobre os membros disponíveis.
 (Conjunto de linhas MEMBERS*)</p></td>
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
O operador de árvore (para obter mais informações, consulte o OLE DB para a documentação do OLAP).</p></td>
</tr>
<tr class="even">
<td><p><strong>adSchemaPrimaryKeys</strong></p></td>
<td><p>28</p></td>
<td><p>Retorna as colunas de chave principal definidas no catálogo por um determinado usuário.
 (Conjunto de linhas PRIMARY_KEYS)</p></td>
<td><p>PK_TABLE_CATALOG<br />
PK_TABLE_SCHEMA<br />
PK_TABLE_NAME</p></td>
</tr>
<tr class="odd">
<td><p><strong>adSchemaProcedureColumns</strong></p></td>
<td><p>29</p></td>
<td><p>Retorna informações sobre as colunas de conjuntos de linhas por procedimentos.
 (Conjunto de linhas PROCEDURE_COLUMNS)</p></td>
<td><p>PROCEDURE_CATALOG<br />
PROCEDURE_SCHEMA<br />
PROCEDURE_NAME<br />
NOME DA COLUNA</p></td>
</tr>
<tr class="even">
<td><p><strong>adSchemaProcedureParameters</strong></p></td>
<td><p>26</p></td>
<td><p>Retorna informações sobre parâmetros e códigos de retorno de procedimentos.
 (Conjunto de linhas PROCEDURE_PARAMETERS)</p></td>
<td><p>PROCEDURE_CATALOG<br />
PROCEDURE_SCHEMA<br />
PROCEDURE_NAME<br />
NOME_DO</p></td>
</tr>
<tr class="odd">
<td><p><strong>adSchemaProcedures</strong></p></td>
<td><p>16</p></td>
<td><p>Retorna os procedimentos definidos no catálogo, pertencentes a um usuário específico.
 (Conjunto de linhas PROCEDURES)</p></td>
<td><p>PROCEDURE_CATALOG<br />
PROCEDURE_SCHEMA<br />
PROCEDURE_NAME<br />
PROCEDURE_TYPE</p></td>
</tr>
<tr class="even">
<td><p><strong>adSchemaProperties</strong></p></td>
<td><p>37</p></td>
<td><p>Retorna informações sobre as propriedades disponíveis para cada nível de dimensão.
 (Conjunto de linhas PROPERTIES*)</p></td>
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
<td><p>&lt;Provedor específico&gt;</p></td>
</tr>
<tr class="even">
<td><p><strong>adSchemaProviderTypes</strong></p></td>
<td><p>22</p></td>
<td><p>Retorna os tipos de dados (base) aceitos pelo provedor de dados.
 (Conjunto de linhas PROVIDER_TYPES)</p></td>
<td><p>DATA_TYPE<br />
BEST_MATCH</p></td>
</tr>
<tr class="odd">
<td><p><strong>AdSchemaReferentialConstraints</strong></p></td>
<td><p>9</p></td>
<td><p>Retorna as restrições de referência definidas no catálogo, pertencentes a um usuário específico.
 (Conjunto de linhas REFERENTIAL_CONSTRAINTS)</p></td>
<td><p>CONSTRAINT_CATALOG<br />
CONSTRAINT_SCHEMA<br />
CONSTRAINT_NAME</p></td>
</tr>
<tr class="even">
<td><p><strong>adSchemaSchemata</strong></p></td>
<td><p>17</p></td>
<td><p>Retorna os esquemas (objetos de banco de dados) pertencentes a um usuário específico.
 (Conjunto de linhas SCHEMATA)</p></td>
<td><p>CATALOG_NAME<br />
SCHEMA_NAME<br />
SCHEMA_OWNER</p></td>
</tr>
<tr class="odd">
<td><p><strong>adSchemaSQLLanguages</strong></p></td>
<td><p>18</p></td>
<td><p>Retorna os níveis, as opções e os dialetos de conformidade aceitos pelos dados de processamento de implementação do SQL definidos no catálogo.
 (Conjunto de linhas SQL_LANGUAGES)</p></td>
<td><p>&lt;Nenhum&gt;</p></td>
</tr>
<tr class="even">
<td><p><strong>adSchemaStatistics</strong></p></td>
<td><p>19</p></td>
<td><p>Retorna as estatísticas definidas no catálogo, pertencentes a um usuário específico.
 (Conjunto de linhas STATISTICS)</p></td>
<td><p>TABLE_CATALOG<br />
TABLE_SCHEMA<br />
TABLE_NAME</p></td>
</tr>
<tr class="odd">
<td><p><strong>adSchemaTableConstraints</strong></p></td>
<td><p>10</p></td>
<td><p>Retorna as restrições de tabela definidas no catálogo, pertencentes a um usuário específico.
 (Conjunto de linha TABLE_CONSTRAINTS)</p></td>
<td><p>CONSTRAINT_CATALOG<br />
CONSTRAINT_SCHEMA<br />
CONSTRAINT_NAME<br />
TABLE_CATALOG<br />
TABLE_SCHEMA<br />
TABLE_NAME<br />
TIPO_RESTRIÇÃO</p></td>
</tr>
<tr class="even">
<td><p><strong>adSchemaTablePrivileges</strong></p></td>
<td><p>14</p></td>
<td><p>Retorna, nas tabelas definidas no catálogo, os privilégios que estão disponíveis para um determinado usuário ou foram concedidos a ele.
 (Conjunto de linhas TABLE_PRIVILEGES)</p></td>
<td><p>TABLE_CATALOG<br />
TABLE_SCHEMA<br />
TABLE_NAME<br />
CONCEDEROU<br />
RECEBEDOR DA PERMISSÃO</p></td>
</tr>
<tr class="odd">
<td><p><strong>adSchemaTables</strong></p></td>
<td><p>20</p></td>
<td><p>Retorna as tabelas (inclusive as exibições) definidas no catálogo que estão acessíveis para um determinado usuário.
 (Conjunto de linhas TABLES)</p></td>
<td><p>TABLE_CATALOG<br />
TABLE_SCHEMA<br />
TABLE_NAME<br />
TABLE_TYPE</p></td>
</tr>
<tr class="even">
<td><p><strong>adSchemaTranslations</strong></p></td>
<td><p>21</p></td>
<td><p>Retorna as conversões de caracteres definidas no catálogo que estão acessíveis para um usuário específico.
 (Conjunto de linhas TRANSLATIONS)</p></td>
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
<td><p>Retorna, nos objetos definidos no catálogo, os privilégios USAGE que estão disponíveis para um determinado usuário ou foram concedidos a ele.
 (Conjunto de linhas USAGE_PRIVILEGES)</p></td>
<td><p>OBJECT_CATALOG<br />
OBJECT_SCHEMA<br />
OBJECT_NAME<br />
TIPO_DO_OBJETO<br />
CONCEDEROU<br />
RECEBEDOR DA PERMISSÃO</p></td>
</tr>
<tr class="odd">
<td><p><strong>adSchemaViewColumnUsage</strong></p></td>
<td><p>24</p></td>
<td><p>Retorna as colunas das quais as tabelas exibidas, definidas no catálogo e pertencentes a um usuário específico, são dependentes.
 (Conjunto de linhas VIEW_COLUMN_USAGE)</p></td>
<td><p>VIEW_CATALOG<br />
VIEW_SCHEMA<br />
VIEW_NAME</p></td>
</tr>
<tr class="even">
<td><p><strong>adSchemaViews</strong></p></td>
<td><p>23</p></td>
<td><p>Retorna as exibições definidas no catálogo que estão acessíveis para um determinado usuário.
 (Conjunto de linhas VIEWS)</p></td>
<td><p>TABLE_CATALOG<br />
TABLE_SCHEMA<br />
TABLE_NAME</p></td>
</tr>
<tr class="odd">
<td><p><strong>adSchemaViewTableUsage</strong></p></td>
<td><p>25</p></td>
<td><p>Retorna as tabelas das quais as tabelas exibidas, definidas no catálogo e pertencentes a um usuário específico, são dependentes.
 (Conjunto de linhas VIEW_TABLE_USAGE)</p></td>
<td><p>VIEW_CATALOG<br />
VIEW_SCHEMA<br />
VIEW_NAME</p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a>Equivalente ADO/WFC

Pacote: **com.ms.wfc.data**

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Constante</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>AdoEnums.Schema.ASSERTS</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.Schema.CATALOGS</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.Schema.CHARACTERSETS</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.Schema.CHECKCONSTRAINTS</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.Schema.COLLATIONS</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.Schema.COLUMNPRIVILEGES</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.Schema.COLUMNS</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.Schema.COLUMNSDOMAINUSAGE</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.Schema.CONSTRAINTCOLUMNUSAGE</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.Schema.CONSTRAINTTABLEUSAGE</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.Schema.CUBES</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.Schema.DBINFOKEYWORDS</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.Schema.DBINFOLITERALS</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.Schema.DIMENSIONS</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.Schema.FOREIGNKEYS</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.Schema.HIERARCHIES</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.Schema.INDEXES</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.Schema.KEYCOLUMNUSAGE</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.Schema.LEVELS</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.Schema.MEASURES</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.Schema.MEMBERS</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.Schema.PRIMARYKEYS</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.Schema.PROCEDURECOLUMNS</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.Schema.PROCEDUREPARAMETERS</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.Schema.PROCEDURES</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.Schema.PROPERTIES</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.Schema.PROVIDERSPECIFIC</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.Schema.PROVIDERTYPES</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.Schema.REFERENTIALCONTRAINTS</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.Schema.SCHEMATA</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.Schema.SQLLANGUAGES</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.Schema.STATISTICS</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.Schema.TABLECONSTRAINTS</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.Schema.TABLEPRIVILEGES</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.Schema.TABLES</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.Schema.TRANSLATIONS</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.Schema.TRUSTEES</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.Schema.USAGEPRIVILEGES</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.Schema.VIEWCOLUMNUSAGE</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.Schema.VIEWS</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.Schema.VIEWTABLEUSAGE</p></td>
</tr>
</tbody>
</table>

