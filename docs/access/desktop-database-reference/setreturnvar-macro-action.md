---
title: Ação da macro DefinirVardeRetorno
TOCTitle: SetReturnVar macro action
ms:assetid: 53719857-00bb-4f33-b5d2-93aff92d736e
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193989(v=office.15)
ms:contentKeyID: 48544870
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 0e0c849fc507d535807bc088e667acd74410ddd8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308670"
---
# <a name="setreturnvar-macro-action"></a>Ação da macro DefinirVardeRetorno

**Aplica-se ao:** Access 2013, Office 2013

A **ação SetReturnVar** cria uma variável de retorno e a define como um valor específico.

> [!NOTE]
> A **ação DefinirVarReturna** está disponível somente em Macros de Dados.

## <a name="setting"></a>Setting

A **ação SetReturnVar** tem os seguintes argumentos.

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
<td><p>Nome</p></td>
<td><p>Sim</p></td>
<td><p>Uma cadeia de caracteres que especifica o nome da variável.</p></td>
</tr>
<tr class="even">
<td><p>Expression</p></td>
<td><p>Sim</p></td>
<td><p>Uma expressão que será usada para definir o valor dessa variável temporária. Não preceda a expressão com o sinal de igualdade (=). Você pode clicar no botão <strong>Build</strong> para usar o <strong>Construtor de Expressões</strong> para definir esse argumento.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Comentários

A **ação SetReturnVar** é usada para criar uma **Variável** RetornarVar , que é uma variável que pode ser usada por macros que chamam uma macro de dados usando a ação **RunDataMacro.**

Depois que **uma Revar** Retornada é criada pela **ação DefinirVarVar,** a macro de chamada pode usá-la em uma expressão. Por exemplo, se você criou uma **ReturnVar** chamada **UpdateSuccess,** poderá usar a variável usando a seguinte sintaxe:

```vb
    =[ReturnVars]![UpdateSuccess]
```

A **ação SetReturnVar** pode ser usada somente em macros de dados nomeadas. Ela não está disponível em macros de dados anexadas a um evento de macro de dados.

## <a name="example"></a>Exemplo

O exemplo a seguir mostra como usar a ação SetReturnVar para retornar um valor de uma macro de dados nomeada. Uma ReturnVar chamada **CurrentServiceRequest** é retornada para a macro ou sub-rotina Visual Basic for Applications (VBA) que chamou a macro de dados nomeada.

**Código de exemplo fornecido por:** a [Referência do programador do Microsoft Access 2010](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).

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
