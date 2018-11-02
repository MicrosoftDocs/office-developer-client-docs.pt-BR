---
title: Bloco de dados Pesquisarregistro
TOCTitle: LookupRecord data block
ms:assetid: 750dc8ca-3bab-c3d1-c91d-2196f9c0604d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195882(v=office.15)
ms:contentKeyID: 48545671
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: d53bb8b6e4520810b98bfe81c9d35186a2392904
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25928590"
---
# <a name="lookuprecord-data-block"></a><span data-ttu-id="31760-102">Bloco de dados Pesquisarregistro</span><span class="sxs-lookup"><span data-stu-id="31760-102">LookupRecord data block</span></span>

<span data-ttu-id="31760-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="31760-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="31760-104">Um bloco de dados **PesquisarRegistro** executa um conjunto de ações em um registro específico.</span><span class="sxs-lookup"><span data-stu-id="31760-104">A **LookupRecord** data block performs a set of actions on a specific record.</span></span>

> [!NOTE]
> <span data-ttu-id="31760-105">[!OBSERVAçãO] O bloco de dados **PesquisarRegistro** está disponível somente em Macros de Dados.</span><span class="sxs-lookup"><span data-stu-id="31760-105">The **LookupRecord** data block is available only in Data Macros.</span></span>

## <a name="setting"></a><span data-ttu-id="31760-106">Configuração</span><span class="sxs-lookup"><span data-stu-id="31760-106">Setting</span></span>

<span data-ttu-id="31760-107">A ação **PesquisarRegistro** tem os seguintes argumentos.</span><span class="sxs-lookup"><span data-stu-id="31760-107">The **SetField** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="31760-108">Argumento</span><span class="sxs-lookup"><span data-stu-id="31760-108">Argument</span></span></p></th>
<th><p><span data-ttu-id="31760-109">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="31760-109">Required</span></span></p></th>
<th><p><span data-ttu-id="31760-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="31760-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="31760-111">Em</span><span class="sxs-lookup"><span data-stu-id="31760-111">In</span></span></p></td>
<td><p><span data-ttu-id="31760-112">Sim</span><span class="sxs-lookup"><span data-stu-id="31760-112">Yes</span></span></p></td>
<td><p><span data-ttu-id="31760-113">Uma cadeia de caracteres que identifica o registro para operar em.</span><span class="sxs-lookup"><span data-stu-id="31760-113">A string that identifies the record to operate on.</span></span> <span data-ttu-id="31760-114">O argumento <em>em</em> pode conter o nome da tabela, uma consulta seleção ou uma instrução SQL.</span><span class="sxs-lookup"><span data-stu-id="31760-114">The <em>In</em> argument can contain the name of the table, a select query, or a SQL statement.</span></span></p>

> [!NOTE]
> <span data-ttu-id="31760-115">O registro especificado não pode incluir dados armazenados em uma tabela vinculada ou fonte de dados ODBC.</span><span class="sxs-lookup"><span data-stu-id="31760-115">The specified record cannot include data stored in a linked table or ODBC data source.</span></span>


<p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="31760-116">Condição Where</span><span class="sxs-lookup"><span data-stu-id="31760-116">Where Condition</span></span></p></td>
<td><p><span data-ttu-id="31760-117">Não</span><span class="sxs-lookup"><span data-stu-id="31760-117">No</span></span></p></td>
<td><p><span data-ttu-id="31760-118">Uma expressão de cadeia de caracteres usada para restringir o intervalo de dados no qual o bloco de dados <strong>Pesquisarregistro</strong> é executada.</span><span class="sxs-lookup"><span data-stu-id="31760-118">A string expression used to restrict the range of data on which the <strong>LookupRecord</strong> data block is performed.</span></span> <span data-ttu-id="31760-119">Por exemplo, critérios costumam ser equivalentes à cláusula WHERE em uma expressão SQL, sem a palavra onde.</span><span class="sxs-lookup"><span data-stu-id="31760-119">For example, criteria are often equivalent to the WHERE clause in an SQL expression, without the word WHERE.</span></span> <span data-ttu-id="31760-120">Se os critérios forem omitidos, o bloco de dados <strong>Pesquisarregistro</strong> opera em todo o domínio especificado pelo argumento <em>em</em> .</span><span class="sxs-lookup"><span data-stu-id="31760-120">If criteria are omitted, the <strong>LookupRecord</strong> data block operates on the entire domain specified by the <em>In</em> argument.</span></span> <span data-ttu-id="31760-121">Qualquer campo que está incluído nos critérios também deve ser um campo no <em>In</em>.</span><span class="sxs-lookup"><span data-stu-id="31760-121">Any field that is included in criteria must also be a field in <em>In</em>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="31760-122">Alias</span><span class="sxs-lookup"><span data-stu-id="31760-122">Alias</span></span></p></td>
<td><p><span data-ttu-id="31760-123">Não</span><span class="sxs-lookup"><span data-stu-id="31760-123">No</span></span></p></td>
<td><p><span data-ttu-id="31760-124">Uma cadeia de caracteres que fornece um nome alternativo para o registro especificado pelo argumento <em>em</em> .</span><span class="sxs-lookup"><span data-stu-id="31760-124">A string that provides an alternative name for the record specified by the <em>In</em> argument.</span></span> <span data-ttu-id="31760-125">Frequentemente usado para reduzir o nome da tabela referências posteriores evitar possíveis referências ambíguas.</span><span class="sxs-lookup"><span data-stu-id="31760-125">Often used to shorten the table name for subsequent references to prevent possible ambiguous references.</span></span> <span data-ttu-id="31760-126">Se o <em>Alias</em> não for especificado, o nome da tabela ou da consulta será usado como o alias.</span><span class="sxs-lookup"><span data-stu-id="31760-126">If <em>Alias</em> is not specified, the table or query name will be used as the alias.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="31760-127">Comentários</span><span class="sxs-lookup"><span data-stu-id="31760-127">Remarks</span></span>

<span data-ttu-id="31760-128">Se os critérios especificados pelos argumentos *no* e a *Condição Where* especifica mais de um registro, o bloco de dados **Pesquisarregistro** funcionará apenas no primeiro registro.</span><span class="sxs-lookup"><span data-stu-id="31760-128">If the criteria specified by the *In* and *Where Condition* arguments specifies more than one record, the **LookupRecord** data block will operate only on the first record.</span></span>

## <a name="example"></a><span data-ttu-id="31760-129">Exemplo</span><span class="sxs-lookup"><span data-stu-id="31760-129">Example</span></span>

<span data-ttu-id="31760-130">O exemplo a seguir mostra como usar a ação de SetReturnVar para retornar um valor de uma macro de dados nomeada.</span><span class="sxs-lookup"><span data-stu-id="31760-130">The following example shows how to use the SetReturnVar action to return a value from a named data macro.</span></span> <span data-ttu-id="31760-131">Um ReturnVar chamado **CurrentServiceRequest** é retornada para a macro ou o Visual Basic para a sub-rotina Applications (VBA) que chamou a macro de dados nomeada.</span><span class="sxs-lookup"><span data-stu-id="31760-131">A ReturnVar named **CurrentServiceRequest** is returned to the macro or Visual Basic for Applications (VBA) subroutine that called the named data macro.</span></span>

<span data-ttu-id="31760-132">**Código de exemplo fornecido pela** [referência do programador do Microsoft Access 2010](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span><span class="sxs-lookup"><span data-stu-id="31760-132">**Sample code provided by** the [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span></span>

```vb
    RunDataMacro
        Macro Name tblServiceRequests.dmGetCurrentServiceRequest
    
    Parameters
        prmAssignedTo =[ID]
    
    SetProperty
        Control Name txtCurrentSR
        Property Value
        Value =[ReturnVars]![CurrentServiceRequest]
```

<br/>

<span data-ttu-id="31760-133">O exemplo a seguir mostra como usar a ação Gerarerro para cancelar o evento de macro de dados antes de alterar.</span><span class="sxs-lookup"><span data-stu-id="31760-133">The following example shows how to use the RaiseError action to cancel the Before Change data macro event.</span></span> <span data-ttu-id="31760-134">Quando o campo AssignedTo é atualizado, um bloco de dados Pesquisarregistro é usado para determinar se o técnico atribuído atualmente atribuído a uma solicitação de serviço em aberto.</span><span class="sxs-lookup"><span data-stu-id="31760-134">When the AssignedTo field is updated, a LookupRecord data block is used to determine whether the assigned technician is currently assigned to an open service request.</span></span> <span data-ttu-id="31760-135">Se isso for verdadeiro, o evento antes de alterar será cancelado e o registro não será atualizado.</span><span class="sxs-lookup"><span data-stu-id="31760-135">If this is true, the Before Change event is cancelled and the record is not updated.</span></span>

```vb
    /* Get the name of the technician  */
    Look Up A Record In tblTechnicians
        Where Condition =[tblTechnicians].[ID]=[tblServiceRequests].[AssignedTo]
    SetLocalVar
        Name TechName
        Expression [tblTechnicians].[FirstName] & " " & [tblTechnicians].[LastName]
    /* End LookUpRecord  */
    
    If Updated("AssignedTo") Then
        Look Up A Record In tblServiceRequests
            Where Condition SR.[AssignedTo]=tblServiceRequests[AssignedTo] And 
                SR.[ID]<>tblServiceRequests.[ID] And IsNull(SR.[ActualCompletionDate])
            Alias SR
            RaiseError
                Error Number 1234
                Error Description ="Cannot assign a request to the specified technician: " & [TechName]
    
    End If
```
