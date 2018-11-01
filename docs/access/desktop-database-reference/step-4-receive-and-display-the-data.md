---
title: 'Etapa 4: Receber e exibir os dados'
TOCTitle: 'Step 4: Receive and Display the Data'
ms:assetid: a27cc1d8-0ee0-95a5-ad70-88c454c10485
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249749(v=office.15)
ms:contentKeyID: 48546764
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 03a089e600799e1ac5fa85886ee6a16e1dd86026
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25869075"
---
# <a name="step-4-receive-and-display-the-data"></a>Etapa 4: Receber e exibir os dados


**Aplica-se a**: Access 2013, o Office 2013

## <a name="step-4-receive-and-display-the-data"></a>Etapa 4: Receber e exibir os dados

Nesta etapa, você criará um arquivo HTML com um objeto [RDS.DataControl](datacontrol-object-rds.md) incorporado que aponta para o arquivo XMLResponse.asp para obter o **Recordset**. Abra o arquivo default.htm com um editor de texto, como o Bloco de Notas do Windows, e adicione o código a seguir. Substitua "sqlserver" no URL pelo nome do seu computador servidor.

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

Feche o arquivo default.htm e salve-o na mesma pasta na qual você salvou o arquivo XMLResponse.asp. Usando o Internet Explorer 4.0 ou posterior, abra a URL https://*sqlserver*/XMLPersist/default.htm e observe os resultados. Os dados são exibidos em uma tabela DHTML vinculada. Agora, abra a URL https://*sqlserver*/XMLPersist/XMLResponse.asp e observe os resultados. O XML é exibido.

