---
title: Botões de navegação do Catálogo de Endereços
TOCTitle: Address Book Navigation Buttons
ms:assetid: 4ec32c08-5b35-8dce-23ec-0daa4db551cf
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249253(v=office.15)
ms:contentKeyID: 48544765
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 3d68a15873bc5030fd51e54c2219a0ffd91f080f
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25464117"
---
# <a name="address-book-navigation-buttons"></a>Botões de navegação do Catálogo de Endereços


**Aplica-se a**: Access 2013 | Office 2013

O aplicativo de Catálogo de Endereço exibe os botões de navegação no fim da página da Web. Você pode utilizar os botões de navegação para navegar através dos dados na exibição da grade HTML, selecionando a primeira e a última linha de dados ou linhas adjacentes à seleção atual.

## <a name="navigation-sub-procedures"></a>Subprocedimentos de navegação

O aplicativo de Catálogo de Endereço contém vários procedimentos que permitem aos usuários clicarem nos botões **Primeiro**, **Próximo**, **Anterior** e **Último** para mover-se ap redor dos dados.

Por exemplo, clicando no botão **primeiro** ativa a primeira VBScript\_procedimento OnClick Sub. O procedimento executa um método [MoveFirst](movefirst-movelast-movenext-and-moveprevious-methods-rds.md), que torna a primeira linha de dados a seleção atual. Clicar no botão **último** ativa a última\_procedimento OnClick Sub, que chama o método [MoveLast](movefirst-movelast-movenext-and-moveprevious-methods-rds.md) , tornando a última linha de dados da seleção atual. Os demais botões de navegação trabalham de uma maneira semelhante.

```vb 
 
' Move to the first record in the bound Recordset. 
Sub First_OnClick 
 DC1.Recordset.MoveFirst 
End Sub 
 
' Move to the next record from the current position 
' in the bound Recordset. 
Sub Next_OnClick 
 If Not DC1.Recordset.EOF Then ' Cannot move beyond bottom record. 
 DC1.Recordset.MoveNext 
 Exit Sub 
 End If 
End Sub 
 
' Move to the previous record from the current position in the bound 
' Recordset. 
Sub Prev_OnClick 
 If Not DC1.Recordset.BOF Then ' Cannot move beyond top record. 
 DC1.Recordset.MovePrevious 
 Exit Sub 
 End If 
End Sub 
 
' Move to the last record in the bound Recordset. 
Sub Last_OnClick 
 DC1.Recordset.MoveLast 
End Sub 
```
