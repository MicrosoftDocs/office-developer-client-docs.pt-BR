---
title: Ação de macro ExecutarMacrodeDados
TOCTitle: RunDataMacro Macro Action
ms:assetid: fe4ac2f4-7851-7797-ce91-5f2dd3ba4d22
ms:mtpsurl: https://msdn.microsoft.com/library/Ff837269(v=office.15)
ms:contentKeyID: 48548933
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm168493
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 9790faf03ba0f6ea02520abb525c4301ac2181e2
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25462435"
---
# <a name="rundatamacro-macro-action"></a>Ação de macro ExecutarMacrodeDados

**Aplica-se a**: Access 2013 | Office 2013

Você pode usar a ação **ExecutarMacrodeDados** para executar uma macro.

## <a name="setting"></a>Configuração

A ação **ExecutarMacrodeDados** tem os seguintes argumentos.

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
<td><p>Name</p></td>
<td><p>O nome da macro de dados a ser executada.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Comentários

Você pode usar a ação **ExecutarMacrodeDados** em macros, macros de dados nomeadas e nos seguintes eventos de macro: **[Evento de macro Após Exclusão](after-delete-macro-event.md)**, **[Evento de macro Após Inserir](after-insert-macro-event.md)** e **[Evento de macro Após Atualizar](after-update-macro-event.md)**.

O nome da macro de dados deve incluir a tabela à qual ele está conectado (por exemplo, **comentários**, não apenas **AddComment**).

Quando você selecionar a macro de dados que deseja executar no designer de macros, o Access determinará se a macro de dados exige parâmetros. Se a macro de dados requer parâmetros, caixas de texto aparecem onde você pode digitar nos argumentos.

Quando você executa uma macro que contém a ação **ExecutarMacrodeDados** e ela alcançar a ação **ExecutarMacrodeDados**, o Access executará a macro de dados chamada. Após a conclusão da macro de dados chamada, o Access retornará à macro original e executará a próxima ação.

## <a name="example"></a>Exemplo

O exemplo a seguir mostra como passar um parâmetro a uma macro de dados nomeada. A macro de dados da tabela tblServiceRequests dmGetCurrentServiceRequest é chamada usando a ação ExecutarMacrodeDados. Quando o dmGetCurrentServiceRequest for concluído, a variável CurrentServiceRequest retornados a macro de dados está escrita à caixa de texto txtCurrentSR do formulário.

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
