---
title: 'Etapa 4: Receber e exibir os dados'
TOCTitle: 'Step 4: Receive and Display the Data'
ms:assetid: a27cc1d8-0ee0-95a5-ad70-88c454c10485
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249749(v=office.15)
ms:contentKeyID: 48546764
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: d2a447b68b8c0eeb18d18050ba8dbbb6f09786ab
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25464661"
---
# <a name="step-4-receive-and-display-the-data"></a><span data-ttu-id="8ddb6-102">Etapa 4: Receber e exibir os dados</span><span class="sxs-lookup"><span data-stu-id="8ddb6-102">Step 4: Receive and Display the Data</span></span>


<span data-ttu-id="8ddb6-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="8ddb6-103">**Applies to**: Access 2013 | Office 2013</span></span>

## <a name="step-4-receive-and-display-the-data"></a><span data-ttu-id="8ddb6-104">Etapa 4: Receber e exibir os dados</span><span class="sxs-lookup"><span data-stu-id="8ddb6-104">Step 4: Receive and Display the Data</span></span>

<span data-ttu-id="8ddb6-p101">Nesta etapa, você criará um arquivo HTML com um objeto [RDS.DataControl](datacontrol-object-rds.md) incorporado que aponta para o arquivo XMLResponse.asp para obter o **Recordset**. Abra o arquivo default.htm com um editor de texto, como o Bloco de Notas do Windows, e adicione o código a seguir. Substitua "sqlserver" no URL pelo nome do seu computador servidor.</span><span class="sxs-lookup"><span data-stu-id="8ddb6-p101">In this step you will create an HTML file with an embedded [RDS.DataControl](datacontrol-object-rds.md) object that points at the XMLResponse.asp file to get the **Recordset**. Open default.htm with a text editor, such as Windows Notepad, and add the code below. Replace "sqlserver" in the URL with the name of your server computer.</span></span>

```html 
 
<HTML> 
<HEAD><TITLE>ADO Recordset Persistence Sample</TITLE></HEAD> 
<BODY> 
 
<TABLE DATASRC="#RDC1" border="1"> 
  <TR> 
<TD><SPAN DATAFLD="title"></SPAN></TD> 
<TD><SPAN DATAFLD="price"></SPAN></TD> 
  </TR> 
</TABLE> 

<OBJECT CLASSID="clsid:BD96C556-65A3-11D0-983A-00C04FC29E33" ID="RDC1"> 
   <PARAM NAME="URL" VALUE="XMLResponse.asp"> 
</OBJECT> 
 
</BODY> 
</HTML> 
```

<span data-ttu-id="8ddb6-108">Feche o arquivo default.htm e salve-o na mesma pasta na qual você salvou o arquivo XMLResponse.asp.</span><span class="sxs-lookup"><span data-stu-id="8ddb6-108">Close the default.htm file and save it to the same folder where you saved XMLResponse.asp.</span></span> <span data-ttu-id="8ddb6-109">Usando o Internet Explorer 4.0 ou posterior, abra a URL https://*sqlserver*/XMLPersist/default.htm e observe os resultados.</span><span class="sxs-lookup"><span data-stu-id="8ddb6-109">Using Internet Explorer 4.0 or later, open the URL https://*sqlserver*/XMLPersist/default.htm and observe the results.</span></span> <span data-ttu-id="8ddb6-110">Os dados são exibidos em uma tabela DHTML vinculada.</span><span class="sxs-lookup"><span data-stu-id="8ddb6-110">The data is displayed in a bound DHTML table.</span></span> <span data-ttu-id="8ddb6-111">Agora, abra a URL https://*sqlserver*/XMLPersist/XMLResponse.asp e observe os resultados.</span><span class="sxs-lookup"><span data-stu-id="8ddb6-111">Now open the URL https://*sqlserver*/XMLPersist/XMLResponse.asp and observe the results.</span></span> <span data-ttu-id="8ddb6-112">O XML é exibido.</span><span class="sxs-lookup"><span data-stu-id="8ddb6-112">The XML is displayed.</span></span>

