---
title: Microsoft Cursor Service for OLE DB (Componente de Serviço do ADO)
TOCTitle: Microsoft Cursor Service for OLE DB (ADO Service Component)
ms:assetid: 6818fc05-9c9f-9b67-07d2-e622c93133c2
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249405(v=office.15)
ms:contentKeyID: 48545376
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: d79d060922c6e7f28209242ebe82821c2ba97bfd
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28713727"
---
# <a name="microsoft-cursor-service-for-ole-db-ado-service-component"></a><span data-ttu-id="66f94-102">Microsoft Cursor Service for OLE DB (Componente de Serviço do ADO)</span><span class="sxs-lookup"><span data-stu-id="66f94-102">Microsoft Cursor Service for OLE DB (ADO Service Component)</span></span>


<span data-ttu-id="66f94-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="66f94-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="66f94-p101">O Microsoft Cursor Service for OLE DB complementa as funções de suporte do cursor dos provedores de dados. Como resultado, o usuário percebe uma funcionalidade relativamente uniforme de todos os provedores de dados.</span><span class="sxs-lookup"><span data-stu-id="66f94-p101">The Microsoft Cursor Service for OLE DB supplements the cursor support functions of data providers. As a result, the user perceives relatively uniform functionality from all data providers.</span></span>

<span data-ttu-id="66f94-p102">O Cursor Service disponibiliza propriedades dinâmicas e melhora o comportamento de determinados métodos. Por exemplo, a propriedade dinâmica [Optimize](optimize-property-dynamic-ado.md) permite a criação de índices temporários para facilitar determinadas operações, como o método [Find](find-method-ado.md).</span><span class="sxs-lookup"><span data-stu-id="66f94-p102">The Cursor Service makes dynamic properties available and enhances the behavior of certain methods. For example, the [Optimize](optimize-property-dynamic-ado.md) dynamic property enables the creation of temporary indexes to facilitate certain operations, such as the [Find](find-method-ado.md) method.</span></span>

<span data-ttu-id="66f94-p103">O Cursor Service permite o suporte para atualização em lote em todos os casos. Além disso, ele simula tipos de cursores mais avançados, como os cursores dinâmicos, quando um provedor de dados pode oferecer suporte apenas a cursores com menos recursos, como os cursores estáticos.</span><span class="sxs-lookup"><span data-stu-id="66f94-p103">The Cursor Service enables support for batch updating in all cases. It also simulates more capable cursor types, such as dynamic cursors, when a data provider can only supply less capable cursors, such as static cursors.</span></span>

## <a name="keyword"></a><span data-ttu-id="66f94-110">Palavra-chave</span><span class="sxs-lookup"><span data-stu-id="66f94-110">Keyword</span></span>

<span data-ttu-id="66f94-111">Para invocar esse componente de serviço, defina a propriedade [CursorLocation](recordset-object-ado.md) dos objetos [Recordset](connection-object-ado.md) ou [Connection](cursorlocation-property-ado.md) como **adUseClient**.</span><span class="sxs-lookup"><span data-stu-id="66f94-111">To invoke this service component, set the [Recordset](recordset-object-ado.md) or [Connection](connection-object-ado.md) object's [CursorLocation](cursorlocation-property-ado.md) property to **adUseClient**.</span></span>

`connection.CursorLocation=adUseClientrecordset.CursorLocation=adUseClient`

## <a name="dynamic-properties"></a><span data-ttu-id="66f94-112">Propriedades dinâmicas</span><span class="sxs-lookup"><span data-stu-id="66f94-112">Dynamic Properties</span></span>

<span data-ttu-id="66f94-p104">Quando o Cursor Service para OLE DB é invocado, as propriedades dinâmicas listadas abaixo são adicionadas à coleção **Properties** do objeto [Recordset](properties-collection-ado.md). A lista completa de propriedades dinâmicas dos objetos **Connection** e **Recordset** é fornecida no [Índice de Propriedades Dinâmicas do ADO](ado-dynamic-property-index.md). Os nomes das propriedades associadas do OLE DB, quando adequados, são incluídos entre parênteses após o nome da propriedade do ADO.</span><span class="sxs-lookup"><span data-stu-id="66f94-p104">When the Cursor Service for OLE DB is invoked, the following dynamic properties are added to the **Recordset** object's [Properties](properties-collection-ado.md) collection. The full list of **Connection** and **Recordset** object dynamic properties is listed in the [ADO Dynamic Property Index](ado-dynamic-property-index.md). The associated OLE DB property names, where appropriate, are included in parenthesis after the ADO property name.</span></span>

<span data-ttu-id="66f94-116">As alterações em algumas propriedades dinâmicas não são visíveis para a fonte de dados de base depois que o Cursor Service é invocado.</span><span class="sxs-lookup"><span data-stu-id="66f94-116">Changes to some dynamic properties are not visible to the underlying data source after the Cursor Service has been invoked.</span></span> <span data-ttu-id="66f94-117">Por exemplo, a configuração da propriedade de *Comando de tempo limite* em um **Recordset** não será visível para o provedor de dados subjacente.</span><span class="sxs-lookup"><span data-stu-id="66f94-117">For example, setting the *Command Time out* property on a **Recordset** will not be visible to the underlying data provider.</span></span>

```vb 
... 
Recordset1.CursorLocation = adUseClient 'invokes cursor service 
Recordset1.Open "authors", _ 
 "Provider=SQLOLEDB;Data Source=DBServer;User Id=usr;" & _ 
 "Password=pwd;Initial Catalog=pubs;",,adCmdTable 
Recordset1.Properties.Item("Command Time out") = 50 
' 'Command Time out' property on DBServer is still default (30). 
... 

```

<span data-ttu-id="66f94-p106">Se o seu aplicativo exige o Cursor Service, mas você precisa definir propriedades dinâmicas no provedor de base, defina as propriedades antes de chamar o Cursor Service. As definições de propriedades de objetos de comando sempre são passadas para o provedor de dados de base, independentemente do local do cursor. Portanto, você também pode usar um objeto de comando para definir as propriedades a qualquer momento.</span><span class="sxs-lookup"><span data-stu-id="66f94-p106">If your application requires the Cursor Service, but you need to set dynamic properties on the underlying provider, set the properties before invoking the Cursor Service. Command object property settings are always passed to the underlying data provider regardless of cursor location. Therefore, you can also use a command object to set the properties at any time.</span></span>

> [!NOTE]
> <span data-ttu-id="66f94-121">O serviço de cursor não oferece suporte à propriedade dinâmica DBPROP_SERVERDATAONINSERT, mesmo que o provedor de dados de base ofereça esse suporte.</span><span class="sxs-lookup"><span data-stu-id="66f94-121">The dynamic property DBPROP_SERVERDATAONINSERT is not supported by the cursor service, even if it is supported by the underlying data provider.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="66f94-122">Nome da propriedade</span><span class="sxs-lookup"><span data-stu-id="66f94-122">Property Name</span></span></p></th>
<th><p><span data-ttu-id="66f94-123">Descrição</span><span class="sxs-lookup"><span data-stu-id="66f94-123">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="66f94-124">Auto Recalc</span><span class="sxs-lookup"><span data-stu-id="66f94-124">Auto Recalc</span></span><br />
<span data-ttu-id="66f94-125">(DBPROP_ADC_AUTORECALC)</span><span class="sxs-lookup"><span data-stu-id="66f94-125">(DBPROP_ADC_AUTORECALC)</span></span></p></td>
<td><p><span data-ttu-id="66f94-p107">Nos conjuntos de registros criados com o Data Shaping Service, esse valor indica com que frequência as colunas calculadas e agregadas serão calculadas. O padrão (valor=1) é recalcular sempre que o Data Shaping Service determinar que os valores foram alterados. Se o valor for 0, as colunas calculadas ou agregadas serão calculadas somente durante a construção inicial da hierarquia.</span><span class="sxs-lookup"><span data-stu-id="66f94-p107">For recordsets created with the Data Shaping Service, this value indicates how often calculated and aggregate columns are calculated. The default (value=1) is to recalculate whenever the Data Shaping Service determines that the values have changed. If the value is 0, the calculated or aggregate columns are only calculated when the hierarchy is initially built.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="66f94-129">Batch Size</span><span class="sxs-lookup"><span data-stu-id="66f94-129">Batch Size</span></span><br />
<span data-ttu-id="66f94-130">(DBPROP_ADC_BATCHSIZE)</span><span class="sxs-lookup"><span data-stu-id="66f94-130">(DBPROP_ADC_BATCHSIZE)</span></span></p></td>
<td><p><span data-ttu-id="66f94-p108">Indica o número de instruções de atualização que podem ser colocadas em lote antes de serem enviadas para o repositório de dados. Quanto maior for o número de instruções em um lote, menos ciclos de armazenamento de dados serão necessários.</span><span class="sxs-lookup"><span data-stu-id="66f94-p108">Indicates the number of update statements that can be batched before being sent to the data store. The more statements in a batch, the fewer round trips to the data store.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="66f94-133">Cache Child Rows</span><span class="sxs-lookup"><span data-stu-id="66f94-133">Cache Child Rows</span></span><br />
<span data-ttu-id="66f94-134">(DBPROP_ADC_CACHECHILDROWS)</span><span class="sxs-lookup"><span data-stu-id="66f94-134">(DBPROP_ADC_CACHECHILDROWS)</span></span></p></td>
<td><p><span data-ttu-id="66f94-135">Nos conjuntos de registros criados com o Data Shaping Service, este valor indica se os conjuntos de registros filhos serão armazenados em um cache para utilização posterior.</span><span class="sxs-lookup"><span data-stu-id="66f94-135">For recordsets created with the Data Shaping Service, this value indicates whether child recordsets are stored in a cache for later use.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="66f94-136">Cursor Engine Version</span><span class="sxs-lookup"><span data-stu-id="66f94-136">Cursor Engine Version</span></span><br />
<span data-ttu-id="66f94-137">(DBPROP_ADC_CEVER)</span><span class="sxs-lookup"><span data-stu-id="66f94-137">(DBPROP_ADC_CEVER)</span></span></p></td>
<td><p><span data-ttu-id="66f94-138">Indica a versão do Cursor Service que está sendo utilizada.</span><span class="sxs-lookup"><span data-stu-id="66f94-138">Indicates the version of the Cursor Service being used.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="66f94-139">Maintain Change Status</span><span class="sxs-lookup"><span data-stu-id="66f94-139">Maintain Change Status</span></span><br />
<span data-ttu-id="66f94-140">(DBPROP_ADC_MAINTAINCHANGESTATUS)</span><span class="sxs-lookup"><span data-stu-id="66f94-140">(DBPROP_ADC_MAINTAINCHANGESTATUS)</span></span></p></td>
<td><p><span data-ttu-id="66f94-141">Indica o texto do comando utilizado para sincronizar novamente uma ou mais linhas em uma junção de várias tabelas.</span><span class="sxs-lookup"><span data-stu-id="66f94-141">Indicates the text of the command used for resynchronizing a one or more rows in a multiple table join.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="66f94-142"><a href="optimize-property-dynamic-ado.md">Otimizar</a></span><span class="sxs-lookup"><span data-stu-id="66f94-142"><a href="optimize-property-dynamic-ado.md">Optimize</a></span></span></p></td>
<td><p><span data-ttu-id="66f94-p109">Indica se um índice deverá ser criado. Se for definido como <strong>True</strong>, autorizará a criação temporária de índices para melhorar a execução de determinadas operações.</span><span class="sxs-lookup"><span data-stu-id="66f94-p109">Indicates whether an index should be created. When set to <strong>True</strong>, authorizes the temporary creation of indexes to improve the execution of certain operations.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="66f94-145"><a href="reshape-name-property-dynamic-ado.md">Reshape Name</a></span><span class="sxs-lookup"><span data-stu-id="66f94-145"><a href="reshape-name-property-dynamic-ado.md">Reshape Name</a></span></span></p></td>
<td><p><span data-ttu-id="66f94-p110">Indica o nome do <strong>Recordset</strong>. Pode ser referenciado nos comandos atuais ou de data shaping subsequentes.</span><span class="sxs-lookup"><span data-stu-id="66f94-p110">Indicates the name of the <strong>Recordset</strong>. May be referenced within the current, or subsequent, data shaping commands.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="66f94-148"><a href="resync-command-property-dynamic-ado.md">Resync Command</a></span><span class="sxs-lookup"><span data-stu-id="66f94-148"><a href="resync-command-property-dynamic-ado.md">Resync Command</a></span></span></p></td>
<td><p><span data-ttu-id="66f94-149">Indica uma sequência de comandos personalizada utilizada pelo método <a href="resync-method-ado.md">Resync</a> quando a propriedade <a href="unique-table-unique-schema-unique-catalog-properties-dynamic-ado.md">Unique Table</a> estiver em vigor.</span><span class="sxs-lookup"><span data-stu-id="66f94-149">Indicates a custom command string that is used by the <a href="resync-method-ado.md">Resync</a> method when the <a href="unique-table-unique-schema-unique-catalog-properties-dynamic-ado.md">Unique Table</a> property is in effect.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="66f94-150"><a href="unique-table-unique-schema-unique-catalog-properties-dynamic-ado.md">Unique Catalog</a></span><span class="sxs-lookup"><span data-stu-id="66f94-150"><a href="unique-table-unique-schema-unique-catalog-properties-dynamic-ado.md">Unique Catalog</a></span></span></p></td>
<td><p><span data-ttu-id="66f94-151">Indica o nome do banco de dados que contém a tabela referenciada na propriedade <strong>Unique Table</strong>.</span><span class="sxs-lookup"><span data-stu-id="66f94-151">Indicates the name of the database containing the table referenced in the <strong>Unique Table</strong> property.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="66f94-152"><a href="unique-table-unique-schema-unique-catalog-properties-dynamic-ado.md">Unique Schema</a></span><span class="sxs-lookup"><span data-stu-id="66f94-152"><a href="unique-table-unique-schema-unique-catalog-properties-dynamic-ado.md">Unique Schema</a></span></span></p></td>
<td><p><span data-ttu-id="66f94-153">Indica o nome do proprietário da tabela referenciada na propriedade <strong>Unique Table</strong>.</span><span class="sxs-lookup"><span data-stu-id="66f94-153">Indicates the name of the owner of the table referenced in the <strong>Unique Table</strong> property.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="66f94-154"><a href="unique-table-unique-schema-unique-catalog-properties-dynamic-ado.md">Unique Table</a></span><span class="sxs-lookup"><span data-stu-id="66f94-154"><a href="unique-table-unique-schema-unique-catalog-properties-dynamic-ado.md">Unique Table</a></span></span></p></td>
<td><p><span data-ttu-id="66f94-155">Indica o nome da tabela única criada em um <strong>Recordset</strong> a partir de várias tabelas que podem ter sido modificadas por inserções, atualizações ou exclusões.</span><span class="sxs-lookup"><span data-stu-id="66f94-155">Indicates the name of the one table in a <strong>Recordset</strong> created from multiple tables that may be modified by insertions, updates, or deletions.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="66f94-156">Update Criteria</span><span class="sxs-lookup"><span data-stu-id="66f94-156">Update Criteria</span></span><br />
<span data-ttu-id="66f94-157">(DBPROP_ADC_UPDATECRITERIA)</span><span class="sxs-lookup"><span data-stu-id="66f94-157">(DBPROP_ADC_UPDATECRITERIA)</span></span></p></td>
<td><p><span data-ttu-id="66f94-158">Indica quais campos da cláusula <strong>WHERE</strong> serão utilizados para lidar com colisões que ocorram durante uma atualização.</span><span class="sxs-lookup"><span data-stu-id="66f94-158">Indicates which fields in the <strong>WHERE</strong> clause are used to handle collisions occurring during an update.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="66f94-159"><a href="update-resync-property-dynamic-ado.md">Update Resync</a>(DBPROP_ADC_UPDATERESYNC)</span><span class="sxs-lookup"><span data-stu-id="66f94-159"><a href="update-resync-property-dynamic-ado.md">Update Resync</a>(DBPROP_ADC_UPDATERESYNC)</span></span></p></td>
<td><p><span data-ttu-id="66f94-160">Indica se o método <strong>Resync</strong> será invocado implicitamente após o método <a href="updatebatch-method-ado.md">UpdateBatch</a> (e seu comportamento) quando a propriedade <strong>Unique Table</strong> estiver em vigor.</span><span class="sxs-lookup"><span data-stu-id="66f94-160">Indicates whether the <strong>Resync</strong> method is implicitly invoked after the <a href="updatebatch-method-ado.md">UpdateBatch</a> method (and its behavior), when the <strong>Unique Table</strong> property is in effect.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="66f94-p111">Você também pode definir ou recuperar uma propriedade dinâmica especificando o seu nome como índice da coleção **Properties**. Isso, por exemplo, recupera e imprime o valor atual da propriedade dinâmica [Optimize](optimize-property-dynamic-ado.md) e depois define um novo valor:</span><span class="sxs-lookup"><span data-stu-id="66f94-p111">You may also set or retrieve a dynamic property by specifying its name as the index to the **Properties** collection. For example, get and print the current value of the [Optimize](optimize-property-dynamic-ado.md) dynamic property, then set a new value, like this:</span></span>

```vb 
 
Debug.Print rs.Properties("Optimize") 
rs.Properties("Optimize") = True 
```

## <a name="built-in-property-behavior"></a><span data-ttu-id="66f94-163">Comportamento de propriedades internas</span><span class="sxs-lookup"><span data-stu-id="66f94-163">Built-in Property Behavior</span></span>

<span data-ttu-id="66f94-164">O Cursor Service para OLE DB também afeta o comportamento de determinadas propriedades internas.</span><span class="sxs-lookup"><span data-stu-id="66f94-164">The Cursor Service for OLE DB also affects the behavior of certain built-in properties.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="66f94-165">Nome da propriedade</span><span class="sxs-lookup"><span data-stu-id="66f94-165">Property Name</span></span></p></th>
<th><p><span data-ttu-id="66f94-166">Descrição</span><span class="sxs-lookup"><span data-stu-id="66f94-166">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="66f94-167"><a href="cursortype-property-ado.md">CursorType</a></span><span class="sxs-lookup"><span data-stu-id="66f94-167"><a href="cursortype-property-ado.md">CursorType</a></span></span></p></td>
<td><p><span data-ttu-id="66f94-168">Complementa os tipos de cursores que estão disponíveis para um <strong>Recordset</strong>.</span><span class="sxs-lookup"><span data-stu-id="66f94-168">Supplements the types of cursors that are available for a <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="66f94-169"><a href="locktype-property-ado.md">LockType</a></span><span class="sxs-lookup"><span data-stu-id="66f94-169"><a href="locktype-property-ado.md">LockType</a></span></span></p></td>
<td><p><span data-ttu-id="66f94-p112">Complementa os tipos de bloqueios que estão disponíveis para um <strong>Recordset</strong>. Habilita atualizações em lote.</span><span class="sxs-lookup"><span data-stu-id="66f94-p112">Supplements the types of locks available for a <strong>Recordset</strong>. Enables batch updates.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="66f94-172"><a href="sort-property-ado.md">Sort</a></span><span class="sxs-lookup"><span data-stu-id="66f94-172"><a href="sort-property-ado.md">Sort</a></span></span></p></td>
<td><p><span data-ttu-id="66f94-173">Especifica um ou mais nomes de campos com base nos quais o <strong>Recordset</strong> será classificado e se cada campo será classificado em ordem crescente ou decrescente.</span><span class="sxs-lookup"><span data-stu-id="66f94-173">Specifies one or more field names that the <strong>Recordset</strong> is sorted on, and whether each field is sorted in ascending or descending order.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="method-behavior"></a><span data-ttu-id="66f94-174">Comportamento de métodos</span><span class="sxs-lookup"><span data-stu-id="66f94-174">Method Behavior</span></span>

<span data-ttu-id="66f94-175">O Cursor Service para OLE DB habilita ou afeta o comportamento do método [Append](field-object-ado.md) do objeto [Field](append-method-ado.md); e dos métodos **Open**, [Resync](open-method-ado-recordset.md), [UpdateBatch](resync-method-ado.md) e [Save](updatebatch-method-ado.md) do objeto [Recordset](save-method-ado.md).</span><span class="sxs-lookup"><span data-stu-id="66f94-175">The Cursor Service for OLE DB enables or affects the behavior of the [Field](field-object-ado.md) object's [Append](append-method-ado.md) method; and the **Recordset** object's [Open](open-method-ado-recordset.md), [Resync](resync-method-ado.md), [UpdateBatch](updatebatch-method-ado.md), and [Save](save-method-ado.md) methods.</span></span>

