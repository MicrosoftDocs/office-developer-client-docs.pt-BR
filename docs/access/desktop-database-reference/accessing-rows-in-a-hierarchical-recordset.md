---
title: Acessando as linhas em um Recordset hierárquico
TOCTitle: Accessing rows in a hierarchical Recordset
ms:assetid: db59b152-b780-539c-17ef-462e8adfb26e
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250106(v=office.15)
ms:contentKeyID: 48548104
ms.date: 10/17/2018
mtps_version: v=office.15
ms.openlocfilehash: 3041aa1486f9630a36383dde4ad675c50c799339
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25870027"
---
# <a name="accessing-rows-in-a-hierarchical-recordset"></a>Acessando as linhas em um Recordset hierárquico

**Aplica-se a**: Access 2013, o Office 2013

O exemplo a seguir mostra as etapas necessárias para acessar as linhas em um [Recordset](recordset-object-ado.md) hierárquico:

1. Os objetos **Recordset** dos autores e as tabelas do autor de títulos são relacionados pelo ID do autor.

2. O loop externo exibe o nome e sobrenome de cada autor, o estado e a identificação.

3. O **Recordset** anexado para cada linha é recuperado da coleção **Fields** e designado ao *rstTitleAuthor*.

4. O loop interno exibe quatro campos de cada linha no **Recordset** anexado.

> [!NOTE] 
> A propriedade [StayInSync](stayinsync-property-ado.md) é definida como FALSE para fins de ilustração, para que você possa ver o capítulo alterar explicitamente cada iteração do loop externo. No entanto, o exemplo será mais eficiente se a atribuição na etapa 3 for movida antes da primeira linha na etapa 2; de modo que a atribuição seja executada apenas uma vez. Defina a propriedade **StayInSync** como TRUE, para que *rstTitleAuthor* automaticamente e implicitamente alterará o capítulo correspondente sempre que *rst* move para uma nova linha.

**Exemplo**

```vb 
 
Sub datashape() 
 Dim cnn As New ADODB.Connection 
 Dim rst As New ADODB.Recordset 
 Dim rstTitleAuthor As New ADODB.Recordset 
 
 cnn.Provider = "MSDataShape" 
 cnn.Open "Data Provider=MSDASQL;" & _ 
 "Data Source=SRV;" & _ 
 "User Id=MyUserName;Password=MyPassword;Database=Pubs" 
' STEP 1 
 rst.StayInSync = FALSE 
 rst.Open "SHAPE {select * from authors} " & _ 
 "APPEND ({select * from titleauthor} " & _ 
 "RELATE au_id TO au_id) AS chapTitleAuthor", _ 
 cnn 
' STEP 2 
 While Not rst.EOF 
 Debug.Print rst("au_fname"), rst("au_lname"), _ 
 rst("state"), rst("au_id") 
' STEP 3 
 Set rstTitleAuthor = rst("chapTitleAuthor").Value 
' STEP 4 
 While Not rstTitleAuthor.EOF 
 Debug.Print rstTitleAuthor(0), rstTitleAuthor(1), _ 
 rstTitleAuthor(2), rstTitleAuthor(3) 
 rstTitleAuthor.MoveNext 
 Wend 
 rst.MoveNext 
 Wend 
End Sub 
```

