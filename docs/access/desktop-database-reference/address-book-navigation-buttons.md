---
title: Botões de navegação do Catálogo de Endereços
TOCTitle: Address Book navigation buttons
ms:assetid: 4ec32c08-5b35-8dce-23ec-0daa4db551cf
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249253(v=office.15)
ms:contentKeyID: 48544765
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: e7c87acd433df4a303c1e6a15a60184cadf994c3
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28700245"
---
# <a name="address-book-navigation-buttons"></a>Botões de navegação do Catálogo de Endereços

**Aplica-se a**: Access 2013, o Office 2013

O aplicativo de catálogo de endereços exibe os botões de navegação na parte inferior da página da Web. Você pode utilizar os botões de navegação para navegar através dos dados na exibição da grade HTML, selecionando a primeira e a última linha de dados ou linhas adjacentes à seleção atual.

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

