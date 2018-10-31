---
title: Objetos de objeto Error - acesso a dados (DAO)
TOCTitle: Error Object
ms:assetid: e2608bc9-bece-9b47-4562-7a2689601f75
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835711(v=office.15)
ms:contentKeyID: 48548289
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 526498ee22bc82735eb3b98e633aa3d1b4cfb610
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25864099"
---
# <a name="error-object-dao"></a><span data-ttu-id="dc8a4-102">Objeto Error (DAO)</span><span class="sxs-lookup"><span data-stu-id="dc8a4-102">Error Object (DAO)</span></span>


<span data-ttu-id="dc8a4-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="dc8a4-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="dc8a4-104">O objeto **Error** contém detalhes sobre os erros de acesso aos dados, que pertencem a uma única operação envolvendo DAO.</span><span class="sxs-lookup"><span data-stu-id="dc8a4-104">**Error** object contains details about data access errors, each of which pertains to a single operation involving DAO.</span></span>

## <a name="remarks"></a><span data-ttu-id="dc8a4-105">Comentários</span><span class="sxs-lookup"><span data-stu-id="dc8a4-105">Remarks</span></span>

<span data-ttu-id="dc8a4-p101">Qualquer operação envolvendo DAO pode gerar um ou mais erros. Por exemplo, uma chamada para um servidor ODBC pode resultar em um erro no servidor de banco de dados, no ODBC e no DAO. À medida que esse tipo de erro ocorre, um objeto **Error** é colocado na coleção **Errors** do objeto **DBEngine**. Um único evento pode resultar em vários objetos **Error** aparecendo na coleção **Errors**.</span><span class="sxs-lookup"><span data-stu-id="dc8a4-p101">Any operation involving DAO can generate one or more errors. For example, a call to an ODBC server might result in an error from the database server, an error from ODBC, and a DAO error. As each such error occurs, an **Error** object is placed in the **Errors** collection of the **DBEngine** object. A single event can therefore result in several **Error** objects appearing in the **Errors** collection.</span></span>

<span data-ttu-id="dc8a4-p102">Quando uma operação DAO subsequente gera um erro, a coleção **Errors** é limpa, e um ou mais novos objetos **Error** são colocados na coleção **Errors**. As operações DAO que não geram nenhum erro não são efetivadas na coleção **Errors**.</span><span class="sxs-lookup"><span data-stu-id="dc8a4-p102">When a subsequent DAO operation generates an error, the **Errors** collection is cleared, and one or more new **Error** objects are placed in the **Errors** collection. DAO operations that don't generate an error have no effect on the **Errors** collection.</span></span>

<span data-ttu-id="dc8a4-p103">A definição dos objetos **Error** na coleção **Errors** descreve um erro. O primeiro objeto **Error** é o erro no nível mais baixo (o erro de origem), o segundo é o erro no próximo nível mais alto e assim por diante. Por exemplo, se ocorrer um erro ODBC durante a tentativa de abrir um objeto **[Recordset](recordset-object-dao.md)**, o primeiro objeto **Error**  **Errors**(0)  conterá o erro ODBC no nível mais baixo; os erros subsequentes conterão os erros ODBC retornados por várias camadas ODBC. Nesse caso, o gerenciador do driver ODBC, e possivelmente o próprio driver, retorna objetos **Error** separados. O último objeto **Error**  **Errors.Count-** 1  contém o erro DAO que indica que o objeto não pode ser aberto.</span><span class="sxs-lookup"><span data-stu-id="dc8a4-p103">The set of **Error** objects in the **Errors** collection describes one error. The first **Error** object is the lowest level error (the originating error), the second the next higher level error, and so forth. For example, if an ODBC error occurs while trying to open a **[Recordset](recordset-object-dao.md)** object, the first **Error** object— **Errors**(0)— contains the lowest level ODBC error; subsequent errors contain the ODBC errors returned by the various layers of ODBC. In this case, the ODBC driver manager, and possibly the driver itself, return separate **Error** objects. The last **Error** object— **Errors.Count-** 1— contains the DAO error indicating that the object couldn't be opened.</span></span>

<span data-ttu-id="dc8a4-p104">Enumerar os erros específicos na coleção **Errors** permite que as rotinas de tratamento de erros determinem de forma mais precisa a causa e a origem de um erro e executem as etapas apropriadas para recuperação. Você pode ler as propriedades do objeto **Error** para obter detalhes específicos sobre cada erro, inclusive:</span><span class="sxs-lookup"><span data-stu-id="dc8a4-p104">Enumerating the specific errors in the **Errors** collection enables your error-handling routines to more precisely determine the cause and origin of an error, and take appropriate steps to recover. You can read the **Error** object's properties to obtain specific details about each error, including:</span></span>

  - <span data-ttu-id="dc8a4-119">A propriedade **[Description](error-description-property-dao.md)**, que contém o texto do alerta de erros que será exibido na tela se o erro não for rastreado.</span><span class="sxs-lookup"><span data-stu-id="dc8a4-119">The **[Description](error-description-property-dao.md)** property, which contains the text of the error alert that will be displayed on the screen if the error is not trapped.</span></span>

  - <span data-ttu-id="dc8a4-120">A propriedade **[Number](error-number-property-dao.md)**, que contém o valor inteiro Long da constante de erros.</span><span class="sxs-lookup"><span data-stu-id="dc8a4-120">The **[Number](error-number-property-dao.md)** property, which contains the Long integer value of the error constant.</span></span>

  - <span data-ttu-id="dc8a4-p105">A propriedade **[Source](error-source-property-dao.md)**, que identifica o objeto que ocasionou o erro. Isso é particularmente útil quando você tem vários objetos **Error** na coleção **Errors** seguindo uma solicitação para uma fonte de dados ODBC.</span><span class="sxs-lookup"><span data-stu-id="dc8a4-p105">The **[Source](error-source-property-dao.md)** property, which identifies the object that raised the error. This is particularly useful when you have several **Error** objects in the **Errors** collection following a request to an ODBC data source.</span></span>

  - <span data-ttu-id="dc8a4-123">As propriedades **HelpFile** e **HelpContext**, que indicam o arquivo e o tópico de Ajuda apropriados do Microsoft Windows, respectivamente (se houver algum) para o erro.</span><span class="sxs-lookup"><span data-stu-id="dc8a4-123">The **HelpFile** and **HelpContext** properties, which indicate the appropriate Microsoft Windows Help file and Help topic, respectively, (if any exist) for the error.</span></span>
    

    > [!NOTE]
    > <span data-ttu-id="dc8a4-124">[!OBSERVAçãO] Durante uma programação no Microsoft Visual Basic for Applications, se você usar a palavra-chave **New** para criar um objeto que, subsequentemente, causa um erro antes de o objeto ser acrescentado a uma coleção, a coleção **Errors** do objeto **DBEngine** não conterá nenhum entrada para aquele erro do objeto, porque o novo objeto não está associado ao objeto **DBEngine**.</span><span class="sxs-lookup"><span data-stu-id="dc8a4-124">When programming in Microsoft Visual Basic for Applications (VBA), if you use the **New** keyword to create an object that subsequently causes an error before that object has been appended to a collection, the **DBEngine** object's **Errors** collection won't contain an entry for that object's error, because the new object is not associated with the **DBEngine** object.</span></span> <span data-ttu-id="dc8a4-125">Entretanto, as informações do erro estão disponíveis no objeto **Err** do VBA.</span><span class="sxs-lookup"><span data-stu-id="dc8a4-125">However, the error information is available in the VBA **Err** object.</span></span> <span data-ttu-id="dc8a4-126">Seu código de tratamento de erro deve examinar a coleção **Errors** sempre que você antecipa um erro de acesso aos dados.</span><span class="sxs-lookup"><span data-stu-id="dc8a4-126">Your VBA error-handling code should examine the **Errors** collection whenever you anticipate a data access error.</span></span> <span data-ttu-id="dc8a4-127">Se você estiver gravando uma rotina de tratamento de erro centralizada, teste o objeto **Err** do VBA para determinar se as informações do erro na coleção **Errors** são válidas.</span><span class="sxs-lookup"><span data-stu-id="dc8a4-127">If you are writing a centralized error handler, test the VBA **Err** object to determine if the error information in the **Errors** collection is valid.</span></span> <span data-ttu-id="dc8a4-128">Se a propriedade **Number** do último elemento da coleção **Errors** (DBEngine.Errors.Count - 1) e o valor da correspondência objeto **Err** , você pode usar uma série de instruções **Select Case** para identificar o erro específico do DAO ou erros que ocorreram.</span><span class="sxs-lookup"><span data-stu-id="dc8a4-128">If the **Number** property of the last element of the **Errors** collection (DBEngine.Errors.Count - 1) and the value of the **Err** object match, you can then use a series of **Select Case** statements to identify the particular DAO error or errors that occurred.</span></span> <span data-ttu-id="dc8a4-129">Se eles não forem correspondentes, use o método [Refresh](errors-refresh-method-dao.md) na coleção **Errors**.</span><span class="sxs-lookup"><span data-stu-id="dc8a4-129">If they do not match, use the [Refresh](errors-refresh-method-dao.md) method on the **Errors** collection.</span></span>



## <a name="example"></a><span data-ttu-id="dc8a4-130">Exemplo</span><span class="sxs-lookup"><span data-stu-id="dc8a4-130">Example</span></span>

<span data-ttu-id="dc8a4-131">Este exemplo força um erro, captura-o e exibe as propriedades **Description**, **Number**, **Source**, **HelpContext** e **HelpFile** do objeto **Error** resultante.</span><span class="sxs-lookup"><span data-stu-id="dc8a4-131">This example forces an error, traps it, and displays the **Description**, **Number**, **Source**, **HelpContext**, and **HelpFile** properties of the resulting **Error** object.</span></span>

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
            "  " & .Description & vbCr 
         strError = strError & _ 
            "  (Source: " & .Source & ")" & vbCr 
         strError = strError & _ 
            "Press F1 to see topic " & .HelpContext & vbCr 
         strError = strError & _ 
            "  in the file " & .HelpFile & "." 
      End With 
      MsgBox strError 
   Next 
 
   Resume Next 
 
End Sub 
 
```

