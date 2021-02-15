---
title: Ação da macro ExecutarMacrodeDados
TOCTitle: RunDataMacro macro action
ms:assetid: fe4ac2f4-7851-7797-ce91-5f2dd3ba4d22
ms:mtpsurl: https://msdn.microsoft.com/library/Ff837269(v=office.15)
ms:contentKeyID: 48548933
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm168493
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 32945f0822682a9432d75ed1ac59117dde3cc0e9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306808"
---
# <a name="rundatamacro-macro-action"></a>Ação da macro ExecutarMacrodeDados

**Aplica-se ao:** Access 2013, Office 2013

Você pode usar a ação **ExecutarMacrodeDados** para executar uma macro.

## <a name="setting"></a>Setting

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
<td><p>Nome</p></td>
<td><p>O nome da macro de dados a ser executada.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Comentários

Você pode usar a ação **RunDataMacro** em macros, macros de dados nomeadas e os seguintes eventos de macro: evento de **[macro](after-delete-macro-event.md)** Após Exclusão , evento de **[macro](after-insert-macro-event.md)** Após Inserir e evento de macro Após **[Atualização.](after-update-macro-event.md)**

O nome da macro de dados deve incluir a tabela à qual está anexada (por exemplo, **Comments.AddComment**, não apenas **AddComment**).

Quando você selecionar a macro de dados que deseja executar no designer de macros, o Access determinará se a macro de dados exige parâmetros. Se a macro de dados exigir parâmetros, as caixas de texto aparecerão onde você poderá digitar os argumentos.

Quando você executa uma macro que contém a ação **ExecutarMacrodeDados** e ela alcançar a ação **ExecutarMacrodeDados**, o Access executará a macro de dados chamada. Após a conclusão da macro de dados chamada, o Access retornará à macro original e executará a próxima ação.

## <a name="example"></a>Exemplo

O exemplo a seguir mostra como passar um parâmetro para uma macro de dados nomeada. A macro de dados dmGetCurrentServiceRequest da tabela tblServiceRequests é chamada usando a ação RunDataMacro. Quando o dmGetCurrentServiceRequest é concluído, a variável CurrentServiceRequest retornou a forma como a macro de dados é escrita na caixa de texto txtCurrentSR.

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
