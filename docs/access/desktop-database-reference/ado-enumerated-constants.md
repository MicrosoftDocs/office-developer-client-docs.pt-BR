---
title: Constantes enumeradas do ADO
TOCTitle: ADO Enumerated Constants
ms:assetid: 7c983acd-8b38-dc3c-6704-46e649ebb7d6
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249522(v=office.15)
ms:contentKeyID: 48545841
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 3e9944138dcdca49f33ca293a9bdf41d88d86e9e
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25882305"
---
# <a name="ado-enumerated-constants"></a>Constantes enumeradas do ADO


**Aplica-se a**: Access 2013, o Office 2013

Para ajudar na depuração, as enumerações do ADO listam um valor para cada constante. Contudo, esse valor é temporário e pode ser alterado de uma versão do ADO para outra. Seu código deve depender somente do nome, não do valor real, de cada constante enumerada.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><a href="adcprop-asyncthreadpriority-enum.md">ADCPROP_ASYNCTHREADPRIORITY_ENUM</a></p></td>
<td><p>Para um objeto do <strong>Recordset</strong> RDS, especifica a prioridade de execução do encadeamento assíncrono que recupera os dados.</p></td>
</tr>
<tr class="even">
<td><p><a href="adcprop-autorecalc-enum.md">ADCPROP_AUTORECALC_ENUM</a></p></td>
<td><p>Especifica quando o provedor <strong>MSDataShape</strong> recalcula colunas calculadas e agregadas em um <strong>Recordset</strong>de hierárquico.</p></td>
</tr>
<tr class="odd">
<td><p><a href="adcprop-updatecriteria-enum.md">ADCPROP_UPDATECRITERIA_ENUM</a></p></td>
<td><p>Especifica quais campos podem ser usados para detectar conflitos durante uma atualização otimista de uma linha da fonte de dados com um objeto <strong>Recordset</strong>.</p></td>
</tr>
<tr class="even">
<td><p><a href="adcprop-updateresync-enum.md">ADCPROP_UPDATERESYNC_ENUM</a></p></td>
<td><p>Especifica se o método <strong>UpdateBatch</strong> é seguido por uma operação do método <strong>Resync</strong> implícita e, se for, especifica o escopo dessa operação.</p></td>
</tr>
<tr class="odd">
<td><p><a href="affectenum.md">AffectEnum</a></p></td>
<td><p>Especifica quais registros foram afetados por uma operação.</p></td>
</tr>
<tr class="even">
<td><p><a href="bookmarkenum.md">BookmarkEnum</a></p></td>
<td><p>Especifica um indicador mostrando onde a operação deveria começar.</p></td>
</tr>
<tr class="odd">
<td><p><a href="commandtypeenum.md">CommandTypeEnum</a></p></td>
<td><p>Especifica como um argumento de comando deve ser interpretado.</p></td>
</tr>
<tr class="even">
<td><p><a href="compareenum.md">CompareEnum</a></p></td>
<td><p>Especifica a posição relativa de dois registros representados por seus indicadores.</p></td>
</tr>
<tr class="odd">
<td><p><a href="connectmodeenum.md">ConnectModeEnum</a></p></td>
<td><p>Especifica as permissões disponíveis para modificar os dados em uma <strong>Connection</strong>, abrir um <strong>Record</strong> ou especificar os valores para a propriedade <strong>Mode</strong> dos objetos <strong>Record</strong> e <strong>Stream</strong>.</p></td>
</tr>
<tr class="even">
<td><p><a href="connectoptionenum.md">ConnectOptionEnum</a></p></td>
<td><p>Especifica se o método <strong>Open</strong> de um objeto <strong>Connection</strong> deve ser retornado após a conexão (de maneira síncrona) ou antes da (de maneira assíncrona) conexão ser estabelecida.</p></td>
</tr>
<tr class="odd">
<td><p><a href="connectpromptenum.md">ConnectPromptEnum</a></p></td>
<td><p>Especifica se uma caixa de diálogo deve ser exibida para avisar sobre parâmetros ausentes ao abrir uma conexão para uma fonte de dados ODBC.</p></td>
</tr>
<tr class="even">
<td><p><a href="copyrecordoptionsenum.md">CopyRecordOptionsEnum</a></p></td>
<td><p>Especifica o comportamento do método <strong>CopyRecord</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><a href="cursorlocationenum.md">CursorLocationEnum</a></p></td>
<td><p>Especifica a localização do mecanismo do cursor.</p></td>
</tr>
<tr class="even">
<td><p><a href="cursoroptionenum.md">CursorOptionEnum</a></p></td>
<td><p>Especifica a funcionalidade para a qual o método <strong>Supports</strong> deve ser testado.</p></td>
</tr>
<tr class="odd">
<td><p><a href="cursortypeenum.md">CursorTypeEnum</a></p></td>
<td><p>Especifica o tipo de cursor usado em um objeto <strong>Recordset</strong>.</p></td>
</tr>
<tr class="even">
<td><p><a href="datatypeenum.md">DataTypeEnum</a></p></td>
<td><p>Especifica o tipo de dados de <strong>Field</strong>, <strong>Parameter</strong> ou <strong>Property</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><a href="editmodeenum.md">EditModeEnum</a></p></td>
<td><p>Especifica o status de edição de um registro.</p></td>
</tr>
<tr class="even">
<td><p><a href="errorvalueenum.md">ErrorValueEnum</a></p></td>
<td><p>Especifica o tipo de erro de tempo de execução do ADO.</p></td>
</tr>
<tr class="odd">
<td><p><a href="eventreasonenum.md">EventReasonEnum</a></p></td>
<td><p>Especifica a razão que fez com que ocorresse um evento.</p></td>
</tr>
<tr class="even">
<td><p><a href="eventstatusenum.md">EventStatusEnum</a></p></td>
<td><p>Especifica o status atual da execução de um evento.</p></td>
</tr>
<tr class="odd">
<td><p><a href="executeoptionenum.md">ExecuteOptionEnum</a></p></td>
<td><p>Especifica como um provedor deve executar um comando.</p></td>
</tr>
<tr class="even">
<td><p><a href="fieldenum.md">FieldEnum</a></p></td>
<td><p>Especifica os campos especiais mencionados em uma coleção de <strong>Campos</strong> do objeto <strong>Record</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><a href="fieldattributeenum.md">FieldAttributeEnum</a></p></td>
<td><p>Especifica um ou mais atributos de um objeto <strong>Field</strong>.</p></td>
</tr>
<tr class="even">
<td><p><a href="fieldstatusenum.md">FieldStatusEnum</a></p></td>
<td><p>Especifica o status de um objeto <strong>Field</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><a href="filtergroupenum.md">FilterGroupEnum</a></p></td>
<td><p>Especifica o grupo de registros a serem filtrados a partir de um <strong>Recordset</strong>.</p></td>
</tr>
<tr class="even">
<td><p><a href="getrowsoptionenum.md">GetRowsOptionEnum</a></p></td>
<td><p>Especifica quantos registros devem ser recuperados de um <strong>Recorset</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><a href="isolationlevelenum.md">IsolationLevelEnum</a></p></td>
<td><p>Especifica o nível de isolamento da transação para um objeto <strong>Connection</strong>.</p></td>
</tr>
<tr class="even">
<td><p><a href="lineseparatorsenum.md">LineSeparatorsEnum</a></p></td>
<td><p>Especifica o caractere usado como um separador de linha nos objetos <strong>Stream</strong> de texto.</p></td>
</tr>
<tr class="odd">
<td><p><a href="locktypeenum.md">LockTypeEnum</a></p></td>
<td><p>Especifica o tipo de bloqueio colocado nos registros durante a edição.</p></td>
</tr>
<tr class="even">
<td><p><a href="marshaloptionsenum.md">MarshalOptionsEnum</a></p></td>
<td><p>Especifica quais registros devem ser retornados ao servidor.</p></td>
</tr>
<tr class="odd">
<td><p><a href="moverecordoptionsenum.md">MoveRecordOptionsEnum</a></p></td>
<td><p>Especifica o comportamento do objeto <strong>Record</strong> do método <strong>MoveRecord</strong>.</p></td>
</tr>
<tr class="even">
<td><p><a href="objectstateenum.md">ObjectStateEnum</a></p></td>
<td><p>Especifica se um objeto está aberto ou fechado, conectando a uma fonte de dados, executando um comando ou buscando dados.</p></td>
</tr>
<tr class="odd">
<td><p><a href="parameterattributesenum.md">ParameterAttributesEnum</a></p></td>
<td><p>Especifica os atributos de um objeto <strong>Parameter</strong>.</p></td>
</tr>
<tr class="even">
<td><p><a href="parameterdirectionenum.md">ParameterDirectionEnum</a></p></td>
<td><p>Especifica se <strong>Parameter</strong> representa um parâmetro de entrada, de saída, ou ambos, ou se é o valor de retorno de um procedimento armazenado.</p></td>
</tr>
<tr class="odd">
<td><p><a href="persistformatenum.md">PersistFormatEnum</a></p></td>
<td><p>Especifica o formato no qual se deve salvar um <strong>Recorset</strong>.</p></td>
</tr>
<tr class="even">
<td><p><a href="positionenum.md">PositionEnum</a></p></td>
<td><p>Especifica a posição atual do ponteiro do registro em um <strong>Recordset</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><a href="propertyattributesenum.md">PropertyAttributesEnum</a></p></td>
<td><p>Especifica os atributos de um objeto <strong>Property</strong>.</p></td>
</tr>
<tr class="even">
<td><p><a href="recordcreateoptionsenum.md">RecordCreateOptionsEnum</a></p></td>
<td><p>Especifica o método <strong>Open</strong> do objeto <strong>Record</strong> se um <strong>Record</strong> existente estiver aberto ou se um novo <strong>Record</strong> for criado.</p></td>
</tr>
<tr class="odd">
<td><p><a href="recordopenoptionsenum.md">RecordOpenOptionsEnum</a></p></td>
<td><p>Especifica as opções para abrir um objeto <strong>Record</strong>. Esses valores podem ser combinados utilizando um operador OR.</p></td>
</tr>
<tr class="even">
<td><p><a href="recordstatusenum.md">RecordStatusEnum</a></p></td>
<td><p>Especifica o status de um registro com relação a atualizações de batch e outras operações em massa.</p></td>
</tr>
<tr class="odd">
<td><p><a href="recordtypeenum.md">RecordTypeEnum</a></p></td>
<td><p>Especifica o tipo de objeto <strong>Record</strong>.</p></td>
</tr>
<tr class="even">
<td><p><a href="resyncenum.md">ResyncEnum</a></p></td>
<td><p>Especifica se os valores subjacentes são sobregravados por uma chamada para <strong>Resync</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><a href="saveoptionsenum.md">SaveOptionsEnum</a></p></td>
<td><p>Especifica se um arquivo deveria ser criado ou sobregravado ao salvar a partir de um objeto <strong>Stream</strong>. Os valores podem ser combinados com um operador AND.</p></td>
</tr>
<tr class="even">
<td><p><a href="schemaenum.md">SchemaEnum</a></p></td>
<td><p>Especifica o tipo de esquema <strong>Recordset</strong> que o método <strong>OpenSchema</strong> recupera. Especifica a direção de uma pesquisa de registro dentro de um <strong>Recordset</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><a href="searchdirectionenum.md">SearchDirectionEnum</a></p></td>
<td><p>Especifica a direção de uma pesquisa de registro dentro de um <strong>Recordset</strong>. Especifica o tipo de <strong>Seek</strong> a ser executado.</p></td>
</tr>
<tr class="even">
<td><p><a href="seekenum.md">SeekEnum</a></p></td>
<td><p>Especifica o tipo de <strong>Seek</strong> a ser executado. Especifica as opções para a abertura de um objeto <strong>Stream</strong>. Os valores podem ser combinados a um operador AND.</p></td>
</tr>
<tr class="odd">
<td><p><a href="streamopenoptionsenum.md">StreamOpenOptionsEnum</a></p></td>
<td><p>Especifica as opções para abrir um objeto <strong>Stream</strong>. Os valores podem ser combinados a um operador AND. Especifica se o fluxo inteiro ou a próxima linha deve ser lida a partir do objeto <strong>Stream</strong>.</p></td>
</tr>
<tr class="even">
<td><p><a href="streamreadenum.md">StreamReadEnum</a></p></td>
<td><p>Especifica se o fluxo inteiro ou a próxima linha deve ser lida a partir do objeto <strong>Stream</strong>. Especifica os tipos de dados armazenados em um objeto <strong>Stream</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><a href="streamtypeenum.md">StreamTypeEnum</a></p></td>
<td><p>Especifica os tipos de dados armazenados em um objeto <strong>Stream</strong>. Especifica se um separador de linha está anexado à sequência de caracteres escrita no objeto <strong>Stream</strong>.</p></td>
</tr>
<tr class="even">
<td><p><a href="streamwriteenum.md">StreamWriteEnum</a></p></td>
<td><p>Especifica se um separador de linha está anexado à sequência de caracteres escrita no objeto <strong>Stream</strong>. Especifica o formato ao recuperar um <strong>Recordset</strong> como uma sequência de caracteres.</p></td>
</tr>
<tr class="odd">
<td><p><a href="stringformatenum.md">StringFormatEnum</a></p></td>
<td><p>Especifica o formato ao recuperar um <strong>Recordset</strong> como uma sequência de caracteres. Especifica os atributos da transação de um objeto <strong>Connection</strong>.</p></td>
</tr>
<tr class="even">
<td><p><a href="xactattributeenum.md">XactAttributeEnum</a></p></td>
<td><p>Especifica os atributos de transação de um objeto <strong>Connection</strong>.</p></td>
</tr>
</tbody>
</table>

