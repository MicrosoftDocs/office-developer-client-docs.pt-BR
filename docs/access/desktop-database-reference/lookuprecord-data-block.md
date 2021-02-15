---
title: Bloco de dados LookupRecord
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
# <a name="lookuprecord-data-block"></a>Bloco de dados LookupRecord

**Aplica-se ao:** Access 2013, Office 2013

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
<td><p>Uma cadeia de caracteres que identifica o registro a ser utilizado. O <em>argumento In</em> pode conter o nome da tabela, uma consulta seleção ou uma instrução SQL.</p><p><strong>OBSERVAÇÃO:</strong>o registro especificado não pode incluir dados armazenados em uma tabela vinculada ou fonte de dados ODBC.</p></td>
</tr>
<tr class="even">
<td><p>Condição Where</p></td>
<td><p>Não</p></td>
<td><p>Uma expressão de cadeia de caracteres usada para restringir o intervalo de dados no qual o bloco de dados <strong>PesquisarRegistro</strong> opera. Por exemplo, os critérios geralmente são equivalentes à cláusula WHERE em uma expressão SQL, sem a palavra WHERE. Se os critérios são omitidos, o bloco de dados <strong>LookupRecord</strong> opera em todo o domínio especificado pelo <em>argumento</em> In. Qualquer campo incluído nos critérios também deve ser um campo em <em>Em</em>.</p></td>
</tr>
<tr class="odd">
<td><p>Alias</p></td>
<td><p>Não</p></td>
<td><p>Uma cadeia de caracteres que fornece um nome alternativo para o registro especificado pelo <em>argumento</em> In. Comumente usado para reduzir o nome da tabela para subsequentes referências, evitando referências ambíguas. Se o <em>Alias</em> não for especificado, o nome da tabela ou da consulta será usado como o alias.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Comentários

Se os critérios especificados pelos argumentos *In* e *Where Condition* retornarem mais de um registro, o bloco de dados **LookupRecord** funcionará somente no primeiro registro.  Caso nenhum registro corresponder aos critérios especificados, o Access ignorará o conjunto de ações contidas no bloco **LookupRecord,** como se tivesse sido uma expressão de bloco de macro **[If](if-then-else-macro-block.md)** avaliada como false.

## <a name="example"></a>Exemplo

O exemplo a seguir mostra como usar a ação SetReturnVar para retornar um valor de uma macro de dados nomeada. Uma ReturnVar chamada **CurrentServiceRequest** é retornada para a macro ou sub-rotina Visual Basic for Applications (VBA) que chamou a macro de dados nomeada.

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

O exemplo a seguir mostra como usar a ação RaiseError para cancelar o evento de macro de dados Antes de Alterar. Quando o campo AssignedTo é atualizado, um bloco de dados LookupRecord é usado para determinar se o técnico atribuído está atribuído no momento a uma solicitação de serviço aberta. Se isso for verdadeiro, o evento Antes de Alterar será cancelado e o registro não será atualizado.

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
