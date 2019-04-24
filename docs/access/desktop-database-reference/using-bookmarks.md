---
title: Usando indicadores (referência de banco de dados de área de trabalho do Access)
TOCTitle: Using Bookmarks
ms:assetid: fe6333ef-c9d9-1e84-2252-d27edc676e97
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250306(v=office.15)
ms:contentKeyID: 48548935
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 469d8a0cc9b644fe434770d51c21d8210c8038d0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306304"
---
# <a name="using-bookmarks"></a>Uso de marcadores


**Aplica-se ao:** Access 2013, Office 2013

Frequentemente é útil retornar diretamente a um registro específico depois de ter percorrido o **Recordset** sem precisar rolar por cada registro e comparar valores. Por exemplo, se você tentar pesquisar um registro usando o método **Find** mas a pesquisa não retornar nenhum registro, você será colocado automaticamente em alguma extremidade do **Recordset**. Se o provedor oferecer suporte, poderão ser usados indicadores para marcar seu lugar antes de usar o método **Find**, de forma que você pode retornar ao local. Um indicador é um valor do tipo **Variant** que identifica de maneira exclusiva um registro em um objeto **Recordset**.

Você também pode usar uma matriz variant de indicadores com o método **Filter** do **Recordset** para filtrar um conjunto selecionado de registros. Para obter detalhes sobre essa técnica, consulte Filtrando os resultados no tópico [Trabalhando com recordsets](working-with-recordsets.md), posteriormente neste capítulo.

Você pode usar a propriedade **Bookmark** para obter um indicador para um registro ou definir o registro atual em um objeto **Recordset** para o registro identificado por um indicador válido. O código a seguir usa a propriedade **Bookmark** para definir um indicador e, em seguida, retornar o registro indicado depois de mover-se para outros registros. Para determinar se o seu **Recordset** oferece suporte a indicadores, use o método **Supports**.

```vb 
 
'BeginBookmarkEg 
 Dim varBookmark As Variant 
 Dim blnCanBkmrk As Boolean 
 
 objRs.Open strSQL, strConnStr, adOpenStatic, adLockOptimistic, adCmdText 
 
 If objRs.RecordCount > 4 Then 
 objRs.Move 4 ' move to the fifth record 
 blnCanBkmrk = objRs.Supports(adBookmark) 
 If blnCanBkmrk = True Then 
 varBookmark = objRs.Bookmark ' record the bookmark 
 objRs.MoveLast ' move to a different record 
 objRs.Bookmark = varBookmark ' return to the bookmarked (sixth) record 
 End If 
 End If 
'EndBookmarkEg 
```

O método [Supports](supports-method-ado.md) será abordado em mais detalhes posteriormente.

Exceto no caso de **Recordsets** clonados, os indicadores são exclusivos do **Recordset** no qual foram criados, mesmo que o mesmo comando seja usado. Isso significa que você não pode usar um **Bookmark** obtido de um **Recordset** para mover-se para o mesmo registro em outro **Recordset** aberto com o mesmo comando.

