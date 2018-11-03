---
title: Lidando com falhas de atualização
TOCTitle: Dealing with failed updates
ms:assetid: f6f4914d-59b3-f3f2-b986-218e07ce5a1d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250258(v=office.15)
ms:contentKeyID: 48548752
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 659b5389074371ed4de41b909ab5228ad8fca080
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/03/2018
ms.locfileid: "25947744"
---
# <a name="dealing-with-failed-updates"></a><span data-ttu-id="d85ee-102">Lidando com falhas de atualização</span><span class="sxs-lookup"><span data-stu-id="d85ee-102">Dealing with failed updates</span></span>

<span data-ttu-id="d85ee-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="d85ee-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="dealing-with-failed-updates"></a><span data-ttu-id="d85ee-104">Como lidar com atualizações com falhas</span><span class="sxs-lookup"><span data-stu-id="d85ee-104">Dealing with Failed Updates</span></span>

<span data-ttu-id="d85ee-p101">Quando uma atualização é concluída com erros, a maneira como você resolve os erros depende da natureza e da gravidade deles, bem como da lógica do seu aplicativo. Contudo, se o banco de dados for compartilhado com outros usuários, um erro típico seria outra pessoa modificar o campo antes de você. Esse tipo de erro é chamado de *conflito.* O ADO detecta essa situação e relata um erro.</span><span class="sxs-lookup"><span data-stu-id="d85ee-p101">When an update concludes with errors, how you resolve the errors depends on the nature and severity of the errors and the logic of your application. However, if the database is shared with other users, a typical error is that someone else modifies the field before you do. This type of error is called a *conflict.* ADO detects this situation and reports an error.</span></span>

<span data-ttu-id="d85ee-109">Se houver erros de atualização, eles serão interceptados em uma rotina de tratamento de erros.</span><span class="sxs-lookup"><span data-stu-id="d85ee-109">If there are update errors, they will be trapped in an error-handling routine.</span></span> <span data-ttu-id="d85ee-110">Filtre o **Recordset** com a constante **adFilterConflictingRecords**, de modo que as linhas conflitantes fiquem visíveis.</span><span class="sxs-lookup"><span data-stu-id="d85ee-110">Filter the **Recordset** with the **adFilterConflictingRecords** constant so that only the conflicting rows are visible.</span></span> <span data-ttu-id="d85ee-111">Neste exemplo, a estratégia de resolução de erro é meramente imprimir o autor do primeiro e último nome (**au\_fname** e **au\_SNome**).</span><span class="sxs-lookup"><span data-stu-id="d85ee-111">In this example, the error-resolution strategy is merely to print the author's first and last names (**au\_fname** and **au\_lname**).</span></span>

<span data-ttu-id="d85ee-112">O código usado para alertar o usuário sobre o conflito de atualização tem esta aparência:</span><span class="sxs-lookup"><span data-stu-id="d85ee-112">The code to alert the user to the update conflict looks like this:</span></span>

```vb 
 
objRs.Filter = adFilterConflictingRecords 
objRs.MoveFirst 
Do While Not objRst.EOF 
   Debug.Print "Conflict: Name =  "; objRs!au_fname; " "; objRs!au_lname 
   objRs.MoveNext 
Loop 
```

