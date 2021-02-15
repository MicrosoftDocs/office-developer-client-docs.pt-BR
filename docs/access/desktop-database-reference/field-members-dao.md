---
title: Membros de campo (DAO)
TOCTitle: Field Members
ms:assetid: 4b6a587f-1fd0-37fb-db7d-75b587a8dc60
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193511(v=office.15)
ms:contentKeyID: 48544689
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 1a0e448662384572163fca074e554a5e30be30a7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293088"
---
# <a name="field-members-dao"></a><span data-ttu-id="290e7-102">Membros de campo (DAO)</span><span class="sxs-lookup"><span data-stu-id="290e7-102">Field members (DAO)</span></span>


<span data-ttu-id="290e7-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="290e7-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="290e7-104">Um objeto Field representa uma coluna de dados com um tipo de dados comum e um conjunto comum de propriedades.</span><span class="sxs-lookup"><span data-stu-id="290e7-104">A Field object represents a column of data with a common data type and a common set of properties.</span></span>

## <a name="methods"></a><span data-ttu-id="290e7-105">Métodos</span><span class="sxs-lookup"><span data-stu-id="290e7-105">Methods</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="290e7-106">Nome</span><span class="sxs-lookup"><span data-stu-id="290e7-106">Name</span></span></p></th>
<th><p><span data-ttu-id="290e7-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="290e7-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="290e7-108"><strong><a href="field-appendchunk-method-dao.md">AppendChunk</a></strong></span><span class="sxs-lookup"><span data-stu-id="290e7-108"><strong><a href="field-appendchunk-method-dao.md">AppendChunk</a></strong></span></span></p></td>
<td><p><span data-ttu-id="290e7-109">Acrescenta dados de uma expressão de cadeia de caracteres a um objeto <strong><a href="field-object-dao.md">Field</a></strong> Memo ou Long Binary em um <strong><a href="recordset-object-dao.md">Recordset</a></strong>.</span><span class="sxs-lookup"><span data-stu-id="290e7-109">Appends data from a string expression to a Memo or Long Binary <strong><a href="field-object-dao.md">Field</a></strong> object in a <strong><a href="recordset-object-dao.md">Recordset</a></strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="290e7-110"><strong><a href="field-createproperty-method-dao.md">CreateProperty</a></strong></span><span class="sxs-lookup"><span data-stu-id="290e7-110"><strong><a href="field-createproperty-method-dao.md">CreateProperty</a></strong></span></span></p></td>
<td><p><span data-ttu-id="290e7-111">Cria um novo objeto <strong><a href="property-object-dao.md">Property</a></strong> definido pelo usuário (apenas espaços de trabalho do Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="290e7-111">Creates a new user-defined <strong><a href="property-object-dao.md">Property</a></strong> object (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="290e7-112"><strong><a href="field-getchunk-method-dao.md">GetChunk</a></strong></span><span class="sxs-lookup"><span data-stu-id="290e7-112"><strong><a href="field-getchunk-method-dao.md">GetChunk</a></strong></span></span></p></td>
<td><p><span data-ttu-id="290e7-113">Retorna todo ou parte do conteúdo de um <strong>objeto Field Memo</strong> ou <strong>Long Binary</strong> <strong><a href="field-object-dao.md"></a></strong> na coleção <strong><a href="fields-collection-dao.md">Fields</a></strong> de um <strong><a href="recordset-object-dao.md">objeto Recordset</a></strong> .</span><span class="sxs-lookup"><span data-stu-id="290e7-113">Returns all or a portion of the contents of a <strong>Memo</strong> or <strong>Long Binary</strong> <strong><a href="field-object-dao.md">Field</a></strong> object in the <strong><a href="fields-collection-dao.md">Fields</a></strong> collection of a <strong><a href="recordset-object-dao.md">Recordset</a></strong> object.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="properties"></a><span data-ttu-id="290e7-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="290e7-114">Properties</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="290e7-115">Nome</span><span class="sxs-lookup"><span data-stu-id="290e7-115">Name</span></span></p></th>
<th><p><span data-ttu-id="290e7-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="290e7-116">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="290e7-117"><strong><a href="field-allowzerolength-property-dao.md">AllowZeroLength</a></strong></span><span class="sxs-lookup"><span data-stu-id="290e7-117"><strong><a href="field-allowzerolength-property-dao.md">AllowZeroLength</a></strong></span></span></p></td>
<td><p><span data-ttu-id="290e7-118">Define ou retorna um valor que indica se uma cadeia de caracteres de comprimento zero ( ) é uma configuração válida para a propriedade Value do objeto Field com um tipo de dados Texto ou Memorando (apenas espaços de trabalho do &quot; &quot; Microsoft Access). <strong><a href="field-value-property-dao.md"></a></strong> <strong><a href="field-object-dao.md"></a></strong></span><span class="sxs-lookup"><span data-stu-id="290e7-118">Sets or returns a value that indicates whether a zero-length string (&quot;&quot;) is a valid setting for the <strong><a href="field-value-property-dao.md">Value</a></strong> property of the <strong><a href="field-object-dao.md">Field</a></strong> object with a Text or Memo data type (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="290e7-119"><strong><a href="field-attributes-property-dao.md">Atributos</a></strong></span><span class="sxs-lookup"><span data-stu-id="290e7-119"><strong><a href="field-attributes-property-dao.md">Attributes</a></strong></span></span></p></td>
<td><p><span data-ttu-id="290e7-120">Define ou retorna um valor que indica uma ou mais características de um objeto <strong><a href="field-object-dao.md">Field</a></strong>.</span><span class="sxs-lookup"><span data-stu-id="290e7-120">Sets or returns a value that indicates one or more characteristics of a <strong><a href="field-object-dao.md">Field</a></strong> object.</span></span> <span data-ttu-id="290e7-121"><strong>Long</strong> de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="290e7-121">Read/write <strong>Long</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="290e7-122"><strong><a href="field-collatingorder-property-dao.md">CollatingOrder</a></strong></span><span class="sxs-lookup"><span data-stu-id="290e7-122"><strong><a href="field-collatingorder-property-dao.md">CollatingOrder</a></strong></span></span></p></td>
<td><p><span data-ttu-id="290e7-p102">Retorna um valor que especifica a sequência da ordem de classificação no texto para comparação ou classificação da sequência (apenas espaços de trabalho do Microsoft Access). <strong>Long</strong> somente leitura.</span><span class="sxs-lookup"><span data-stu-id="290e7-p102">Returns a value that specifies the sequence of the sort order in text for string comparison or sorting (Microsoft Access workspaces only). Read-only <strong>Long</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="290e7-125"><strong><a href="field-dataupdatable-property-dao.md">DataUpdatable</a></strong></span><span class="sxs-lookup"><span data-stu-id="290e7-125"><strong><a href="field-dataupdatable-property-dao.md">DataUpdatable</a></strong></span></span></p></td>
<td><p><span data-ttu-id="290e7-126">Retorna um valor que indica se os dados no campo representados por um objeto <strong><a href="field-object-dao.md">Field</a></strong> são atualizáveis.</span><span class="sxs-lookup"><span data-stu-id="290e7-126">Returns a value that indicates whether the data in the field represented by a <strong><a href="field-object-dao.md">Field</a></strong> object is updatable.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="290e7-127"><strong><a href="field-defaultvalue-property-dao.md">DefaultValue</a></strong></span><span class="sxs-lookup"><span data-stu-id="290e7-127"><strong><a href="field-defaultvalue-property-dao.md">DefaultValue</a></strong></span></span></p></td>
<td><p><span data-ttu-id="290e7-p103">Define ou retorna o valor padrão de um objeto <strong><a href="field-object-dao.md">Field</a></strong>. Para um objeto <strong>Field</strong> ainda não acrescentado à coleção <strong><a href="fields-collection-dao.md">Fields</a></strong>, essa propriedade é de leitura/gravação (apenas espaços de trabalho do Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="290e7-p103">Sets or returns the default value of a <strong><a href="field-object-dao.md">Field</a></strong> object. For a <strong>Field</strong> object not yet appended to the <strong><a href="fields-collection-dao.md">Fields</a></strong> collection, this property is read/write (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="290e7-130"><strong><a href="field-fieldsize-property-dao.md">FieldSize</a></strong></span><span class="sxs-lookup"><span data-stu-id="290e7-130"><strong><a href="field-fieldsize-property-dao.md">FieldSize</a></strong></span></span></p></td>
<td><p><span data-ttu-id="290e7-131">Retorna o número de bytes usado no banco de dados (em vez da memória) do objeto Memo ou Long Binary <strong><a href="field-object-dao.md">Field</a></strong> na coleção <strong><a href="fields-collection-dao.md">Fields</a></strong> de um objeto <strong><a href="recordset-object-dao.md">Recordset</a></strong>.</span><span class="sxs-lookup"><span data-stu-id="290e7-131">Returns the number of bytes used in the database (rather than in memory) of a Memo or Long Binary <strong><a href="field-object-dao.md">Field</a></strong> object in the <strong><a href="fields-collection-dao.md">Fields</a></strong> collection of a <strong><a href="recordset-object-dao.md">Recordset</a></strong> object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="290e7-132"><strong><a href="field-foreignname-property-dao.md">ForeignName</a></strong></span><span class="sxs-lookup"><span data-stu-id="290e7-132"><strong><a href="field-foreignname-property-dao.md">ForeignName</a></strong></span></span></p></td>
<td><p><span data-ttu-id="290e7-133">Define ou retorna um valor que especifica o nome do objeto <strong><a href="field-object-dao.md">Field</a></strong> em uma tabela externa que corresponde a um campo em uma tabela primária de uma relação (somente nos espaços de trabalho do Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="290e7-133">Sets or returns a value that specifies the name of the <strong><a href="field-object-dao.md">Field</a></strong> object in a foreign table that corresponds to a field in a primary table for a relationship (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="290e7-134"><strong><a href="field-name-property-dao.md">Name</a></strong></span><span class="sxs-lookup"><span data-stu-id="290e7-134"><strong><a href="field-name-property-dao.md">Name</a></strong></span></span></p></td>
<td><p><span data-ttu-id="290e7-p104">Retorna ou define o nome do objeto especificado. <strong>String</strong> de leitura/gravação se o objeto não foi acrescentado a uma coleção. <strong>String</strong> somente leitura se o objeto foi acrescentado a uma coleção.</span><span class="sxs-lookup"><span data-stu-id="290e7-p104">Returns or sets the name of the specified object. Read/write <strong>String</strong> if the object has not been appended to a collection. Read-only <strong>String</strong> if the object has been appended to a collection.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="290e7-138"><strong><a href="field-ordinalposition-property-dao.md">OrdinalPosition</a></strong></span><span class="sxs-lookup"><span data-stu-id="290e7-138"><strong><a href="field-ordinalposition-property-dao.md">OrdinalPosition</a></strong></span></span></p></td>
<td><p><span data-ttu-id="290e7-139">Define ou retorna a posição relativa de um <strong><a href="field-object-dao.md">objeto Field</a></strong> dentro de uma <strong><a href="fields-collection-dao.md">coleção Fields</a></strong> .</span><span class="sxs-lookup"><span data-stu-id="290e7-139">Sets or returns the relative position of a <strong><a href="field-object-dao.md">Field</a></strong> object within a <strong><a href="fields-collection-dao.md">Fields</a></strong> collection.</span></span> <span data-ttu-id="290e7-140">.</span><span class="sxs-lookup"><span data-stu-id="290e7-140">.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="290e7-141"><strong><a href="field-originalvalue-property-dao.md">OriginalValue</a></strong></span><span class="sxs-lookup"><span data-stu-id="290e7-141"><strong><a href="field-originalvalue-property-dao.md">OriginalValue</a></strong></span></span></p></td>
<td><p><span data-ttu-id="290e7-142">Um dos <strong><a href="workspacetypeenum-enumeration-dao.md">valores de WorkspaceTypeEnum.</a></strong></span><span class="sxs-lookup"><span data-stu-id="290e7-142">One of the <strong><a href="workspacetypeenum-enumeration-dao.md">WorkspaceTypeEnum</a></strong> values.</span></span></p>
<td><p><span data-ttu-id="290e7-143"><strong>OBSERVAÇÃO</strong>: o Microsoft Access 2013 não oferece suporte para espaços de trabalho ODBCDirect.</span><span class="sxs-lookup"><span data-stu-id="290e7-143"><strong>NOTE</strong>: ODBCDirect workspaces are not supported in Microsoft Access 2013.</span></span> <span data-ttu-id="290e7-144">Use o ADO para acessar fontes de dados externas sem usar o mecanismo de banco de dados do Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="290e7-144">Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span></p>
<p><span data-ttu-id="290e7-145">Retorna o valor de um <strong>Field</strong> no banco de dados existente quando começou a última atualização em lotes (somente nos espaços de trabalho ODBCDirect).</span><span class="sxs-lookup"><span data-stu-id="290e7-145">Returns the value of a <strong>Field</strong> in the database that existed when the last batch update began (ODBCDirect workspaces only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="290e7-146"><strong><a href="field-properties-property-dao.md">Properties</a></strong></span><span class="sxs-lookup"><span data-stu-id="290e7-146"><strong><a href="field-properties-property-dao.md">Properties</a></strong></span></span></p></td>
<td><p><span data-ttu-id="290e7-147">Retorna a coleção <strong><a href="properties-collection-dao.md">Properties</a></strong> do objeto especificado.</span><span class="sxs-lookup"><span data-stu-id="290e7-147">Returns the <strong><a href="properties-collection-dao.md">Properties</a></strong> collection of the specified object.</span></span> <span data-ttu-id="290e7-148">Somente leitura.</span><span class="sxs-lookup"><span data-stu-id="290e7-148">Read-only.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="290e7-149"><strong><a href="field-required-property-dao.md">Obrigatório</a></strong></span><span class="sxs-lookup"><span data-stu-id="290e7-149"><strong><a href="field-required-property-dao.md">Required</a></strong></span></span></p></td>
<td><p><span data-ttu-id="290e7-150">Define ou retorna um valor que indica se um objeto <strong><a href="field-object-dao.md">Field</a></strong> requer um valor não Null.</span><span class="sxs-lookup"><span data-stu-id="290e7-150">Sets or returns a value that indicates whether a <strong><a href="field-object-dao.md">Field</a></strong> object requires a non-Null value.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="290e7-151"><strong><a href="field-fieldsize-property-dao.md">Tamanho</a></strong></span><span class="sxs-lookup"><span data-stu-id="290e7-151"><strong><a href="field-fieldsize-property-dao.md">Size</a></strong></span></span></p></td>
<td><p><span data-ttu-id="290e7-152">Retorna o número de bytes usado no banco de dados (em vez da memória) do objeto Memo ou Long Binary <strong><a href="field-object-dao.md">Field</a></strong> na coleção <strong><a href="fields-collection-dao.md">Fields</a></strong> de um objeto <strong><a href="recordset-object-dao.md">Recordset</a></strong>.</span><span class="sxs-lookup"><span data-stu-id="290e7-152">Returns the number of bytes used in the database (rather than in memory) of a Memo or Long Binary <strong><a href="field-object-dao.md">Field</a></strong> object in the <strong><a href="fields-collection-dao.md">Fields</a></strong> collection of a <strong><a href="recordset-object-dao.md">Recordset</a></strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="290e7-153"><strong><a href="field-sourcefield-property-dao.md">SourceField</a></strong></span><span class="sxs-lookup"><span data-stu-id="290e7-153"><strong><a href="field-sourcefield-property-dao.md">SourceField</a></strong></span></span></p></td>
<td><p><span data-ttu-id="290e7-p108">Retorna um valor que indica o nome do campo que é a fonte de dados original de um objeto <strong>Field</strong>. <strong>String</strong> somente leitura.</span><span class="sxs-lookup"><span data-stu-id="290e7-p108">Returns a value that indicates the name of the field that is the original source of the data for a <strong>Field</strong> object. Read-only <strong>String</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="290e7-156"><strong><a href="field-sourcetable-property-dao.md">SourceTable</a></strong></span><span class="sxs-lookup"><span data-stu-id="290e7-156"><strong><a href="field-sourcetable-property-dao.md">SourceTable</a></strong></span></span></p></td>
<td><p><span data-ttu-id="290e7-p109">Retorna um valor que indica o nome da tabela que é a fonte de dados original de um objeto <strong>Field</strong>. <strong>String</strong> somente leitura.</span><span class="sxs-lookup"><span data-stu-id="290e7-p109">Returns a value that indicates the name of the table that is the original source of the data for a <strong>Field</strong> object. Read-only <strong>String</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="290e7-159"><strong><a href="field-type-property-dao.md">Tipo</a></strong></span><span class="sxs-lookup"><span data-stu-id="290e7-159"><strong><a href="field-type-property-dao.md">Type</a></strong></span></span></p></td>
<td><p><span data-ttu-id="290e7-160">Define ou retorna um valor que indica o tipo operacional ou o tipo de dados de um objeto.</span><span class="sxs-lookup"><span data-stu-id="290e7-160">Sets or returns a value that indicates the operational type or data type of an object.</span></span> <span data-ttu-id="290e7-161"><strong>número inteiro</strong> de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="290e7-161">Read/write <strong>Integer</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="290e7-162"><strong><a href="field-validateonset-property-dao.md">ValidateOnSet</a></strong></span><span class="sxs-lookup"><span data-stu-id="290e7-162"><strong><a href="field-validateonset-property-dao.md">ValidateOnSet</a></strong></span></span></p></td>
<td><p><span data-ttu-id="290e7-163">Define ou retorna um valor que especifica ou não se o valor de um objeto <strong><a href="field-object-dao.md">Field</a></strong> será imediatamente validado quando a propriedade <strong><a href="field-value-property-dao.md">Value</a></strong> do objeto será definida (somente em espaços de trabalho Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="290e7-163">Sets or returns a value that specifies whether or not the value of a <strong><a href="field-object-dao.md">Field</a></strong> object is immediately validated when the object's <strong><a href="field-value-property-dao.md">Value</a></strong> property is set (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="290e7-164"><strong><a href="field-validationrule-property-dao.md">ValidationRule</a></strong></span><span class="sxs-lookup"><span data-stu-id="290e7-164"><strong><a href="field-validationrule-property-dao.md">ValidationRule</a></strong></span></span></p></td>
<td><p><span data-ttu-id="290e7-p111">Define ou retorna um valor que valida os dados em um campo, conforme ele é alterado ou adicionado a uma tabela (apenas espaços de trabalho do Microsoft Access). <strong>String</strong> de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="290e7-p111">Sets or returns a value that validates the data in a field as it's changed or added to a table (Microsoft Access workspaces only). Read/write <strong>String</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="290e7-167"><strong><a href="field-validationtext-property-dao.md">ValidationText</a></strong></span><span class="sxs-lookup"><span data-stu-id="290e7-167"><strong><a href="field-validationtext-property-dao.md">ValidationText</a></strong></span></span></p></td>
<td><p><span data-ttu-id="290e7-p112">Define ou retorna um valor que especifica o texto da mensagem exibido pelo aplicativo, caso o valor de um objeto <strong>Field</strong> não satisfaça a regra de validação especificada pela definição da propriedade <strong>ValidationRule</strong> (somente nos espaços de trabalho do Microsoft Access). <strong>String</strong> de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="290e7-p112">Sets or returns a value that specifies the text of the message that your application displays if the value of a <strong>Field</strong> object doesn't satisfy the validation rule specified by the <strong>ValidationRule</strong> property setting (Microsoft Access workspaces only). Read/write <strong>String</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="290e7-170"><strong><a href="field-value-property-dao.md">Valor</a></strong></span><span class="sxs-lookup"><span data-stu-id="290e7-170"><strong><a href="field-value-property-dao.md">Value</a></strong></span></span></p></td>
<td><p><span data-ttu-id="290e7-171">Define ou retorna o valor de um objeto.</span><span class="sxs-lookup"><span data-stu-id="290e7-171">Sets or returns the value of an object.</span></span> <span data-ttu-id="290e7-172"><strong>Variant</strong> de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="290e7-172">Read/write <strong>Variant</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="290e7-173"><strong><a href="field-visiblevalue-property-dao.md">VisibleValue</a></strong></span><span class="sxs-lookup"><span data-stu-id="290e7-173"><strong><a href="field-visiblevalue-property-dao.md">VisibleValue</a></strong></span></span></p></td>
<td><p><span data-ttu-id="290e7-174">Um dos <strong><a href="workspacetypeenum-enumeration-dao.md">valores de WorkspaceTypeEnum.</a></strong></span><span class="sxs-lookup"><span data-stu-id="290e7-174">One of the <strong><a href="workspacetypeenum-enumeration-dao.md">WorkspaceTypeEnum</a></strong> values.</span></span></p>
<td><p><span data-ttu-id="290e7-175"><strong>OBSERVAÇÃO</strong>: o Microsoft Access 2013 não oferece suporte para espaços de trabalho ODBCDirect.</span><span class="sxs-lookup"><span data-stu-id="290e7-175"><strong>NOTE</strong>: ODBCDirect workspaces are not supported in Microsoft Access 2013.</span></span> <span data-ttu-id="290e7-176">Use o ADO para acessar fontes de dados externas sem usar o mecanismo de banco de dados do Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="290e7-176">Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span></p>
<p><span data-ttu-id="290e7-177">Retorna um valor atualmente no banco de dados mais recente que a propriedade <strong>OriginalValue</strong> como determinado pelo conflito de atualização em lotes (somente nos espaços de trabalho do ODBCDirect).</span><span class="sxs-lookup"><span data-stu-id="290e7-177">Returns a value currently in the database that is newer than the <strong>OriginalValue</strong> property as determined by a batch update conflict (ODBCDirect workspaces only).</span></span></p></td>
</tr>
</tbody>
</table>

