---
title: 'Etapa 3: Enviar os dados'
TOCTitle: 'Step 3: Send the Data'
ms:assetid: d22ffe59-179b-fd1a-1211-be1a0d76b02f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250049(v=office.15)
ms:contentKeyID: 48547878
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: ed3e6bfd6fe3b6727055eb264b1261b13d7a5a0b
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25462175"
---
# <a name="step-3-send-the-data"></a>Etapa 3: Enviar os dados


**Aplica-se a**: Access 2013 | Office 2013

## <a name="step-3-send-the-data"></a>Etapa 3: Enviar os dados

Agora que você tem um **Recorset**, você precisa enviá-lo ao cliente, salvando-o como XML no objeto **Response** ASP. Adicione o seguinte código na parte inferior do XMLResponse.asp:

```vb 
 
  Response.ContentType = "text/xml" 
  Response.Expires = 0 
  Response.Buffer = False 
 
 
  Response.Write "<?xml version='1.0'?>" & vbNewLine 
  adoRec.save Response, adPersistXML 
  adoRec.Close 
  Set adoRec=Nothing 
%> 
```

Observe que o objeto de **resposta** do ASP é especificado como destino para o método **Recordset** [Salvar](save-method-ado.md) . O destino do método **Save** pode ser qualquer objeto que ofereça suporte à interface **IStream**, como um objeto [Stream](stream-object-ado.md) ADO ou um nome de arquivo que inclui o caminho completo no qual o **Recordset** deve ser salvo.

Salve e feche o arquivo XMLResponse.asp antes de ir para a próxima etapa. Também copiar o arquivo adovbs de c:\\Program Files\\arquivos comuns\\sistema\\pasta Ado na mesma pasta onde está o arquivo XMLResponse.asp.

**Próximo** [Etapa 4: receber os dados](step-4-receive-and-display-the-data.md)

