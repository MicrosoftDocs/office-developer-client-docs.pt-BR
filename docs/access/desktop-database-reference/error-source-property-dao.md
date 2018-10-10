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
ms.openlocfilehash: b9aafe1b16b3d989a81ff21f97bd4b6d10f79de3
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25464231"
---
# <a name="errorsource-property-dao"></a><span data-ttu-id="309be-102">Propriedade Error (DAO)</span><span class="sxs-lookup"><span data-stu-id="309be-102">Error.Source Property (DAO)</span></span>


<span data-ttu-id="309be-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="309be-103">**Applies to**: Access 2013 | Office 2013</span></span>


<span data-ttu-id="309be-104">Retorna o nome do objeto ou do aplicativo que gerou originalmente o erro.</span><span class="sxs-lookup"><span data-stu-id="309be-104">Returns the name of the object or application that originally generated the error.</span></span>

## <a name="syntax"></a><span data-ttu-id="309be-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="309be-105">Syntax</span></span>

<span data-ttu-id="309be-106">*expressão* . Fonte</span><span class="sxs-lookup"><span data-stu-id="309be-106">*expression* .Source</span></span>

<span data-ttu-id="309be-107">*expressão* Uma variável que representa um objeto **Error** .</span><span class="sxs-lookup"><span data-stu-id="309be-107">*expression* A variable that represents an **Error** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="309be-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="309be-108">Remarks</span></span>

<span data-ttu-id="309be-p101">Geralmente, o valor da propriedade **Source** é o nome da classe do objeto ou a ID programática. Use a propriedade **Source** para fornecer informações aos usuários, quando o código não estiver disponível para lidar com um erro gerado em um objeto em outro aplicativo.</span><span class="sxs-lookup"><span data-stu-id="309be-p101">The **Source** property value is usually the object's class name or programmatic ID. Use the **Source** property to provide your users with information when your code is unable to handle an error generated in an object in another application.</span></span>

<span data-ttu-id="309be-111">Por exemplo, se você acessar o Microsoft Excel e ele gerar um erro de "Divisão por zero", o Microsoft Excel define **Number** para o código do Microsoft Excel para esse erro e define a propriedade **Source** como o Excel. Application.</span><span class="sxs-lookup"><span data-stu-id="309be-111">For example, if you access Microsoft Excel and it generates a "Division by zero" error, Microsoft Excel sets **Error.Number** to the Microsoft Excel code for that error and sets the **Source** property to Excel.Application.</span></span> <span data-ttu-id="309be-112">Observe que se o erro for gerado em outro objeto chamado pelo Microsoft Excel, este interceptará o erro e ainda definirá **Error.Number** como o código do Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="309be-112">Note that if the error is generated in another object called by Microsoft Excel, Microsoft Excel intercepts the error and still sets **Error.Number** to the Microsoft Excel code.</span></span> <span data-ttu-id="309be-113">No entanto, as outras propriedades do objeto **Error** (incluindo **Source**) reterão os valores como foram definidos pelo objeto que gerou o erro.</span><span class="sxs-lookup"><span data-stu-id="309be-113">However, the other **Error** object properties (including **Source**) will retain the values as set by the object that generated the error.</span></span> <span data-ttu-id="309be-114">A propriedade **Source** sempre contém o nome do objeto que gerou originalmente o erro.</span><span class="sxs-lookup"><span data-stu-id="309be-114">The **Source** property always contains the name of the object that originally generated the error.</span></span>

<span data-ttu-id="309be-p103">Com base em toda a documentação de erros, é possível gravar um código que trate o erro de forma adequada. Se houver falhas no manipulador de erros, você poderá usar as informações do objeto **[Error](error-object-dao.md)** para descrever o erro para o usuário, por meio da propriedade **Source** e das outras propriedades **Error** para fornecer ao usuário informações sobre qual objeto gerou originalmente o erro, a descrição do erro e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="309be-p103">Based on all of the error documentation, you can write code that will handle the error appropriately. If your error handler fails, you can use the **[Error](error-object-dao.md)** object information to describe the error to your user, using the **Source** property and the other **Error** properties to give the user information about which object originally caused the error, the description of the error, and so forth.</span></span>


> [!NOTE]
> <P><span data-ttu-id="309be-p104">A construção <STRONG>On Error Resume Next</STRONG> poderá ser preferível a <STRONG>On Error GoTo</STRONG> durante a manipulação de erros gerados durante o acesso a outros objetos. A verificação da propriedade do objeto <STRONG>Error</STRONG> depois de cada interação com um objeto remove a ambiguidade do objeto que o código estava acessando durante a ocorrência do erro. Assim, você pode ter certeza de que o objeto colocou o código de erro em <STRONG>Error.Number</STRONG>, assim como aquele objeto que gerou originalmente o erro (<STRONG>Error.Source</STRONG>).</span><span class="sxs-lookup"><span data-stu-id="309be-p104">The <STRONG>On Error Resume Next</STRONG> construct may be preferable to <STRONG>On Error GoTo</STRONG> when dealing with errors generated during access to other objects. Checking the <STRONG>Error</STRONG> object property after each interaction with an object removes ambiguity about which object your code was accessing when the error occurred. Thus, you can be sure which object placed the error code in <STRONG>Error.Number</STRONG>, as well as which object originally generated the error (<STRONG>Error.Source</STRONG>).</span></span></P>



## <a name="example"></a><span data-ttu-id="309be-120">Exemplo</span><span class="sxs-lookup"><span data-stu-id="309be-120">Example</span></span>

<span data-ttu-id="309be-121">Este exemplo força um erro, captura-o e exibe as propriedades **Description**, **Number**, **Source**, **HelpContext** e **HelpFile** do objeto **Error** resultante.</span><span class="sxs-lookup"><span data-stu-id="309be-121">This example forces an error, traps it, and displays the **Description**, **Number**, **Source**, **HelpContext**, and **HelpFile** properties of the resulting **Error** object.</span></span>

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
