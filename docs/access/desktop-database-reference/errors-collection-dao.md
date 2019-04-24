---
title: Coleção Errors (DAO)
TOCTitle: Errors Collection
ms:assetid: d42007b5-6410-14e9-baf9-9306fdef38f9
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834805(v=office.15)
ms:contentKeyID: 48547929
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: cf8e891936d4f8bd03535fa199026bc4ad8ff9ba
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293410"
---
# <a name="errors-collection-dao"></a><span data-ttu-id="e0981-102">Coleção Errors (DAO)</span><span class="sxs-lookup"><span data-stu-id="e0981-102">Errors collection (DAO)</span></span>


<span data-ttu-id="e0981-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="e0981-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="e0981-104">Uma coleção **Errors** contém todos os objetos **Error** armazenados, cada um dos quais pertence a uma única operação envolvendo o DAO.</span><span class="sxs-lookup"><span data-stu-id="e0981-104">An **Errors** collection contains all stored **Error** objects, each of which pertains to a single operation involving DAO.</span></span>

## <a name="remarks"></a><span data-ttu-id="e0981-105">Comentários</span><span class="sxs-lookup"><span data-stu-id="e0981-105">Remarks</span></span>

<span data-ttu-id="e0981-106">Qualquer operação envolvendo objetos do DAO pode gerar um ou mais erros.</span><span class="sxs-lookup"><span data-stu-id="e0981-106">Any operation involving DAO objects can generate one or more errors.</span></span> <span data-ttu-id="e0981-107">Quando cada erro ocorre, um ou mais objetos **Error** são colocados na coleção **Errors** do objeto **DBEngine**.</span><span class="sxs-lookup"><span data-stu-id="e0981-107">As each error occurs, one or more **Error** objects are placed in the **Errors** collection of the **DBEngine** object.</span></span> <span data-ttu-id="e0981-108">Quando outra operação do DAO gera um erro, a coleção **Errors** é limpa e o novo conjunto de objetos **Error** é colocado na coleção **Errors**.</span><span class="sxs-lookup"><span data-stu-id="e0981-108">When another DAO operation generates an error, the **Errors** collection is cleared, and the new set of **Error** objects is placed in the **Errors** collection.</span></span> <span data-ttu-id="e0981-109">O objeto de número mais elevado na coleção \*\*Errors \*\*(DBEngine.Errors.Count - 1) corresponde ao erro informado pelo objeto **Err** do Microsoft Visual Basic for Applications (VBA).</span><span class="sxs-lookup"><span data-stu-id="e0981-109">The highest-numbered object in the **Errors** collection (DBEngine.Errors.Count - 1) corresponds to the error reported by the Microsoft Visual Basic for Applications (VBA) **Err** object.</span></span>

<span data-ttu-id="e0981-110">Operações do DAO que não geram erro não produzem efeito na coleção **Errors**.</span><span class="sxs-lookup"><span data-stu-id="e0981-110">DAO operations that don't generate an error have no effect on the **Errors** collection.</span></span>

<span data-ttu-id="e0981-111">Elementos da coleção **Errors** não são acrescentados como geralmente ocorre com outras coleções, portanto a coleção **Errors** não oferece suporte para os métodos **Append** e **Delete**.</span><span class="sxs-lookup"><span data-stu-id="e0981-111">Elements of the **Errors** collection aren't appended as they typically are with other collections, so the **Errors** collection doesn't support the **Append** and **Delete** methods.</span></span>

<span data-ttu-id="e0981-p102">O conjunto de objetos **Error** na coleção **Errors** descreve um erro. O primeiro objeto **Error** é o erro de nível mais baixo, o segundo, o próximo nível mais alto, e assim por diante. Por exemplo, se um erro de ODBC ocorre durante a tentativa de abrir um objeto **[Recordset](recordset-object-dao.md)**, o primeiro objeto error contém o erro de ODBC de nível mais baixo; erros subsequentes contêm os erros de ODBC retornados pelas várias camadas de ODBC. Neste caso, o gerenciador de driver ODBC e possivelmente o próprio driver retornam objetos **Error** separados. O último objeto **Error** contém o erro do DAO indicando que o objeto não pôde ser aberto.</span><span class="sxs-lookup"><span data-stu-id="e0981-p102">The set of **Error** objects in the **Errors** collection describes one error. The first **Error** object is the lowest level error, the second the next higher level, and so forth. For example, if an ODBC error occurs while trying to open a **[Recordset](recordset-object-dao.md)** object, the first error object contains the lowest level ODBC error; subsequent errors contain the ODBC errors returned by the various layers of ODBC. In this case, the ODBC driver manager, and possibly the driver itself, return separate **Error** objects. The last **Error** object contains the DAO error indicating that the object couldn't be opened.</span></span>

<span data-ttu-id="e0981-117">Enumerar os erros específicos na coleção **Errors** permite que suas rotinas de manipulação de erros determinem mais precisamente a causa e a origem de um erro e tomem as medidas de recuperação apropriadas.</span><span class="sxs-lookup"><span data-stu-id="e0981-117">Enumerating the specific errors in the **Errors** collection enables your error-handling routines to more precisely determine the cause and origin of an error, and take appropriate steps to recover.</span></span>


> [!NOTE]
> <span data-ttu-id="e0981-p103">[!OBSERVAçãO] Se você utiliza a palavra-chave **New** para criar um objeto que causa um erro tanto antes como quando ele está sendo colocado na coleção **Errors**, a coleção não conterá informações de erro sobre aquele objeto, porque o novo objeto não está associado ao objeto **DBEngine**. No entanto, a informação de erro estará disponível no objeto **Err** do VBA.</span><span class="sxs-lookup"><span data-stu-id="e0981-p103">If you use the **New** keyword to create an object that causes an error either before or while being placed into the **Errors** collection, the collection doesn't contain error information about that object, because the new object is not associated with the **DBEngine** object. However, the error information is available in the VBA **Err** object.</span></span>

## <a name="example"></a><span data-ttu-id="e0981-120">Exemplo</span><span class="sxs-lookup"><span data-stu-id="e0981-120">Example</span></span>

<span data-ttu-id="e0981-121">Este exemplo força um erro, captura-o e exibe as propriedades **Description**, **Number**, **Source**, **HelpContext** e **HelpFile** do objeto **Error** resultante.</span><span class="sxs-lookup"><span data-stu-id="e0981-121">This example forces an error, traps it, and displays the **Description**, **Number**, **Source**, **HelpContext**, and **HelpFile** properties of the resulting **Error** object.</span></span>

```vb 
Sub DescriptionX() 
 
 Dim dbsTest As Database 
 
 On Error GoTo ErrorHandler 
 
 ' Intentionally trigger an error. 
 Set dbsTest = OpenDatabase("NoDatabase") 
 
 Exit Sub 
 
ErrorHandler: 
 Dim strError As String 
 Dim errLoop As Error 
 
 ' Enumerate Errors collection and display properties of 
 ' each Error object. 
 For Each errLoop In Errors 
 With errLoop 
 strError = _ 
 "Error #" & .Number & vbCr 
 strError = strError & _ 
 " " & .Description & vbCr 
 strError = strError & _ 
 " (Source: " & .Source & ")" & vbCr 
 strError = strError & _ 
 "Press F1 to see topic " & .HelpContext & vbCr 
 strError = strError & _ 
 " in the file " & .HelpFile & "." 
 End With 
 MsgBox strError 
 Next 
 
 Resume Next 
 
End Sub 
 
```

