---
title: 'Etapa 2: Obter os dados'
TOCTitle: 'Step 2: Get the Data'
ms:assetid: e6be8801-6e57-d287-e8d2-348963706edc
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250171(v=office.15)
ms:contentKeyID: 48548387
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 80dae05dc691343b3c89ce8fd3ccfe72b776984c
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25860326"
---
# <a name="step-2-get-the-data"></a><span data-ttu-id="218ab-102">Etapa 2: Obter os dados</span><span class="sxs-lookup"><span data-stu-id="218ab-102">Step 2: Get the Data</span></span>


<span data-ttu-id="218ab-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="218ab-103">**Applies to**: Access 2013 | Office 2013</span></span>

## <a name="step-2-get-the-data"></a><span data-ttu-id="218ab-104">Etapa 2: Obter os dados</span><span class="sxs-lookup"><span data-stu-id="218ab-104">Step 2: Get the Data</span></span>

<span data-ttu-id="218ab-p101">Nesta etapa, você gravará o código para abrir um **Recordset** ADO e preparar para enviá-lo ao cliente. Abra o arquivo XMLResponse.asp com um editor de texto, como o Bloco de Notas do Windows, e insira o seguinte código:</span><span class="sxs-lookup"><span data-stu-id="218ab-p101">In this step, you will write the code to open an ADO **Recordset** and prepare to send it to the client. Open the file XMLResponse.asp with a text editor, such as Windows Notepad, and insert the following code:</span></span>

```vb 
 
<%@ language="VBScript" %> 
 
<!-- #include file='adovbs.inc' --> 
 
<% 
  Dim strSQL, strCon 
  Dim adoRec  
  Dim adoCon  
  Dim xmlDoc  
 
  ' You will need to change "slqServer" below to the name of the SQL  
  ' server machine to which you want to connect. 
  strCon = "Provider=sqloledb;Data Source=sqlServer;Initial Catalog=Pubs;Integrated Security=SSPI;" 
  Set adoCon = server.createObject("ADODB.Connection") 
  adoCon.Open strCon 
 
  strSQL = "SELECT Title, Price FROM Titles ORDER BY Price" 
  Set adoRec = Server.CreateObject("ADODB.Recordset") 
  adoRec.Open strSQL, adoCon, adOpenStatic, adLockOptimistic, adCmdText 
```

<span data-ttu-id="218ab-107">Certifique-se de alterar o valor do parâmetro fonte de dados no parâmetro no strCon com o nome do seu computador Microsoft SQL Server.</span><span class="sxs-lookup"><span data-stu-id="218ab-107">Be sure to change the value of the Data Source parameter in parameter in strCon to the name of your Microsoft SQL Server computer.</span></span>

<span data-ttu-id="218ab-108">Mantenha o arquivo aberto e vá para a próxima etapa.</span><span class="sxs-lookup"><span data-stu-id="218ab-108">Keep the file open and go on to the next step.</span></span>

### <a name="next-step"></a><span data-ttu-id="218ab-109">Próxima etapa</span><span class="sxs-lookup"><span data-stu-id="218ab-109">Next step</span></span>

[<span data-ttu-id="218ab-110">Etapa 3: Enviar os dados</span><span class="sxs-lookup"><span data-stu-id="218ab-110">Step 3: Send the Data</span></span>](step-3-send-the-data.md)

