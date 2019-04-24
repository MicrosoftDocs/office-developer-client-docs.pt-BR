---
title: Bloco de dados Pesquisarregistro
TOCTitle: LookupRecord data block
ms:assetid: 750dc8ca-3bab-c3d1-c91d-2196f9c0604d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195882(v=office.15)
ms:contentKeyID: 48545671
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 920f0830a310452962eb5dd1c21be63215bf0f03
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32289788"
---
# <a name="lookuprecord-data-block"></a><span data-ttu-id="b5445-102">Bloco de dados Pesquisarregistro</span><span class="sxs-lookup"><span data-stu-id="b5445-102">LookupRecord data block</span></span>

<span data-ttu-id="b5445-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="b5445-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="b5445-104">Um bloco de dados **PesquisarRegistro** executa um conjunto de ações em um registro específico.</span><span class="sxs-lookup"><span data-stu-id="b5445-104">A **LookupRecord** data block performs a set of actions on a specific record.</span></span>

> [!NOTE]
> <span data-ttu-id="b5445-105">O bloco de dados **PesquisarRegistro** está disponível somente em Macros de Dados.</span><span class="sxs-lookup"><span data-stu-id="b5445-105">The **LookupRecord** data block is available only in Data Macros.</span></span>

## <a name="setting"></a><span data-ttu-id="b5445-106">Configuração</span><span class="sxs-lookup"><span data-stu-id="b5445-106">Setting</span></span>

<span data-ttu-id="b5445-107">A ação **PesquisarRegistro** tem os seguintes argumentos.</span><span class="sxs-lookup"><span data-stu-id="b5445-107">The **SetField** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b5445-108">Argument</span><span class="sxs-lookup"><span data-stu-id="b5445-108">Argument</span></span></p></th>
<th><p><span data-ttu-id="b5445-109">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="b5445-109">Required</span></span></p></th>
<th><p><span data-ttu-id="b5445-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="b5445-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b5445-111">POL</span><span class="sxs-lookup"><span data-stu-id="b5445-111">In</span></span></p></td>
<td><p><span data-ttu-id="b5445-112">Sim</span><span class="sxs-lookup"><span data-stu-id="b5445-112">Yes</span></span></p></td>
<td><p><span data-ttu-id="b5445-113">Uma cadeia de caracteres que identifica o registro a ser utilizado.</span><span class="sxs-lookup"><span data-stu-id="b5445-113">A string that identifies the record to operate on.</span></span> <span data-ttu-id="b5445-114">O argumento <em>in</em> pode conter o nome da tabela, uma consulta seleção ou uma instrução SQL.</span><span class="sxs-lookup"><span data-stu-id="b5445-114">The <em>In</em> argument can contain the name of the table, a select query, or a SQL statement.</span></span></p><p><span data-ttu-id="b5445-115"><strong>Observação</strong>: o registro especificado não pode incluir dados armazenados em uma tabela vinculada ou fonte de dados ODBC.</span><span class="sxs-lookup"><span data-stu-id="b5445-115"><strong>NOTE</strong>: The specified record cannot include data stored in a linked table or ODBC data source.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b5445-116">Condição Where</span><span class="sxs-lookup"><span data-stu-id="b5445-116">Where Condition</span></span></p></td>
<td><p><span data-ttu-id="b5445-117">Não</span><span class="sxs-lookup"><span data-stu-id="b5445-117">No</span></span></p></td>
<td><p><span data-ttu-id="b5445-118">Uma expressão de cadeia de caracteres usada para restringir o intervalo de dados no qual o bloco de dados <strong>PesquisarRegistro</strong> opera.</span><span class="sxs-lookup"><span data-stu-id="b5445-118">A string expression used to restrict the range of data on which the <strong>LookupRecord</strong> data block is performed.</span></span> <span data-ttu-id="b5445-119">Por exemplo, os critérios geralmente são equivalentes à cláusula WHERE em uma expressão SQL, sem a palavra WHERE.</span><span class="sxs-lookup"><span data-stu-id="b5445-119">For example, criteria are often equivalent to the WHERE clause in an SQL expression, without the word WHERE.</span></span> <span data-ttu-id="b5445-120">Se os critérios forem omitidos, o bloco de dados <strong>pesquisarregistro</strong> operará em todo o domínio especificado pelo argumento <em>in</em> .</span><span class="sxs-lookup"><span data-stu-id="b5445-120">If criteria are omitted, the <strong>LookupRecord</strong> data block operates on the entire domain specified by the <em>In</em> argument.</span></span> <span data-ttu-id="b5445-121">Qualquer campo incluído nos critérios também deve ser um campo em <em>Em</em>.</span><span class="sxs-lookup"><span data-stu-id="b5445-121">Any field that is included in criteria must also be a field in <em>In</em>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b5445-122">Alias</span><span class="sxs-lookup"><span data-stu-id="b5445-122">Alias</span></span></p></td>
<td><p><span data-ttu-id="b5445-123">Não</span><span class="sxs-lookup"><span data-stu-id="b5445-123">No</span></span></p></td>
<td><p><span data-ttu-id="b5445-124">Uma cadeia de caracteres que fornece um nome alternativo para o registro especificado pelo argumento <em>in</em> .</span><span class="sxs-lookup"><span data-stu-id="b5445-124">A string that provides an alternative name for the record specified by the <em>In</em> argument.</span></span> <span data-ttu-id="b5445-125">Comumente usado para reduzir o nome da tabela para subsequentes referências, evitando referências ambíguas.</span><span class="sxs-lookup"><span data-stu-id="b5445-125">Often used to shorten the table name for subsequent references to prevent possible ambiguous references.</span></span> <span data-ttu-id="b5445-126">Se o <em>Alias</em> não for especificado, o nome da tabela ou da consulta será usado como o alias.</span><span class="sxs-lookup"><span data-stu-id="b5445-126">If <em>Alias</em> is not specified, the table or query name will be used as the alias.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="b5445-127">Comentários</span><span class="sxs-lookup"><span data-stu-id="b5445-127">Remarks</span></span>

<span data-ttu-id="b5445-128">Se os critérios especificados pelos argumentos *in* e *Where Condition* especificarem mais de um registro, o bloco de dados **pesquisarregistro** funcionará somente no primeiro registro.</span><span class="sxs-lookup"><span data-stu-id="b5445-128">If the criteria specified by the *In* and *Where Condition* arguments specifies more than one record, the **LookupRecord** data block will operate only on the first record.</span></span>

## <a name="example"></a><span data-ttu-id="b5445-129">Exemplo</span><span class="sxs-lookup"><span data-stu-id="b5445-129">Example</span></span>

<span data-ttu-id="b5445-130">O exemplo a seguir mostra como usar a ação SetReturnVar para retornar um valor de uma macro de dados nomeada.</span><span class="sxs-lookup"><span data-stu-id="b5445-130">The following example shows how to use the SetReturnVar action to return a value from a named data macro.</span></span> <span data-ttu-id="b5445-131">Um ReturnVar chamado **CurrentServiceRequest** é retornado para a macro ou a sub-rotina VBA (Visual Basic for Applications) chamada da macro de dados nomeada.</span><span class="sxs-lookup"><span data-stu-id="b5445-131">A ReturnVar named **CurrentServiceRequest** is returned to the macro or Visual Basic for Applications (VBA) subroutine that called the named data macro.</span></span>

<span data-ttu-id="b5445-132">**Código de exemplo fornecido por:** a [Referência do programador do Microsoft Access 2010](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span><span class="sxs-lookup"><span data-stu-id="b5445-132">**Sample code provided by** the [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span></span>

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

<span data-ttu-id="b5445-133">O exemplo a seguir mostra como usar a ação Gerarerro para cancelar o evento antes de alterar a macro de dados.</span><span class="sxs-lookup"><span data-stu-id="b5445-133">The following example shows how to use the RaiseError action to cancel the Before Change data macro event.</span></span> <span data-ttu-id="b5445-134">Quando o campo AssignedTo é atualizado, um bloco de dados Pesquisarregistro é usado para determinar se o técnico atribuído está atualmente atribuído a uma solicitação de serviço aberta.</span><span class="sxs-lookup"><span data-stu-id="b5445-134">When the AssignedTo field is updated, a LookupRecord data block is used to determine whether the assigned technician is currently assigned to an open service request.</span></span> <span data-ttu-id="b5445-135">Se isso for verdadeiro, o evento antes de alterar será cancelado e o registro não será atualizado.</span><span class="sxs-lookup"><span data-stu-id="b5445-135">If this is true, the Before Change event is cancelled and the record is not updated.</span></span>

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
