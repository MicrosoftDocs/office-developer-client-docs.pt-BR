---
title: Usando indicadores (referência de banco de dados da área de trabalho do Access)
TOCTitle: Using Bookmarks
ms:assetid: fe6333ef-c9d9-1e84-2252-d27edc676e97
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250306(v=office.15)
ms:contentKeyID: 48548935
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 9c362e87f3e962586c2bd821bd6facb35966a77f
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25886834"
---
# <a name="using-bookmarks"></a><span data-ttu-id="f432f-102">Uso de marcadores</span><span class="sxs-lookup"><span data-stu-id="f432f-102">Using Bookmarks</span></span>


<span data-ttu-id="f432f-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="f432f-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="f432f-p101">Frequentemente é útil retornar diretamente a um registro específico depois de ter percorrido o **Recordset** sem precisar rolar por cada registro e comparar valores. Por exemplo, se você tentar pesquisar um registro usando o método **Find** mas a pesquisa não retornar nenhum registro, você será colocado automaticamente em alguma extremidade do **Recordset**. Se o provedor oferecer suporte, poderão ser usados indicadores para marcar seu lugar antes de usar o método **Find**, de forma que você pode retornar ao local. Um indicador é um valor do tipo **Variant** que identifica de maneira exclusiva um registro em um objeto **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="f432f-p101">It is often useful to return directly to a specific record after having moved around in the **Recordset** without having to scroll through every record and compare values. For example, if you attempt to search for a record using the **Find** method but the search returns no records, you are automatically placed at either end of the **Recordset**. If your provider supports them, bookmarks can be used to mark your place before using the **Find** method so you can return to your location. A bookmark is a **Variant** type value that uniquely identifies a record in a **Recordset** object.</span></span>

<span data-ttu-id="f432f-p102">Você também pode usar uma matriz variant de indicadores com o método **Filter** do **Recordset** para filtrar um conjunto selecionado de registros. Para obter detalhes sobre essa técnica, consulte Filtrando os resultados no tópico [Trabalhando com recordsets](working-with-recordsets.md), posteriormente neste capítulo.</span><span class="sxs-lookup"><span data-stu-id="f432f-p102">You can also use a variant array of bookmarks with the **Recordset** **Filter** method to filter on a selected set of records. For details about this technique, see Filtering the Results in the topic, [Working with Recordsets](working-with-recordsets.md), later in this chapter.</span></span>

<span data-ttu-id="f432f-p103">Você pode usar a propriedade **Bookmark** para obter um indicador para um registro ou definir o registro atual em um objeto **Recordset** para o registro identificado por um indicador válido. O código a seguir usa a propriedade **Bookmark** para definir um indicador e, em seguida, retornar o registro indicado depois de mover-se para outros registros. Para determinar se o seu **Recordset** oferece suporte a indicadores, use o método **Supports**.</span><span class="sxs-lookup"><span data-stu-id="f432f-p103">You can use the **Bookmark** property to get a bookmark for a record, or set the current record in a **Recordset** object to the record identified by a valid bookmark. The following code uses the **Bookmark** property to set a bookmark and then return to the bookmarked record after moving on to other records. To determine if your **Recordset** supports bookmarks, use the **Supports** method.</span></span>

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

<span data-ttu-id="f432f-113">O método [Supports](supports-method-ado.md) será abordado em mais detalhes posteriormente.</span><span class="sxs-lookup"><span data-stu-id="f432f-113">The [Supports](supports-method-ado.md) method is covered in more detail later.</span></span>

<span data-ttu-id="f432f-p104">Exceto no caso de **Recordsets** clonados, os indicadores são exclusivos do **Recordset** no qual foram criados, mesmo que o mesmo comando seja usado. Isso significa que você não pode usar um **Bookmark** obtido de um **Recordset** para mover-se para o mesmo registro em outro **Recordset** aberto com o mesmo comando.</span><span class="sxs-lookup"><span data-stu-id="f432f-p104">Except for the case of cloned **Recordsets**, bookmarks are unique to the **Recordset** in which they were created, even if the same command is used. This means that you cannot use a **Bookmark** obtained from one **Recordset** to move to the same record in a second **Recordset** opened with the same command.</span></span>

