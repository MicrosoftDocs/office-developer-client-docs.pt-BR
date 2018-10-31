---
title: Propriedade Error (DAO)
TOCTitle: Source Property
ms:assetid: 3c101cac-278e-025e-55a4-8a9d1ee7db3c
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192677(v=office.15)
ms:contentKeyID: 48544302
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053360
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 51acfc5f349d6096028ef86aac480ce81c9b26bf
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25860494"
---
# <a name="errorsource-property-dao"></a><span data-ttu-id="8319e-102">Propriedade Error (DAO)</span><span class="sxs-lookup"><span data-stu-id="8319e-102">Error.Source Property (DAO)</span></span>


<span data-ttu-id="8319e-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="8319e-103">**Applies to**: Access 2013 | Office 2013</span></span>


<span data-ttu-id="8319e-104">Retorna o nome do objeto ou do aplicativo que gerou originalmente o erro.</span><span class="sxs-lookup"><span data-stu-id="8319e-104">Returns the name of the object or application that originally generated the error.</span></span>

## <a name="syntax"></a><span data-ttu-id="8319e-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8319e-105">Syntax</span></span>

<span data-ttu-id="8319e-106">*expressão* . Fonte</span><span class="sxs-lookup"><span data-stu-id="8319e-106">*expression* .Source</span></span>

<span data-ttu-id="8319e-107">*expressão* Uma variável que representa um objeto **Error** .</span><span class="sxs-lookup"><span data-stu-id="8319e-107">*expression* A variable that represents an **Error** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="8319e-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="8319e-108">Remarks</span></span>

<span data-ttu-id="8319e-p101">Geralmente, o valor da propriedade **Source** é o nome da classe do objeto ou a ID programática. Use a propriedade **Source** para fornecer informações aos usuários, quando o código não estiver disponível para lidar com um erro gerado em um objeto em outro aplicativo.</span><span class="sxs-lookup"><span data-stu-id="8319e-p101">The **Source** property value is usually the object's class name or programmatic ID. Use the **Source** property to provide your users with information when your code is unable to handle an error generated in an object in another application.</span></span>

<span data-ttu-id="8319e-111">Por exemplo, se você acessar o Microsoft Excel e ele gerar um erro de "Divisão por zero", o Microsoft Excel define **Number** para o código do Microsoft Excel para esse erro e define a propriedade **Source** como o Excel. Application.</span><span class="sxs-lookup"><span data-stu-id="8319e-111">For example, if you access Microsoft Excel and it generates a "Division by zero" error, Microsoft Excel sets **Error.Number** to the Microsoft Excel code for that error and sets the **Source** property to Excel.Application.</span></span> <span data-ttu-id="8319e-112">Observe que se o erro for gerado em outro objeto chamado pelo Microsoft Excel, este interceptará o erro e ainda definirá **Error.Number** como o código do Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="8319e-112">Note that if the error is generated in another object called by Microsoft Excel, Microsoft Excel intercepts the error and still sets **Error.Number** to the Microsoft Excel code.</span></span> <span data-ttu-id="8319e-113">No entanto, as outras propriedades do objeto **Error** (incluindo **Source**) reterão os valores como foram definidos pelo objeto que gerou o erro.</span><span class="sxs-lookup"><span data-stu-id="8319e-113">However, the other **Error** object properties (including **Source**) will retain the values as set by the object that generated the error.</span></span> <span data-ttu-id="8319e-114">A propriedade **Source** sempre contém o nome do objeto que gerou originalmente o erro.</span><span class="sxs-lookup"><span data-stu-id="8319e-114">The **Source** property always contains the name of the object that originally generated the error.</span></span>

<span data-ttu-id="8319e-p103">Com base em toda a documentação de erros, é possível gravar um código que trate o erro de forma adequada. Se houver falhas no manipulador de erros, você poderá usar as informações do objeto **[Error](error-object-dao.md)** para descrever o erro para o usuário, por meio da propriedade **Source** e das outras propriedades **Error** para fornecer ao usuário informações sobre qual objeto gerou originalmente o erro, a descrição do erro e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="8319e-p103">Based on all of the error documentation, you can write code that will handle the error appropriately. If your error handler fails, you can use the **[Error](error-object-dao.md)** object information to describe the error to your user, using the **Source** property and the other **Error** properties to give the user information about which object originally caused the error, the description of the error, and so forth.</span></span>


> [!NOTE]
> <span data-ttu-id="8319e-p104">A construção **On Error Resume Next** poderá ser preferível a **On Error GoTo** durante a manipulação de erros gerados durante o acesso a outros objetos. A verificação da propriedade do objeto **Error** depois de cada interação com um objeto remove a ambiguidade do objeto que o código estava acessando durante a ocorrência do erro. Assim, você pode ter certeza de que o objeto colocou o código de erro em **Error.Number**, assim como aquele objeto que gerou originalmente o erro (**Error.Source**).</span><span class="sxs-lookup"><span data-stu-id="8319e-p104">The **On Error Resume Next** construct may be preferable to **On Error GoTo** when dealing with errors generated during access to other objects. Checking the **Error** object property after each interaction with an object removes ambiguity about which object your code was accessing when the error occurred. Thus, you can be sure which object placed the error code in **Error.Number**, as well as which object originally generated the error (**Error.Source**).</span></span>

## <a name="example"></a><span data-ttu-id="8319e-120">Exemplo</span><span class="sxs-lookup"><span data-stu-id="8319e-120">Example</span></span>

<span data-ttu-id="8319e-121">Este exemplo força um erro, captura-o e exibe as propriedades **Description**, **Number**, **Source**, **HelpContext** e **HelpFile** do objeto **Error** resultante.</span><span class="sxs-lookup"><span data-stu-id="8319e-121">This example forces an error, traps it, and displays the **Description**, **Number**, **Source**, **HelpContext**, and **HelpFile** properties of the resulting **Error** object.</span></span>

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
