---
title: Bloco de macro Se...Então...Senão
TOCTitle: If...Then...Else macro block
ms:assetid: 0c4a4b7a-4fdb-9dbc-a94e-939a2ff1c0e5
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845158(v=office.15)
ms:contentKeyID: 48543188
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Priority
ms.openlocfilehash: fb6cbd6cc925a3e4841d9e7d6d77332cc36c7a03
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32291891"
---
# <a name="ifthenelse-macro-block"></a>Bloco de macro Se...Então...Senão


**Aplica-se ao**: Access 2013, Office 2013

Você pode usar o bloco de macro **Se** para executar condicionalmente um grupo de ações, dependendo do valor de uma expressão.

```vb
    If expression Then 
     Insert macro actions here ... 
    Else If expression 
     Insert macro actions here ... 
    Else 
     Insert macro actions here ... 
    End If
```

## <a name="setting"></a>Configuração

Para ambos **Se** e ** Senão Se**, os seguintes argumentos são requeridos.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Argumento da ação</p></th>
<th><p>Descrição</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Expressão</strong>.</p></td>
<td><p>A condição que você deseja testar. Deve ser uma expressão que avalia como True ou False.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Comentários

Quando você seleciona o bloco de macro **Se**, uma caixa de texto é exibida para que você digite uma expressão que representa a condição a ser testada. Além disso, uma caixa de combinação é exibida para que você insira uma ação de macro, abaixo da qual o texto "Encerrar Se" é exibido automaticamente. Se e Encerrar Se delimitam uma área na qual é possível digitar um grupo ou um bloco de ações. O bloco será executado somente se a expressão inserida tiver o valor True.

Para avaliar outra expressão quando a primeira expressão tiver o valor False, clique em **Adicionar Senão Se** para inserir um bloco **Senão Se** adicional. A expressão inserida deve avaliar como True ou False. Nesse caso, o bloco será executado somente se a expressão tiver o valor True e a primeira expressão tiver o valor False.

Você pode adicionar a quantidade necessária de **Senão Se** a um bloco Se.

Clique em **Adicionar Senão** para inserir um bloco **Senão** adicional. Nesse caso, as ações inseridas abaixo de **Senão** formam o bloco **Senão**, que será executado somente se as ações acima não forem executadas. É possível adicionar um único bloco **Senão** a um bloco **Se**.

No exemplo de código a seguir, as ações de macro no primeiro bloco serão executadas se o valor de\[Status\] for maior que 0. Se o valor de \[Status\] não for maior que 0, a expressão após **Senão Se** será avaliada. As ações de macro no bloco**Senão Se** serão executadas se o valor de \[Status\] for igual a 0. Finalmente, se nem o primeiro bloco, nem o segundo forem executados, as ações no bloco **Senão** serão executadas.

```vb
    If [Status] > 0 Then 
     Insert macro actions here ... 
    Else If [Status] = 0 
     Insert macro actions here ... 
    Else 
     Insert macro actions here ... 
    End If
```

Você pode aninhar blocos **Se**. Considere o aninhamento do bloco **Se** em um bloco **Se** se você deseja avaliar uma segunda expressão, quando a primeira expressão tiver o valor True. No exemplo de código a seguir, o bloco interno **Se** somente será executado quando o valor de \[Status\] for maior que 0 *e* maior que 100.

```vb
    If [Status] > 0 Then 
     Insert macro actions here ... 
     If [Status] > 100 
     Insert macro actions here ... 
     EndifEnd If
```
