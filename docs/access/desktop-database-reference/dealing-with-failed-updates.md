---
title: Como lidar com atualizações com falhas
TOCTitle: Dealing with failed updates
ms:assetid: f6f4914d-59b3-f3f2-b986-218e07ce5a1d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250258(v=office.15)
ms:contentKeyID: 48548752
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 9a44548fd8747428b12c03c24207f36d3871e349
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294159"
---
# <a name="dealing-with-failed-updates"></a>Como lidar com atualizações com falhas

**Aplica-se ao:** Access 2013, Office 2013

## <a name="dealing-with-failed-updates"></a>Lidando com falhas de atualização

Quando uma atualização é concluída com erros, a maneira como você resolve os erros depende da natureza e da gravidade deles, bem como da lógica do seu aplicativo. Contudo, se o banco de dados for compartilhado com outros usuários, um erro típico seria outra pessoa modificar o campo antes de você. Esse tipo de erro é chamado de *conflito.* O ADO detecta essa situação e relata um erro.

Se houver erros de atualização, eles serão interceptados em uma rotina de tratamento de erros. Filtre o **Recordset** com a constante **adFilterConflictingRecords**, de modo que as linhas conflitantes fiquem visíveis. Neste exemplo, a estratégia de resolução de erros é simplesmente imprimir o nome e o sobrenome do autor (**au \_ fname** e **au \_ lname**).

O código usado para alertar o usuário sobre o conflito de atualização tem esta aparência:

```vb 
 
objRs.Filter = adFilterConflictingRecords 
objRs.MoveFirst 
Do While Not objRst.EOF 
   Debug.Print "Conflict: Name =  "; objRs!au_fname; " "; objRs!au_lname 
   objRs.MoveNext 
Loop 
```

