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
# <a name="ado-enumerated-constants"></a><span data-ttu-id="61909-102">Constantes enumeradas do ADO</span><span class="sxs-lookup"><span data-stu-id="61909-102">ADO Enumerated Constants</span></span>


<span data-ttu-id="61909-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="61909-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="61909-p101">Para ajudar na depuração, as enumerações do ADO listam um valor para cada constante. Contudo, esse valor é temporário e pode ser alterado de uma versão do ADO para outra. Seu código deve depender somente do nome, não do valor real, de cada constante enumerada.</span><span class="sxs-lookup"><span data-stu-id="61909-p101">To assist in debugging, the ADO enumerations list a value for each constant. However, this value is purely advisory, and may change from one release of ADO to another. Your code should only depend on the name, not the actual value, of each enumerated constant.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="61909-107"><a href="adcprop-asyncthreadpriority-enum.md">ADCPROP_ASYNCTHREADPRIORITY_ENUM</a></span><span class="sxs-lookup"><span data-stu-id="61909-107"><a href="adcprop-asyncthreadpriority-enum.md">ADCPROP_ASYNCTHREADPRIORITY_ENUM</a></span></span></p></td>
<td><p><span data-ttu-id="61909-108">Para um objeto do <strong>Recordset</strong> RDS, especifica a prioridade de execução do encadeamento assíncrono que recupera os dados.</span><span class="sxs-lookup"><span data-stu-id="61909-108">For an RDS <strong>Recordset</strong> object, specifies the execution priority of the asynchronous thread that retrieves data.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="61909-109"><a href="adcprop-autorecalc-enum.md">ADCPROP_AUTORECALC_ENUM</a></span><span class="sxs-lookup"><span data-stu-id="61909-109"><a href="adcprop-autorecalc-enum.md">ADCPROP_AUTORECALC_ENUM</a></span></span></p></td>
<td><p><span data-ttu-id="61909-110">Especifica quando o provedor <strong>MSDataShape</strong> recalcula colunas calculadas e agregadas em um <strong>Recordset</strong>de hierárquico.</span><span class="sxs-lookup"><span data-stu-id="61909-110">Specifies when the <strong>MSDataShape</strong> provider re-calculates aggregate and calculated columns in a hierarchical <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="61909-111"><a href="adcprop-updatecriteria-enum.md">ADCPROP_UPDATECRITERIA_ENUM</a></span><span class="sxs-lookup"><span data-stu-id="61909-111"><a href="adcprop-updatecriteria-enum.md">ADCPROP_UPDATECRITERIA_ENUM</a></span></span></p></td>
<td><p><span data-ttu-id="61909-112">Especifica quais campos podem ser usados para detectar conflitos durante uma atualização otimista de uma linha da fonte de dados com um objeto <strong>Recordset</strong>.</span><span class="sxs-lookup"><span data-stu-id="61909-112">Specifies which fields can be used to detect conflicts during an optimistic update of a row of the data source with a <strong>Recordset</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="61909-113"><a href="adcprop-updateresync-enum.md">ADCPROP_UPDATERESYNC_ENUM</a></span><span class="sxs-lookup"><span data-stu-id="61909-113"><a href="adcprop-updateresync-enum.md">ADCPROP_UPDATERESYNC_ENUM</a></span></span></p></td>
<td><p><span data-ttu-id="61909-114">Especifica se o método <strong>UpdateBatch</strong> é seguido por uma operação do método <strong>Resync</strong> implícita e, se for, especifica o escopo dessa operação.</span><span class="sxs-lookup"><span data-stu-id="61909-114">Specifies whether the <strong>UpdateBatch</strong> method is followed by an implicit <strong>Resync</strong> method operation and if so, the scope of that operation.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="61909-115"><a href="affectenum.md">AffectEnum</a></span><span class="sxs-lookup"><span data-stu-id="61909-115"><a href="affectenum.md">AffectEnum</a></span></span></p></td>
<td><p><span data-ttu-id="61909-116">Especifica quais registros foram afetados por uma operação.</span><span class="sxs-lookup"><span data-stu-id="61909-116">Specifies which records are affected by an operation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="61909-117"><a href="bookmarkenum.md">BookmarkEnum</a></span><span class="sxs-lookup"><span data-stu-id="61909-117"><a href="bookmarkenum.md">BookmarkEnum</a></span></span></p></td>
<td><p><span data-ttu-id="61909-118">Especifica um indicador mostrando onde a operação deveria começar.</span><span class="sxs-lookup"><span data-stu-id="61909-118">Specifies a bookmark indicating where the operation should begin.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="61909-119"><a href="commandtypeenum.md">CommandTypeEnum</a></span><span class="sxs-lookup"><span data-stu-id="61909-119"><a href="commandtypeenum.md">CommandTypeEnum</a></span></span></p></td>
<td><p><span data-ttu-id="61909-120">Especifica como um argumento de comando deve ser interpretado.</span><span class="sxs-lookup"><span data-stu-id="61909-120">Specifies how a command argument should be interpreted.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="61909-121"><a href="compareenum.md">CompareEnum</a></span><span class="sxs-lookup"><span data-stu-id="61909-121"><a href="compareenum.md">CompareEnum</a></span></span></p></td>
<td><p><span data-ttu-id="61909-122">Especifica a posição relativa de dois registros representados por seus indicadores.</span><span class="sxs-lookup"><span data-stu-id="61909-122">Specifies the relative position of two records represented by their bookmarks.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="61909-123"><a href="connectmodeenum.md">ConnectModeEnum</a></span><span class="sxs-lookup"><span data-stu-id="61909-123"><a href="connectmodeenum.md">ConnectModeEnum</a></span></span></p></td>
<td><p><span data-ttu-id="61909-124">Especifica as permissões disponíveis para modificar os dados em uma <strong>Connection</strong>, abrir um <strong>Record</strong> ou especificar os valores para a propriedade <strong>Mode</strong> dos objetos <strong>Record</strong> e <strong>Stream</strong>.</span><span class="sxs-lookup"><span data-stu-id="61909-124">Specifies the available permissions for modifying data in a <strong>Connection</strong>, opening a <strong>Record</strong>, or specifying values for the <strong>Mode</strong> property of the <strong>Record</strong> and <strong>Stream</strong> objects.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="61909-125"><a href="connectoptionenum.md">ConnectOptionEnum</a></span><span class="sxs-lookup"><span data-stu-id="61909-125"><a href="connectoptionenum.md">ConnectOptionEnum</a></span></span></p></td>
<td><p><span data-ttu-id="61909-126">Especifica se o método <strong>Open</strong> de um objeto <strong>Connection</strong> deve ser retornado após a conexão (de maneira síncrona) ou antes da (de maneira assíncrona) conexão ser estabelecida.</span><span class="sxs-lookup"><span data-stu-id="61909-126">Specifies whether the <strong>Open</strong> method of a <strong>Connection</strong> object should return after (synchronously) or before (asynchronously) the connection is established.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="61909-127"><a href="connectpromptenum.md">ConnectPromptEnum</a></span><span class="sxs-lookup"><span data-stu-id="61909-127"><a href="connectpromptenum.md">ConnectPromptEnum</a></span></span></p></td>
<td><p><span data-ttu-id="61909-128">Especifica se uma caixa de diálogo deve ser exibida para avisar sobre parâmetros ausentes ao abrir uma conexão para uma fonte de dados ODBC.</span><span class="sxs-lookup"><span data-stu-id="61909-128">Specifies whether a dialog box should be displayed to prompt for missing parameters when opening a connection to an ODBC data source.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="61909-129"><a href="copyrecordoptionsenum.md">CopyRecordOptionsEnum</a></span><span class="sxs-lookup"><span data-stu-id="61909-129"><a href="copyrecordoptionsenum.md">CopyRecordOptionsEnum</a></span></span></p></td>
<td><p><span data-ttu-id="61909-130">Especifica o comportamento do método <strong>CopyRecord</strong>.</span><span class="sxs-lookup"><span data-stu-id="61909-130">Specifies the behavior of the <strong>CopyRecord</strong> method.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="61909-131"><a href="cursorlocationenum.md">CursorLocationEnum</a></span><span class="sxs-lookup"><span data-stu-id="61909-131"><a href="cursorlocationenum.md">CursorLocationEnum</a></span></span></p></td>
<td><p><span data-ttu-id="61909-132">Especifica a localização do mecanismo do cursor.</span><span class="sxs-lookup"><span data-stu-id="61909-132">Specifies the location of the cursor engine.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="61909-133"><a href="cursoroptionenum.md">CursorOptionEnum</a></span><span class="sxs-lookup"><span data-stu-id="61909-133"><a href="cursoroptionenum.md">CursorOptionEnum</a></span></span></p></td>
<td><p><span data-ttu-id="61909-134">Especifica a funcionalidade para a qual o método <strong>Supports</strong> deve ser testado.</span><span class="sxs-lookup"><span data-stu-id="61909-134">Specifies what functionality the <strong>Supports</strong> method should test for.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="61909-135"><a href="cursortypeenum.md">CursorTypeEnum</a></span><span class="sxs-lookup"><span data-stu-id="61909-135"><a href="cursortypeenum.md">CursorTypeEnum</a></span></span></p></td>
<td><p><span data-ttu-id="61909-136">Especifica o tipo de cursor usado em um objeto <strong>Recordset</strong>.</span><span class="sxs-lookup"><span data-stu-id="61909-136">Specifies the type of cursor used in a <strong>Recordset</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="61909-137"><a href="datatypeenum.md">DataTypeEnum</a></span><span class="sxs-lookup"><span data-stu-id="61909-137"><a href="datatypeenum.md">DataTypeEnum</a></span></span></p></td>
<td><p><span data-ttu-id="61909-138">Especifica o tipo de dados de <strong>Field</strong>, <strong>Parameter</strong> ou <strong>Property</strong>.</span><span class="sxs-lookup"><span data-stu-id="61909-138">Specifies the data type of a <strong>Field</strong>, <strong>Parameter</strong>, or <strong>Property</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="61909-139"><a href="editmodeenum.md">EditModeEnum</a></span><span class="sxs-lookup"><span data-stu-id="61909-139"><a href="editmodeenum.md">EditModeEnum</a></span></span></p></td>
<td><p><span data-ttu-id="61909-140">Especifica o status de edição de um registro.</span><span class="sxs-lookup"><span data-stu-id="61909-140">Specifies the editing status of a record.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="61909-141"><a href="errorvalueenum.md">ErrorValueEnum</a></span><span class="sxs-lookup"><span data-stu-id="61909-141"><a href="errorvalueenum.md">ErrorValueEnum</a></span></span></p></td>
<td><p><span data-ttu-id="61909-142">Especifica o tipo de erro de tempo de execução do ADO.</span><span class="sxs-lookup"><span data-stu-id="61909-142">Specifies the type of ADO run-time error.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="61909-143"><a href="eventreasonenum.md">EventReasonEnum</a></span><span class="sxs-lookup"><span data-stu-id="61909-143"><a href="eventreasonenum.md">EventReasonEnum</a></span></span></p></td>
<td><p><span data-ttu-id="61909-144">Especifica a razão que fez com que ocorresse um evento.</span><span class="sxs-lookup"><span data-stu-id="61909-144">Specifies the reason that caused an event to occur.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="61909-145"><a href="eventstatusenum.md">EventStatusEnum</a></span><span class="sxs-lookup"><span data-stu-id="61909-145"><a href="eventstatusenum.md">EventStatusEnum</a></span></span></p></td>
<td><p><span data-ttu-id="61909-146">Especifica o status atual da execução de um evento.</span><span class="sxs-lookup"><span data-stu-id="61909-146">Specifies the current status of the execution of an event.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="61909-147"><a href="executeoptionenum.md">ExecuteOptionEnum</a></span><span class="sxs-lookup"><span data-stu-id="61909-147"><a href="executeoptionenum.md">ExecuteOptionEnum</a></span></span></p></td>
<td><p><span data-ttu-id="61909-148">Especifica como um provedor deve executar um comando.</span><span class="sxs-lookup"><span data-stu-id="61909-148">Specifies how a provider should execute a command.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="61909-149"><a href="fieldenum.md">FieldEnum</a></span><span class="sxs-lookup"><span data-stu-id="61909-149"><a href="fieldenum.md">FieldEnum</a></span></span></p></td>
<td><p><span data-ttu-id="61909-150">Especifica os campos especiais mencionados em uma coleção de <strong>Campos</strong> do objeto <strong>Record</strong>.</span><span class="sxs-lookup"><span data-stu-id="61909-150">Specifies the special fields referenced in a <strong>Record</strong> object's <strong>Fields</strong> collection.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="61909-151"><a href="fieldattributeenum.md">FieldAttributeEnum</a></span><span class="sxs-lookup"><span data-stu-id="61909-151"><a href="fieldattributeenum.md">FieldAttributeEnum</a></span></span></p></td>
<td><p><span data-ttu-id="61909-152">Especifica um ou mais atributos de um objeto <strong>Field</strong>.</span><span class="sxs-lookup"><span data-stu-id="61909-152">Specifies one or more attributes of a <strong>Field</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="61909-153"><a href="fieldstatusenum.md">FieldStatusEnum</a></span><span class="sxs-lookup"><span data-stu-id="61909-153"><a href="fieldstatusenum.md">FieldStatusEnum</a></span></span></p></td>
<td><p><span data-ttu-id="61909-154">Especifica o status de um objeto <strong>Field</strong>.</span><span class="sxs-lookup"><span data-stu-id="61909-154">Specifies the status of a <strong>Field</strong> object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="61909-155"><a href="filtergroupenum.md">FilterGroupEnum</a></span><span class="sxs-lookup"><span data-stu-id="61909-155"><a href="filtergroupenum.md">FilterGroupEnum</a></span></span></p></td>
<td><p><span data-ttu-id="61909-156">Especifica o grupo de registros a serem filtrados a partir de um <strong>Recordset</strong>.</span><span class="sxs-lookup"><span data-stu-id="61909-156">Specifies the group of records to be filtered from a <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="61909-157"><a href="getrowsoptionenum.md">GetRowsOptionEnum</a></span><span class="sxs-lookup"><span data-stu-id="61909-157"><a href="getrowsoptionenum.md">GetRowsOptionEnum</a></span></span></p></td>
<td><p><span data-ttu-id="61909-158">Especifica quantos registros devem ser recuperados de um <strong>Recorset</strong>.</span><span class="sxs-lookup"><span data-stu-id="61909-158">Specifies how many records to retrieve from a <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="61909-159"><a href="isolationlevelenum.md">IsolationLevelEnum</a></span><span class="sxs-lookup"><span data-stu-id="61909-159"><a href="isolationlevelenum.md">IsolationLevelEnum</a></span></span></p></td>
<td><p><span data-ttu-id="61909-160">Especifica o nível de isolamento da transação para um objeto <strong>Connection</strong>.</span><span class="sxs-lookup"><span data-stu-id="61909-160">Specifies the level of transaction isolation for a <strong>Connection</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="61909-161"><a href="lineseparatorsenum.md">LineSeparatorsEnum</a></span><span class="sxs-lookup"><span data-stu-id="61909-161"><a href="lineseparatorsenum.md">LineSeparatorsEnum</a></span></span></p></td>
<td><p><span data-ttu-id="61909-162">Especifica o caractere usado como um separador de linha nos objetos <strong>Stream</strong> de texto.</span><span class="sxs-lookup"><span data-stu-id="61909-162">Specifies the character used as a line separator in text <strong>Stream</strong> objects.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="61909-163"><a href="locktypeenum.md">LockTypeEnum</a></span><span class="sxs-lookup"><span data-stu-id="61909-163"><a href="locktypeenum.md">LockTypeEnum</a></span></span></p></td>
<td><p><span data-ttu-id="61909-164">Especifica o tipo de bloqueio colocado nos registros durante a edição.</span><span class="sxs-lookup"><span data-stu-id="61909-164">Specifies the type of lock placed on records during editing.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="61909-165"><a href="marshaloptionsenum.md">MarshalOptionsEnum</a></span><span class="sxs-lookup"><span data-stu-id="61909-165"><a href="marshaloptionsenum.md">MarshalOptionsEnum</a></span></span></p></td>
<td><p><span data-ttu-id="61909-166">Especifica quais registros devem ser retornados ao servidor.</span><span class="sxs-lookup"><span data-stu-id="61909-166">Specifies which records should be returned to the server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="61909-167"><a href="moverecordoptionsenum.md">MoveRecordOptionsEnum</a></span><span class="sxs-lookup"><span data-stu-id="61909-167"><a href="moverecordoptionsenum.md">MoveRecordOptionsEnum</a></span></span></p></td>
<td><p><span data-ttu-id="61909-168">Especifica o comportamento do objeto <strong>Record</strong> do método <strong>MoveRecord</strong>.</span><span class="sxs-lookup"><span data-stu-id="61909-168">Specifies the behavior of the <strong>Record</strong> object <strong>MoveRecord</strong> method.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="61909-169"><a href="objectstateenum.md">ObjectStateEnum</a></span><span class="sxs-lookup"><span data-stu-id="61909-169"><a href="objectstateenum.md">ObjectStateEnum</a></span></span></p></td>
<td><p><span data-ttu-id="61909-170">Especifica se um objeto está aberto ou fechado, conectando a uma fonte de dados, executando um comando ou buscando dados.</span><span class="sxs-lookup"><span data-stu-id="61909-170">Specifies whether an object is open or closed, connecting to a data source, executing a command, or fetching data.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="61909-171"><a href="parameterattributesenum.md">ParameterAttributesEnum</a></span><span class="sxs-lookup"><span data-stu-id="61909-171"><a href="parameterattributesenum.md">ParameterAttributesEnum</a></span></span></p></td>
<td><p><span data-ttu-id="61909-172">Especifica os atributos de um objeto <strong>Parameter</strong>.</span><span class="sxs-lookup"><span data-stu-id="61909-172">Specifies the attributes of a <strong>Parameter</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="61909-173"><a href="parameterdirectionenum.md">ParameterDirectionEnum</a></span><span class="sxs-lookup"><span data-stu-id="61909-173"><a href="parameterdirectionenum.md">ParameterDirectionEnum</a></span></span></p></td>
<td><p><span data-ttu-id="61909-174">Especifica se <strong>Parameter</strong> representa um parâmetro de entrada, de saída, ou ambos, ou se é o valor de retorno de um procedimento armazenado.</span><span class="sxs-lookup"><span data-stu-id="61909-174">Specifies whether the <strong>Parameter</strong> represents an input parameter, an output parameter, or both, or if the parameter is the return value from a stored procedure.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="61909-175"><a href="persistformatenum.md">PersistFormatEnum</a></span><span class="sxs-lookup"><span data-stu-id="61909-175"><a href="persistformatenum.md">PersistFormatEnum</a></span></span></p></td>
<td><p><span data-ttu-id="61909-176">Especifica o formato no qual se deve salvar um <strong>Recorset</strong>.</span><span class="sxs-lookup"><span data-stu-id="61909-176">Specifies the format in which to save a <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="61909-177"><a href="positionenum.md">PositionEnum</a></span><span class="sxs-lookup"><span data-stu-id="61909-177"><a href="positionenum.md">PositionEnum</a></span></span></p></td>
<td><p><span data-ttu-id="61909-178">Especifica a posição atual do ponteiro do registro em um <strong>Recordset</strong>.</span><span class="sxs-lookup"><span data-stu-id="61909-178">Specifies the current position of the record pointer within a <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="61909-179"><a href="propertyattributesenum.md">PropertyAttributesEnum</a></span><span class="sxs-lookup"><span data-stu-id="61909-179"><a href="propertyattributesenum.md">PropertyAttributesEnum</a></span></span></p></td>
<td><p><span data-ttu-id="61909-180">Especifica os atributos de um objeto <strong>Property</strong>.</span><span class="sxs-lookup"><span data-stu-id="61909-180">Specifies the attributes of a <strong>Property</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="61909-181"><a href="recordcreateoptionsenum.md">RecordCreateOptionsEnum</a></span><span class="sxs-lookup"><span data-stu-id="61909-181"><a href="recordcreateoptionsenum.md">RecordCreateOptionsEnum</a></span></span></p></td>
<td><p><span data-ttu-id="61909-182">Especifica o método <strong>Open</strong> do objeto <strong>Record</strong> se um <strong>Record</strong> existente estiver aberto ou se um novo <strong>Record</strong> for criado.</span><span class="sxs-lookup"><span data-stu-id="61909-182">Specifies for the <strong>Record</strong> object <strong>Open</strong> method whether an existing <strong>Record</strong> should be opened, or a new <strong>Record</strong> should be created.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="61909-183"><a href="recordopenoptionsenum.md">RecordOpenOptionsEnum</a></span><span class="sxs-lookup"><span data-stu-id="61909-183"><a href="recordopenoptionsenum.md">RecordOpenOptionsEnum</a></span></span></p></td>
<td><p><span data-ttu-id="61909-p102">Especifica as opções para abrir um objeto <strong>Record</strong>. Esses valores podem ser combinados utilizando um operador OR.</span><span class="sxs-lookup"><span data-stu-id="61909-p102">Specifies options for opening a <strong>Record</strong>. These values may be combined by using an OR operator.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="61909-186"><a href="recordstatusenum.md">RecordStatusEnum</a></span><span class="sxs-lookup"><span data-stu-id="61909-186"><a href="recordstatusenum.md">RecordStatusEnum</a></span></span></p></td>
<td><p><span data-ttu-id="61909-187">Especifica o status de um registro com relação a atualizações de batch e outras operações em massa.</span><span class="sxs-lookup"><span data-stu-id="61909-187">Specifies the status of a record with regard to batch updates and other bulk operations.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="61909-188"><a href="recordtypeenum.md">RecordTypeEnum</a></span><span class="sxs-lookup"><span data-stu-id="61909-188"><a href="recordtypeenum.md">RecordTypeEnum</a></span></span></p></td>
<td><p><span data-ttu-id="61909-189">Especifica o tipo de objeto <strong>Record</strong>.</span><span class="sxs-lookup"><span data-stu-id="61909-189">Specifies the type of <strong>Record</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="61909-190"><a href="resyncenum.md">ResyncEnum</a></span><span class="sxs-lookup"><span data-stu-id="61909-190"><a href="resyncenum.md">ResyncEnum</a></span></span></p></td>
<td><p><span data-ttu-id="61909-191">Especifica se os valores subjacentes são sobregravados por uma chamada para <strong>Resync</strong>.</span><span class="sxs-lookup"><span data-stu-id="61909-191">Specifies whether underlying values are overwritten by a call to <strong>Resync</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="61909-192"><a href="saveoptionsenum.md">SaveOptionsEnum</a></span><span class="sxs-lookup"><span data-stu-id="61909-192"><a href="saveoptionsenum.md">SaveOptionsEnum</a></span></span></p></td>
<td><p><span data-ttu-id="61909-p103">Especifica se um arquivo deveria ser criado ou sobregravado ao salvar a partir de um objeto <strong>Stream</strong>. Os valores podem ser combinados com um operador AND.</span><span class="sxs-lookup"><span data-stu-id="61909-p103">Specifies whether a file should be created or overwritten when saving from a <strong>Stream</strong> object. The values can be combined with an AND operator.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="61909-195"><a href="schemaenum.md">SchemaEnum</a></span><span class="sxs-lookup"><span data-stu-id="61909-195"><a href="schemaenum.md">SchemaEnum</a></span></span></p></td>
<td><p><span data-ttu-id="61909-p104">Especifica o tipo de esquema <strong>Recordset</strong> que o método <strong>OpenSchema</strong> recupera. Especifica a direção de uma pesquisa de registro dentro de um <strong>Recordset</strong>.</span><span class="sxs-lookup"><span data-stu-id="61909-p104">Specifies the type of schema <strong>Recordset</strong> that the <strong>OpenSchema</strong> method retrieves. Specifies the direction of a record search within a <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="61909-198"><a href="searchdirectionenum.md">SearchDirectionEnum</a></span><span class="sxs-lookup"><span data-stu-id="61909-198"><a href="searchdirectionenum.md">SearchDirectionEnum</a></span></span></p></td>
<td><p><span data-ttu-id="61909-199">Especifica a direção de uma pesquisa de registro dentro de um <strong>Recordset</strong>. Especifica o tipo de <strong>Seek</strong> a ser executado.</span><span class="sxs-lookup"><span data-stu-id="61909-199">Specifies the direction of a record search within a <strong>Recordset</strong>.Specifies the type of <strong>Seek</strong> to execute.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="61909-200"><a href="seekenum.md">SeekEnum</a></span><span class="sxs-lookup"><span data-stu-id="61909-200"><a href="seekenum.md">SeekEnum</a></span></span></p></td>
<td><p><span data-ttu-id="61909-p105">Especifica o tipo de <strong>Seek</strong> a ser executado. Especifica as opções para a abertura de um objeto <strong>Stream</strong>. Os valores podem ser combinados a um operador AND.</span><span class="sxs-lookup"><span data-stu-id="61909-p105">Specifies the type of <strong>Seek</strong> to execute.Specifies options for opening a <strong>Stream</strong> object. The values can be combined with an AND operator.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="61909-203"><a href="streamopenoptionsenum.md">StreamOpenOptionsEnum</a></span><span class="sxs-lookup"><span data-stu-id="61909-203"><a href="streamopenoptionsenum.md">StreamOpenOptionsEnum</a></span></span></p></td>
<td><p><span data-ttu-id="61909-p106">Especifica as opções para abrir um objeto <strong>Stream</strong>. Os valores podem ser combinados a um operador AND. Especifica se o fluxo inteiro ou a próxima linha deve ser lida a partir do objeto <strong>Stream</strong>.</span><span class="sxs-lookup"><span data-stu-id="61909-p106">Specifies options for opening a <strong>Stream</strong> object. The values can be combined with an AND operator.Specifies whether the whole stream or the next line should be read from a <strong>Stream</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="61909-206"><a href="streamreadenum.md">StreamReadEnum</a></span><span class="sxs-lookup"><span data-stu-id="61909-206"><a href="streamreadenum.md">StreamReadEnum</a></span></span></p></td>
<td><p><span data-ttu-id="61909-207">Especifica se o fluxo inteiro ou a próxima linha deve ser lida a partir do objeto <strong>Stream</strong>. Especifica os tipos de dados armazenados em um objeto <strong>Stream</strong>.</span><span class="sxs-lookup"><span data-stu-id="61909-207">Specifies whether the whole stream or the next line should be read from a <strong>Stream</strong> object.Specifies the type of data stored in a <strong>Stream</strong> object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="61909-208"><a href="streamtypeenum.md">StreamTypeEnum</a></span><span class="sxs-lookup"><span data-stu-id="61909-208"><a href="streamtypeenum.md">StreamTypeEnum</a></span></span></p></td>
<td><p><span data-ttu-id="61909-209">Especifica os tipos de dados armazenados em um objeto <strong>Stream</strong>. Especifica se um separador de linha está anexado à sequência de caracteres escrita no objeto <strong>Stream</strong>.</span><span class="sxs-lookup"><span data-stu-id="61909-209">Specifies the type of data stored in a <strong>Stream</strong> object.Specifies whether a line separator is appended to the string written to a <strong>Stream</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="61909-210"><a href="streamwriteenum.md">StreamWriteEnum</a></span><span class="sxs-lookup"><span data-stu-id="61909-210"><a href="streamwriteenum.md">StreamWriteEnum</a></span></span></p></td>
<td><p><span data-ttu-id="61909-211">Especifica se um separador de linha está anexado à sequência de caracteres escrita no objeto <strong>Stream</strong>. Especifica o formato ao recuperar um <strong>Recordset</strong> como uma sequência de caracteres.</span><span class="sxs-lookup"><span data-stu-id="61909-211">Specifies whether a line separator is appended to the string written to a <strong>Stream</strong> object.Specifies the format when retrieving a <strong>Recordset</strong> as a string.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="61909-212"><a href="stringformatenum.md">StringFormatEnum</a></span><span class="sxs-lookup"><span data-stu-id="61909-212"><a href="stringformatenum.md">StringFormatEnum</a></span></span></p></td>
<td><p><span data-ttu-id="61909-213">Especifica o formato ao recuperar um <strong>Recordset</strong> como uma sequência de caracteres. Especifica os atributos da transação de um objeto <strong>Connection</strong>.</span><span class="sxs-lookup"><span data-stu-id="61909-213">Specifies the format when retrieving a <strong>Recordset</strong> as a string.Specifies the transaction attributes of a <strong>Connection</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="61909-214"><a href="xactattributeenum.md">XactAttributeEnum</a></span><span class="sxs-lookup"><span data-stu-id="61909-214"><a href="xactattributeenum.md">XactAttributeEnum</a></span></span></p></td>
<td><p><span data-ttu-id="61909-215">Especifica os atributos de transação de um objeto <strong>Connection</strong>.</span><span class="sxs-lookup"><span data-stu-id="61909-215">Specifies the transaction attributes of a <strong>Connection</strong> object.</span></span></p></td>
</tr>
</tbody>
</table>

