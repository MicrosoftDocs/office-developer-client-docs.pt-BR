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
# <a name="step-2-get-the-data"></a>Etapa 2: Obter os dados


**Aplica-se a**: Access 2013 | Office 2013

## <a name="step-2-get-the-data"></a>Etapa 2: Obter os dados

Nesta etapa, você gravará o código para abrir um **Recordset** ADO e preparar para enviá-lo ao cliente. Abra o arquivo XMLResponse.asp com um editor de texto, como o Bloco de Notas do Windows, e insira o seguinte código:

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

Certifique-se de alterar o valor do parâmetro fonte de dados no parâmetro no strCon com o nome do seu computador Microsoft SQL Server.

Mantenha o arquivo aberto e vá para a próxima etapa.

### <a name="next-step"></a>Próxima etapa

[Etapa 3: Enviar os dados](step-3-send-the-data.md)

