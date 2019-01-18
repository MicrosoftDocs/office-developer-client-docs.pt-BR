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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28708155"
---
# <a name="setreturnvar-macro-action"></a>Ação da macro DefinirVardeRetorno

**Aplica-se a**: Access 2013, o Office 2013

A ação **SetReturnVar** cria uma variável de retorno e o configura para um valor específico.

> [!NOTE]
> A ação de **SetReturnVar** está disponível somente em Macros de dados.

## <a name="setting"></a>Configuração

A ação **SetReturnVar** tem os seguintes argumentos.

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
<td><p>Name</p></td>
<td><p>Sim</p></td>
<td><p>Uma cadeia de caracteres que especifica o nome da variável.</p></td>
</tr>
<tr class="even">
<td><p>Expressão</p></td>
<td><p>Sim</p></td>
<td><p>Uma expressão que será usada para definir o valor dessa variável temporária. Não preceda a expressão com o sinal de igual (=). Você pode clicar no botão <strong>Construir</strong> para usar o <strong>Construtor de expressões</strong> para definir este argumento.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Comentários

A ação **SetReturnVar** é usada para criar um **ReturnVar**, que é a variável que pode ser usado por macros que chamar uma macro de dados usando a ação **ExecutarMacrodeDados** .

Depois que um **ReturnVar** é criado pela ação **SetReturnVar** , a macro chamada pode ser usada em uma expressão. Por exemplo, se você criou um **ReturnVar** chamado **UpdateSuccess**, você poderia usar a variável usando a seguinte sintaxe:

```vb
    =[ReturnVars]![UpdateSuccess]
```

A ação **SetReturnVar** pode ser usada somente em macros de dados nomeada. Ele não está disponível em macros de dados que estejam anexadas a um evento de macro de dados.

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
