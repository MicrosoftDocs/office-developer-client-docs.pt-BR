---
title: Bloco de dados Pesquisarregistro
TOCTitle: LookupRecord data block
ms:assetid: 750dc8ca-3bab-c3d1-c91d-2196f9c0604d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195882(v=office.15)
ms:contentKeyID: 48545671
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 7a5cccb77300f36f3e33cd1eccb6c6d278db3120
ms.sourcegitcommit: 0419850d5c1b3439d9da59070201fb4952ca5d07
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/28/2020
ms.locfileid: "49734207"
---
# <a name="lookuprecord-data-block"></a>Bloco de dados Pesquisarregistro

**Aplica-se ao**: Access 2013, Office 2013

Um bloco de dados **PesquisarRegistro** executa um conjunto de ações em um registro específico.

> [!NOTE]
> O bloco de dados **PesquisarRegistro** está disponível somente em Macros de Dados.

## <a name="setting"></a>Setting

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
<td><p>POL</p></td>
<td><p>Sim</p></td>
<td><p>Uma cadeia de caracteres que identifica o registro a ser utilizado. O argumento <em>in</em> pode conter o nome da tabela, uma consulta seleção ou uma instrução SQL.</p><p><strong>Observação</strong>: o registro especificado não pode incluir dados armazenados em uma tabela vinculada ou fonte de dados ODBC.</p></td>
</tr>
<tr class="even">
<td><p>Condição Where</p></td>
<td><p>Não</p></td>
<td><p>Uma expressão de cadeia de caracteres usada para restringir o intervalo de dados no qual o bloco de dados <strong>PesquisarRegistro</strong> opera. Por exemplo, os critérios geralmente são equivalentes à cláusula WHERE em uma expressão SQL, sem a palavra WHERE. Se os critérios forem omitidos, o bloco de dados <strong>pesquisarregistro</strong> operará em todo o domínio especificado pelo argumento <em>in</em> . Qualquer campo incluído nos critérios também deve ser um campo em <em>Em</em>.</p></td>
</tr>
<tr class="odd">
<td><p>Alias</p></td>
<td><p>Não</p></td>
<td><p>Uma cadeia de caracteres que fornece um nome alternativo para o registro especificado pelo argumento <em>in</em> . Comumente usado para reduzir o nome da tabela para subsequentes referências, evitando referências ambíguas. Se o <em>Alias</em> não for especificado, o nome da tabela ou da consulta será usado como o alias.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Comentários

Se os critérios especificados pelos argumentos *in* e *Where Condition* retornarem mais de um registro, o bloco de dados **pesquisarregistro** funcionará somente no primeiro registro.  No caso de nenhum registro corresponder aos critérios especificados, o Access ignorará o conjunto de ações contidas no bloco **pesquisarregistro** , como se tivesse sido uma expressão de bloco de macro **[If](if-then-else-macro-block.md)** que foi avaliada como false.

## <a name="example"></a>Exemplo

O exemplo a seguir mostra como usar a ação SetReturnVar para retornar um valor de uma macro de dados nomeada. Um ReturnVar chamado **CurrentServiceRequest** é retornado para a macro ou a sub-rotina VBA (Visual Basic for Applications) chamada da macro de dados nomeada.

**Código de exemplo fornecido pela** [Referência do programador do Microsoft Access 2010](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).

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

O exemplo a seguir mostra como usar a ação Gerarerro para cancelar o evento antes de alterar a macro de dados. Quando o campo AssignedTo é atualizado, um bloco de dados Pesquisarregistro é usado para determinar se o técnico atribuído está atualmente atribuído a uma solicitação de serviço aberta. Se isso for verdadeiro, o evento antes de alterar será cancelado e o registro não será atualizado.

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
