---
title: Membros do campo (DAO)
TOCTitle: Field Members
ms:assetid: 4b6a587f-1fd0-37fb-db7d-75b587a8dc60
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193511(v=office.15)
ms:contentKeyID: 48544689
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 1a0e448662384572163fca074e554a5e30be30a7
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28703598"
---
# <a name="field-members-dao"></a><span data-ttu-id="01048-102">Membros do campo (DAO)</span><span class="sxs-lookup"><span data-stu-id="01048-102">Field members (DAO)</span></span>


<span data-ttu-id="01048-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="01048-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="01048-104">Um objeto Field representa uma coluna de dados com um tipo de dados comum e um conjunto comum de propriedades.</span><span class="sxs-lookup"><span data-stu-id="01048-104">A Field object represents a column of data with a common data type and a common set of properties.</span></span>

## <a name="methods"></a><span data-ttu-id="01048-105">Métodos</span><span class="sxs-lookup"><span data-stu-id="01048-105">Methods</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="01048-106">Nome</span><span class="sxs-lookup"><span data-stu-id="01048-106">Name</span></span></p></th>
<th><p><span data-ttu-id="01048-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="01048-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="01048-108"><strong><a href="field-appendchunk-method-dao.md">AppendChunk</a></strong></span><span class="sxs-lookup"><span data-stu-id="01048-108"><strong><a href="field-appendchunk-method-dao.md">AppendChunk</a></strong></span></span></p></td>
<td><p><span data-ttu-id="01048-109">Acrescenta dados de uma expressão de cadeia de caracteres a um objeto <strong><a href="field-object-dao.md">Field</a></strong> Memo ou Long Binary em um <strong><a href="recordset-object-dao.md">Recordset</a></strong>.</span><span class="sxs-lookup"><span data-stu-id="01048-109">Appends data from a string expression to a Memo or Long Binary <strong><a href="field-object-dao.md">Field</a></strong> object in a <strong><a href="recordset-object-dao.md">Recordset</a></strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="01048-110"><strong><a href="field-createproperty-method-dao.md">CreateProperty</a></strong></span><span class="sxs-lookup"><span data-stu-id="01048-110"><strong><a href="field-createproperty-method-dao.md">CreateProperty</a></strong></span></span></p></td>
<td><p><span data-ttu-id="01048-111">Cria um novo objeto <strong><a href="property-object-dao.md">Property</a></strong> definido pelo usuário (somente espaços de trabalho do Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="01048-111">Creates a new user-defined <strong><a href="property-object-dao.md">Property</a></strong> object (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="01048-112"><strong><a href="field-getchunk-method-dao.md">GetChunk</a></strong></span><span class="sxs-lookup"><span data-stu-id="01048-112"><strong><a href="field-getchunk-method-dao.md">GetChunk</a></strong></span></span></p></td>
<td><p><span data-ttu-id="01048-113">Retorna o conteúdo no todo ou em parte de um objeto <strong><strong>Field</strong></strong> <a href="field-object-dao.md">Memo</a> ou <strong>Long Binary</strong> na coleção <strong><a href="fields-collection-dao.md">Fields</a></strong> de um objeto <strong><a href="recordset-object-dao.md">Recordset</a></strong>.</span><span class="sxs-lookup"><span data-stu-id="01048-113">Returns all or a portion of the contents of a <strong>Memo</strong> or <strong>Long Binary</strong> <strong><a href="field-object-dao.md">Field</a></strong> object in the <strong><a href="fields-collection-dao.md">Fields</a></strong> collection of a <strong><a href="recordset-object-dao.md">Recordset</a></strong> object.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="properties"></a><span data-ttu-id="01048-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="01048-114">Properties</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="01048-115">Nome</span><span class="sxs-lookup"><span data-stu-id="01048-115">Name</span></span></p></th>
<th><p><span data-ttu-id="01048-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="01048-116">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="01048-117"><strong><a href="field-allowzerolength-property-dao.md">AllowZeroLength</a></strong></span><span class="sxs-lookup"><span data-stu-id="01048-117"><strong><a href="field-allowzerolength-property-dao.md">AllowZeroLength</a></strong></span></span></p></td>
<td><p><span data-ttu-id="01048-118">Define ou retorna um valor que indica se uma cadeia de caracteres de comprimento zero (&quot;&quot;) é uma configuração válida para a propriedade <strong><a href="field-value-property-dao.md">Value</a></strong> do objeto <strong><a href="field-object-dao.md">Field</a></strong> com um tipo de dados texto ou memorando (somente espaços de trabalho do Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="01048-118">Sets or returns a value that indicates whether a zero-length string (&quot;&quot;) is a valid setting for the <strong><a href="field-value-property-dao.md">Value</a></strong> property of the <strong><a href="field-object-dao.md">Field</a></strong> object with a Text or Memo data type (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="01048-119"><strong><a href="field-attributes-property-dao.md">Atributos</a></strong></span><span class="sxs-lookup"><span data-stu-id="01048-119"><strong><a href="field-attributes-property-dao.md">Attributes</a></strong></span></span></p></td>
<td><p><span data-ttu-id="01048-p101">Define ou retorna um valor que indica uma ou mais características de um objeto <strong><a href="field-object-dao.md">Field</a></strong>. <strong>Long</strong> de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="01048-p101">Sets or returns a value that indicates one or more characteristics of a <strong><a href="field-object-dao.md">Field</a></strong> object. Read/write <strong>Long</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="01048-122"><strong><a href="field-collatingorder-property-dao.md">CollatingOrder</a></strong></span><span class="sxs-lookup"><span data-stu-id="01048-122"><strong><a href="field-collatingorder-property-dao.md">CollatingOrder</a></strong></span></span></p></td>
<td><p><span data-ttu-id="01048-p102">Retorna um valor que especifica a sequência da ordem de classificação no texto para comparação ou classificação da sequência (apenas espaços de trabalho do Microsoft Access). <strong>Long</strong> somente leitura.</span><span class="sxs-lookup"><span data-stu-id="01048-p102">Returns a value that specifies the sequence of the sort order in text for string comparison or sorting (Microsoft Access workspaces only). Read-only <strong>Long</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="01048-125"><strong><a href="field-dataupdatable-property-dao.md">DataUpdatable</a></strong></span><span class="sxs-lookup"><span data-stu-id="01048-125"><strong><a href="field-dataupdatable-property-dao.md">DataUpdatable</a></strong></span></span></p></td>
<td><p><span data-ttu-id="01048-126">Retorna um valor que indica se os dados no campo representados por um objeto <strong><a href="field-object-dao.md">Field</a></strong> são atualizáveis.</span><span class="sxs-lookup"><span data-stu-id="01048-126">Returns a value that indicates whether the data in the field represented by a <strong><a href="field-object-dao.md">Field</a></strong> object is updatable.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="01048-127"><strong><a href="field-defaultvalue-property-dao.md">DefaultValue</a></strong></span><span class="sxs-lookup"><span data-stu-id="01048-127"><strong><a href="field-defaultvalue-property-dao.md">DefaultValue</a></strong></span></span></p></td>
<td><p><span data-ttu-id="01048-p103">Define ou retorna o valor padrão de um objeto <strong><a href="field-object-dao.md">Field</a></strong>. Para um objeto <strong>Field</strong> ainda não acrescentado à coleção <strong><a href="fields-collection-dao.md">Fields</a></strong>, essa propriedade é de leitura/gravação (apenas espaços de trabalho do Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="01048-p103">Sets or returns the default value of a <strong><a href="field-object-dao.md">Field</a></strong> object. For a <strong>Field</strong> object not yet appended to the <strong><a href="fields-collection-dao.md">Fields</a></strong> collection, this property is read/write (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="01048-130"><strong><a href="field-fieldsize-property-dao.md">Tamanho do campo</a></strong></span><span class="sxs-lookup"><span data-stu-id="01048-130"><strong><a href="field-fieldsize-property-dao.md">FieldSize</a></strong></span></span></p></td>
<td><p><span data-ttu-id="01048-131">Retorna o número de bytes usado no banco de dados (em vez da memória) do objeto Memo ou Long Binary <strong><a href="field-object-dao.md">Field</a></strong> na coleção <strong><a href="fields-collection-dao.md">Fields</a></strong> de um objeto <strong><a href="recordset-object-dao.md">Recordset</a></strong>.</span><span class="sxs-lookup"><span data-stu-id="01048-131">Returns the number of bytes used in the database (rather than in memory) of a Memo or Long Binary <strong><a href="field-object-dao.md">Field</a></strong> object in the <strong><a href="fields-collection-dao.md">Fields</a></strong> collection of a <strong><a href="recordset-object-dao.md">Recordset</a></strong> object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="01048-132"><strong><a href="field-foreignname-property-dao.md">ForeignName</a></strong></span><span class="sxs-lookup"><span data-stu-id="01048-132"><strong><a href="field-foreignname-property-dao.md">ForeignName</a></strong></span></span></p></td>
<td><p><span data-ttu-id="01048-133">Define ou retorna um valor que especifica o nome do objeto <strong><a href="field-object-dao.md">Field</a></strong> em uma tabela externa que corresponde a um campo em uma tabela primária de uma relação (somente nos espaços de trabalho do Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="01048-133">Sets or returns a value that specifies the name of the <strong><a href="field-object-dao.md">Field</a></strong> object in a foreign table that corresponds to a field in a primary table for a relationship (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="01048-134"><strong><a href="field-name-property-dao.md">Name</a></strong></span><span class="sxs-lookup"><span data-stu-id="01048-134"><strong><a href="field-name-property-dao.md">Name</a></strong></span></span></p></td>
<td><p><span data-ttu-id="01048-p104">Retorna ou define o nome do objeto especificado. <strong>String</strong> de leitura/gravação se o objeto não foi acrescentado a uma coleção. <strong>String</strong> somente leitura se o objeto foi acrescentado a uma coleção.</span><span class="sxs-lookup"><span data-stu-id="01048-p104">Returns or sets the name of the specified object. Read/write <strong>String</strong> if the object has not been appended to a collection. Read-only <strong>String</strong> if the object has been appended to a collection.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="01048-138"><strong><a href="field-ordinalposition-property-dao.md">OrdinalPosition</a></strong></span><span class="sxs-lookup"><span data-stu-id="01048-138"><strong><a href="field-ordinalposition-property-dao.md">OrdinalPosition</a></strong></span></span></p></td>
<td><p><span data-ttu-id="01048-p105">Define ou retorna a posição relativa de um objeto <strong><a href="field-object-dao.md">Field</a></strong> em uma coleção <strong><a href="fields-collection-dao.md">Fields</a></strong>.</span><span class="sxs-lookup"><span data-stu-id="01048-p105">Sets or returns the relative position of a <strong><a href="field-object-dao.md">Field</a></strong> object within a <strong><a href="fields-collection-dao.md">Fields</a></strong> collection. .</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="01048-141"><strong><a href="field-originalvalue-property-dao.md">OriginalValue</a></strong></span><span class="sxs-lookup"><span data-stu-id="01048-141"><strong><a href="field-originalvalue-property-dao.md">OriginalValue</a></strong></span></span></p></td>
<td><p><span data-ttu-id="01048-142">Um dos valores <strong><a href="workspacetypeenum-enumeration-dao.md">WorkspaceTypeEnum</a></strong> .</span><span class="sxs-lookup"><span data-stu-id="01048-142">One of the <strong><a href="workspacetypeenum-enumeration-dao.md">WorkspaceTypeEnum</a></strong> values.</span></span></p>
<td><p><span data-ttu-id="01048-143"><strong>Observação</strong>: não há suporte para os espaços de trabalho ODBCDirect no Microsoft Access 2013.</span><span class="sxs-lookup"><span data-stu-id="01048-143"><strong>NOTE</strong>: ODBCDirect workspaces are not supported in Microsoft Access 2013.</span></span> <span data-ttu-id="01048-144">Use o ADO se você quiser acessar fontes de dado externas sem usar o mecanismo de banco de dados do Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="01048-144">Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span></p>
<p><span data-ttu-id="01048-145">Retorna o valor de um <strong>Field</strong> no banco de dados existente quando começou a última atualização em lotes (somente nos espaços de trabalho ODBCDirect).</span><span class="sxs-lookup"><span data-stu-id="01048-145">Returns the value of a <strong>Field</strong> in the database that existed when the last batch update began (ODBCDirect workspaces only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="01048-146"><strong><a href="field-properties-property-dao.md">Propriedades</a></strong></span><span class="sxs-lookup"><span data-stu-id="01048-146"><strong><a href="field-properties-property-dao.md">Properties</a></strong></span></span></p></td>
<td><p><span data-ttu-id="01048-p107">Retorna a coleção <strong><a href="properties-collection-dao.md">Properties</a></strong> do objeto especificado. Somente leitura.</span><span class="sxs-lookup"><span data-stu-id="01048-p107">Returns the <strong><a href="properties-collection-dao.md">Properties</a></strong> collection of the specified object. Read-only.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="01048-149"><strong><a href="field-required-property-dao.md">Necessário</a></strong></span><span class="sxs-lookup"><span data-stu-id="01048-149"><strong><a href="field-required-property-dao.md">Required</a></strong></span></span></p></td>
<td><p><span data-ttu-id="01048-150">Define ou retorna um valor que indica se um objeto <strong><a href="field-object-dao.md">Field</a></strong> requer um valor não Null.</span><span class="sxs-lookup"><span data-stu-id="01048-150">Sets or returns a value that indicates whether a <strong><a href="field-object-dao.md">Field</a></strong> object requires a non-Null value.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="01048-151"><strong><a href="field-fieldsize-property-dao.md">Tamanho</a></strong></span><span class="sxs-lookup"><span data-stu-id="01048-151"><strong><a href="field-fieldsize-property-dao.md">Size</a></strong></span></span></p></td>
<td><p><span data-ttu-id="01048-152">Retorna o número de bytes usado no banco de dados (em vez da memória) do objeto Memo ou Long Binary <strong><a href="field-object-dao.md">Field</a></strong> na coleção <strong><a href="fields-collection-dao.md">Fields</a></strong> de um objeto <strong><a href="recordset-object-dao.md">Recordset</a></strong>.</span><span class="sxs-lookup"><span data-stu-id="01048-152">Returns the number of bytes used in the database (rather than in memory) of a Memo or Long Binary <strong><a href="field-object-dao.md">Field</a></strong> object in the <strong><a href="fields-collection-dao.md">Fields</a></strong> collection of a <strong><a href="recordset-object-dao.md">Recordset</a></strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="01048-153"><strong><a href="field-sourcefield-property-dao.md">SourceField</a></strong></span><span class="sxs-lookup"><span data-stu-id="01048-153"><strong><a href="field-sourcefield-property-dao.md">SourceField</a></strong></span></span></p></td>
<td><p><span data-ttu-id="01048-p108">Retorna um valor que indica o nome do campo que é a fonte de dados original de um objeto <strong>Field</strong>. <strong>String</strong> somente leitura.</span><span class="sxs-lookup"><span data-stu-id="01048-p108">Returns a value that indicates the name of the field that is the original source of the data for a <strong>Field</strong> object. Read-only <strong>String</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="01048-156"><strong><a href="field-sourcetable-property-dao.md">SourceTable</a></strong></span><span class="sxs-lookup"><span data-stu-id="01048-156"><strong><a href="field-sourcetable-property-dao.md">SourceTable</a></strong></span></span></p></td>
<td><p><span data-ttu-id="01048-p109">Retorna um valor que indica o nome da tabela que é a fonte de dados original de um objeto <strong>Field</strong>. <strong>String</strong> somente leitura.</span><span class="sxs-lookup"><span data-stu-id="01048-p109">Returns a value that indicates the name of the table that is the original source of the data for a <strong>Field</strong> object. Read-only <strong>String</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="01048-159"><strong><a href="field-type-property-dao.md">Tipo</a></strong></span><span class="sxs-lookup"><span data-stu-id="01048-159"><strong><a href="field-type-property-dao.md">Type</a></strong></span></span></p></td>
<td><p><span data-ttu-id="01048-p110">Define ou retorna um valor que indica o tipo operacional ou o tipo de dados de um objeto. <strong>Integer</strong> de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="01048-p110">Sets or returns a value that indicates the operational type or data type of an object. Read/write <strong>Integer</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="01048-162"><strong><a href="field-validateonset-property-dao.md">ValidateOnSet</a></strong></span><span class="sxs-lookup"><span data-stu-id="01048-162"><strong><a href="field-validateonset-property-dao.md">ValidateOnSet</a></strong></span></span></p></td>
<td><p><span data-ttu-id="01048-163">Define ou retorna um valor que especifica ou não se o valor de um objeto <strong><a href="field-object-dao.md">Field</a></strong> será imediatamente validado quando a propriedade <strong><a href="field-value-property-dao.md">Value</a></strong> do objeto será definida (somente em espaços de trabalho Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="01048-163">Sets or returns a value that specifies whether or not the value of a <strong><a href="field-object-dao.md">Field</a></strong> object is immediately validated when the object's <strong><a href="field-value-property-dao.md">Value</a></strong> property is set (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="01048-164"><strong><a href="field-validationrule-property-dao.md">ValidationRule</a></strong></span><span class="sxs-lookup"><span data-stu-id="01048-164"><strong><a href="field-validationrule-property-dao.md">ValidationRule</a></strong></span></span></p></td>
<td><p><span data-ttu-id="01048-p111">Define ou retorna um valor que valida os dados em um campo à medida que estes são alterados ou adicionados a uma tabela (somente em espaços de trabalho do Microsoft Access). <strong>String</strong> de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="01048-p111">Sets or returns a value that validates the data in a field as it's changed or added to a table (Microsoft Access workspaces only). Read/write <strong>String</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="01048-167"><strong><a href="field-validationtext-property-dao.md">ValidationText</a></strong></span><span class="sxs-lookup"><span data-stu-id="01048-167"><strong><a href="field-validationtext-property-dao.md">ValidationText</a></strong></span></span></p></td>
<td><p><span data-ttu-id="01048-p112">Define ou retorna um valor que especifica o texto da mensagem exibido pelo aplicativo, caso o valor de um objeto <strong>Field</strong> não satisfaça a regra de validação especificada pela definição da propriedade <strong>ValidationRule</strong> (somente nos espaços de trabalho do Microsoft Access). <strong>String</strong> de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="01048-p112">Sets or returns a value that specifies the text of the message that your application displays if the value of a <strong>Field</strong> object doesn't satisfy the validation rule specified by the <strong>ValidationRule</strong> property setting (Microsoft Access workspaces only). Read/write <strong>String</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="01048-170"><strong><a href="field-value-property-dao.md">Valor</a></strong></span><span class="sxs-lookup"><span data-stu-id="01048-170"><strong><a href="field-value-property-dao.md">Value</a></strong></span></span></p></td>
<td><p><span data-ttu-id="01048-p113">Define ou retorna o valor de um objeto. <strong>Variant</strong> de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="01048-p113">Sets or returns the value of an object. Read/write <strong>Variant</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="01048-173"><strong><a href="field-visiblevalue-property-dao.md">VisibleValue</a></strong></span><span class="sxs-lookup"><span data-stu-id="01048-173"><strong><a href="field-visiblevalue-property-dao.md">VisibleValue</a></strong></span></span></p></td>
<td><p><span data-ttu-id="01048-174">Um dos valores <strong><a href="workspacetypeenum-enumeration-dao.md">WorkspaceTypeEnum</a></strong> .</span><span class="sxs-lookup"><span data-stu-id="01048-174">One of the <strong><a href="workspacetypeenum-enumeration-dao.md">WorkspaceTypeEnum</a></strong> values.</span></span></p>
<td><p><span data-ttu-id="01048-175"><strong>Observação</strong>: não há suporte para os espaços de trabalho ODBCDirect no Microsoft Access 2013.</span><span class="sxs-lookup"><span data-stu-id="01048-175"><strong>NOTE</strong>: ODBCDirect workspaces are not supported in Microsoft Access 2013.</span></span> <span data-ttu-id="01048-176">Use o ADO se você quiser acessar fontes de dado externas sem usar o mecanismo de banco de dados do Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="01048-176">Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span></p>
<p><span data-ttu-id="01048-177">Retorna um valor atualmente no banco de dados mais recente que a propriedade <strong>OriginalValue</strong> como determinado pelo conflito de atualização em lotes (somente nos espaços de trabalho do ODBCDirect).</span><span class="sxs-lookup"><span data-stu-id="01048-177">Returns a value currently in the database that is newer than the <strong>OriginalValue</strong> property as determined by a batch update conflict (ODBCDirect workspaces only).</span></span></p></td>
</tr>
</tbody>
</table>

