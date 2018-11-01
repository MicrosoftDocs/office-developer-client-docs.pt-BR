---
title: Bloco de dados PesquisarRegistro
TOCTitle: LookupRecord Data Block
ms:assetid: 750dc8ca-3bab-c3d1-c91d-2196f9c0604d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195882(v=office.15)
ms:contentKeyID: 48545671
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 3bd9a687d7f74b99dc20ee079f970c37ba627f31
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25877685"
---
# <a name="lookuprecord-data-block"></a>Bloco de dados PesquisarRegistro

**Aplica-se a**: Access 2013, o Office 2013

Um bloco de dados **PesquisarRegistro** executa um conjunto de ações em um registro específico.

> [!NOTE]
> [!OBSERVAçãO] O bloco de dados **PesquisarRegistro** está disponível somente em Macros de Dados.

## <a name="setting"></a>Configuração

A ação **PesquisarRegistro** tem os seguintes argumentos.

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Argumento</p></th>
<th><p>Obrigatório</p></th>
<th><p>Descrição</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Em</p></td>
<td><p>Sim</p></td>
<td><p>Uma cadeia de caracteres que identifica o registro para operar em. O argumento <em>em</em> pode conter o nome da tabela, uma consulta seleção ou uma instrução SQL.</p>

> [!NOTE]
> O registro especificado não pode incluir dados armazenados em uma tabela vinculada ou fonte de dados ODBC.


<p></p></td>
</tr>
<tr class="even">
<td><p>Condição Where</p></td>
<td><p>Não</p></td>
<td><p>Uma expressão de cadeia de caracteres usada para restringir o intervalo de dados no qual o bloco de dados <strong>Pesquisarregistro</strong> é executada. Por exemplo, critérios costumam ser equivalentes à cláusula WHERE em uma expressão SQL, sem a palavra onde. Se os critérios forem omitidos, o bloco de dados <strong>Pesquisarregistro</strong> opera em todo o domínio especificado pelo argumento <em>em</em> . Qualquer campo que está incluído nos critérios também deve ser um campo no <em>In</em>.</p></td>
</tr>
<tr class="odd">
<td><p>Alias</p></td>
<td><p>Não</p></td>
<td><p>Uma cadeia de caracteres que fornece um nome alternativo para o registro especificado pelo argumento <em>em</em> . Frequentemente usado para reduzir o nome da tabela referências posteriores evitar possíveis referências ambíguas. Se o <em>Alias</em> não for especificado, o nome da tabela ou da consulta será usado como o alias.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Comentários

Se os critérios especificados pelos argumentos *no* e a *Condição Where* especifica mais de um registro, o bloco de dados **Pesquisarregistro** funcionará apenas no primeiro registro.

## <a name="example"></a>Exemplo

O exemplo a seguir mostra como usar a ação de SetReturnVar para retornar um valor de uma macro de dados nomeada. Um ReturnVar chamado **CurrentServiceRequest** é retornada para a macro ou o Visual Basic para a sub-rotina Applications (VBA) que chamou a macro de dados nomeada.

**Código de exemplo fornecido pela** [referência do programador do Microsoft Access 2010](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).

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

O exemplo a seguir mostra como usar a ação Gerarerro para cancelar o evento de macro de dados antes de alterar. Quando o campo AssignedTo é atualizado, um bloco de dados Pesquisarregistro é usado para determinar se o técnico atribuído atualmente atribuído a uma solicitação de serviço em aberto. Se isso for verdadeiro, o evento antes de alterar será cancelado e o registro não será atualizado.

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
