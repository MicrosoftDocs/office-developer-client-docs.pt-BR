---
title: Tutorial do RDS (VBScript)
TOCTitle: RDS tutorial (VBScript)
ms:assetid: 7a6596fd-00b9-a637-7d00-fb55a621305f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249506(v=office.15)
ms:contentKeyID: 48545792
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 996c0adf8c883de5c73174d726cf5bd11fc42457
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/06/2018
ms.locfileid: "25996878"
---
# <a name="rds-tutorial-vbscript"></a><span data-ttu-id="19b88-102">Tutorial do RDS (VBScript)</span><span class="sxs-lookup"><span data-stu-id="19b88-102">RDS tutorial (VBScript)</span></span>

<span data-ttu-id="19b88-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="19b88-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="19b88-104">Esse é o tutorial do RDS, escrito em Microsoft Visual Basic Scripting Edition.</span><span class="sxs-lookup"><span data-stu-id="19b88-104">This is the RDS tutorial, written in Microsoft Visual Basic Scripting Edition.</span></span> <span data-ttu-id="19b88-105">Para obter uma descrição do objetivo deste tutorial, consulte o [tutorial RDS](chapter-12-rds-tutorial.md).</span><span class="sxs-lookup"><span data-stu-id="19b88-105">For a description of the purpose of this tutorial, see the [RDS tutorial](chapter-12-rds-tutorial.md).</span></span>

<span data-ttu-id="19b88-106">Neste tutorial, [RDS. DataControl](datacontrol-object-rds.md) e [RDS. DataSpace](dataspace-object-rds.md) são criados no tempo de design; ou seja, eles são definidos com marcas object.</span><span class="sxs-lookup"><span data-stu-id="19b88-106">In this tutorial, [RDS.DataControl](datacontrol-object-rds.md) and [RDS.DataSpace](dataspace-object-rds.md) are created at design time; that is, they are defined with object tags.</span></span> <span data-ttu-id="19b88-107">Como alternativa, eles podem ser criados no momento da execução com o método **Server.CreateObject**.</span><span class="sxs-lookup"><span data-stu-id="19b88-107">Alternatively, they could be created at run time with the **Server.CreateObject** method.</span></span> 

<span data-ttu-id="19b88-108">Por exemplo, o objeto **RDS.DataControl** pode ser criado dessa forma:</span><span class="sxs-lookup"><span data-stu-id="19b88-108">For example, the **RDS.DataControl** object could be created like this:</span></span>

```vb
    Set DC = Server.CreateObject("RDS.DataControl") 
     <!-- RDS.DataControl --> 
     <OBJECT 
     ID="DC1" CLASSID="CLSID:BD96C556-65A3-11D0-983A-00C04FC29E33"> 
     </OBJECT> 
     
     <!-- RDS.DataSpace --> 
     <OBJECT 
     ID="DS1" WIDTH=1 HEIGHT=1 
     CLASSID="CLSID:BD96C556-65A3-11D0-983A-00C04FC29E36"> 
     </OBJECT> 
     
     <SCRIPT LANGUAGE="VBScript"> 
     
     Sub RDSTutorial() 
     Dim DF1 
```

## <a name="step-1--specify-a-server-program"></a><span data-ttu-id="19b88-109">Etapa 1  Especificar um programa de servidor</span><span class="sxs-lookup"><span data-stu-id="19b88-109">Step 1 — Specify a server program</span></span>

<span data-ttu-id="19b88-110">O VBScript pode descobrir o nome do servidor web IIS que está sendo executado no acessando o método VBScript **Request. ServerVariables** disponível para Active Server Pages:</span><span class="sxs-lookup"><span data-stu-id="19b88-110">VBScript can discover the name of the IIS web server it is running on by accessing the VBScript **Request.ServerVariables** method available to Active Server Pages:</span></span>

```vb 
 
"https://<%=Request.ServerVariables("SERVER_NAME")%>" 
```

<span data-ttu-id="19b88-111">No entanto, para esse tutorial, use o servidor imaginário "yourServer".</span><span class="sxs-lookup"><span data-stu-id="19b88-111">However, for this tutorial, use the imaginary server, "yourServer."</span></span>

> [!NOTE]
> <span data-ttu-id="19b88-p103">[!OBSERVAçãO] Preste atenção nos tipos de dados dos argumentos **ByRef**. O VBScript não permite que você especifique o tipo de variável, então, você deve sempre transmitir uma Variant. Quando HTTP for utilizado, o RDS permitirá a transmissão de uma Variant para um método que espera uma non-Variant, se você chamá-lo com o método **CreateObject** do objeto [RDS.DataSpace](createobject-method-rds.md). Ao utilizar DCOM ou um servidor em execução, corresponda os tipos de parâmetros no cliente e no servidor; caso contrário, receberá um erro "Incompatibilidade de tipo".</span><span class="sxs-lookup"><span data-stu-id="19b88-p103">Pay attention to the data type of **ByRef** arguments. VBScript does not let you specify the variable type, so you must always pass a Variant. When using HTTP, RDS will allow you to pass a Variant to a method that expects a non-Variant if you invoke it with the **RDS.DataSpace** object [CreateObject](createobject-method-rds.md) method. When using DCOM or an in-process server, match the parameter types on the client and server sides or you will receive a "Type Mismatch" error.</span></span>

```vb
 
Set DF1 = DS1.CreateObject("RDSServer.DataFactory", "https://yourServer") 
```

## <a name="step-2a--invoke-the-server-program-with-rdsdatacontrol"></a><span data-ttu-id="19b88-116">Etapa 2a  Chamar o programa do servidor com RDS.DataControl</span><span class="sxs-lookup"><span data-stu-id="19b88-116">Step 2a — Invoke the server program with RDS.DataControl</span></span>

<span data-ttu-id="19b88-117">Esse exemplo é meramente um comentário para demonstrar que o comportamento padrão do **RDS.DataControl** destina-se a executar a consulta especificada.</span><span class="sxs-lookup"><span data-stu-id="19b88-117">This example is merely a comment demonstrating that the default behavior of the **RDS.DataControl** is to perform the specified query.</span></span>

```vb
 
<OBJECT CLASSID="clsid:BD96C556-65A3-11D0-983A-00C04FC29E33" ID="DC1"> 
 <PARAM NAME="SQL" VALUE="SELECT * FROM Authors"> 
 <PARAM NAME="Connect" VALUE="DSN=Pubs;"> 
 <PARAM NAME="Server" VALUE="https://yourServer/"> 
</OBJECT> 
... 
<SCRIPT LANGUAGE="VBScript"> 
 
Sub RDSTutorial2A() 
 Dim RS 
 DC1.Refresh 
 Set RS = DC1.Recordset 
... 
```

## <a name="step-2b--invoke-the-server-program-with-rdsserverdatafactory"></a><span data-ttu-id="19b88-118">Etapa 2a  Chamar o programa do servidor com RDS.DataControl</span><span class="sxs-lookup"><span data-stu-id="19b88-118">Step 2b — Invoke the server program with RDSServer.DataFactory</span></span>

## <a name="step-3--server-obtains-a-recordset"></a><span data-ttu-id="19b88-119">Etapa 3  O servidor obtém um Recordset</span><span class="sxs-lookup"><span data-stu-id="19b88-119">Step 3 — Server obtains a Recordset</span></span>

## <a name="step-4--server-returns-the-recordset"></a><span data-ttu-id="19b88-120">Etapa 4  O servidor retorna o Recordset</span><span class="sxs-lookup"><span data-stu-id="19b88-120">Step 4 — Server returns the Recordset</span></span>

```vb
 
Set RS = DF1.Query("DSN=Pubs;", "SELECT * FROM Authors") 
```

## <a name="step-5--datacontrol-is-made-usable-by-visual-controls"></a><span data-ttu-id="19b88-121">Etapa 5  O DataControl torna-se disponível por meio de controles visuais</span><span class="sxs-lookup"><span data-stu-id="19b88-121">Step 5 — DataControl is made usable by visual controls</span></span>

```vb
 
' Assign the returned recordset to the DataControl. 
 
DC1.SourceRecordset = RS 
```

## <a name="step-6a--changes-are-sent-to-the-server-with-rdsdatacontrol"></a><span data-ttu-id="19b88-122">Etapa 6a — as alterações são enviadas para o servidor com RDS. DataControl \*</span><span class="sxs-lookup"><span data-stu-id="19b88-122">Step 6a — Changes are sent to the server with RDS.DataControl\*</span></span>

<span data-ttu-id="19b88-123">Esse exemplo é meramente um comentário que demonstra como o **RDS.DataControl** executa as atualizações.</span><span class="sxs-lookup"><span data-stu-id="19b88-123">This example is merely a comment demonstrating how the **RDS.DataControl** performs updates.</span></span>

```vb
 
<OBJECT CLASSID="clsid:BD96C556-65A3-11D0-983A-00C04FC29E33" ID="DC1"> 
 <PARAM NAME="SQL" VALUE="SELECT * FROM Authors"> 
 <PARAM NAME="Connect" VALUE="DSN=Pubs;"> 
 <PARAM NAME="Server" VALUE="https://yourServer/"> 
</OBJECT> 
... 
<SCRIPT LANGUAGE="VBScript"> 
 
Sub RDSTutorial6A() 
Dim RS 
DC1.Refresh 
... 
Set RS = DC1.Recordset 
' Edit the Recordset object... 
' The SERVER and CONNECT properties are already set from Step 2A. 
Set DC1.SourceRecordset = RS 
... 
DC1.SubmitChanges 
```

## <a name="step-6b--changes-are-sent-to-the-server-with-rdsserverdatafactory"></a><span data-ttu-id="19b88-124">Etapa 6b  As alterações são enviadas para o servidor com o RDSServer.DataFactory</span><span class="sxs-lookup"><span data-stu-id="19b88-124">Step 6b — Changes are sent to the server with RDSServer.DataFactory</span></span>

```vb
 
DF.SubmitChanges"DSN=Pubs", RS 
 
End Sub 
</SCRIPT> 
</BODY> 
</HTML> 
```

<span data-ttu-id="19b88-125">**Esse é o fim do tutorial.**</span><span class="sxs-lookup"><span data-stu-id="19b88-125">**This is the end of the tutorial.**</span></span>

