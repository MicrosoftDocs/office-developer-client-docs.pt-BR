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
# <a name="step-3-send-the-data"></a><span data-ttu-id="5be8d-102">Etapa 3: Enviar os dados</span><span class="sxs-lookup"><span data-stu-id="5be8d-102">Step 3: Send the Data</span></span>


<span data-ttu-id="5be8d-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="5be8d-103">**Applies to**: Access 2013 | Office 2013</span></span>

## <a name="step-3-send-the-data"></a><span data-ttu-id="5be8d-104">Etapa 3: Enviar os dados</span><span class="sxs-lookup"><span data-stu-id="5be8d-104">Step 3: Send the Data</span></span>

<span data-ttu-id="5be8d-p101">Agora que você tem um **Recorset**, você precisa enviá-lo ao cliente, salvando-o como XML no objeto **Response** ASP. Adicione o seguinte código na parte inferior do XMLResponse.asp:</span><span class="sxs-lookup"><span data-stu-id="5be8d-p101">Now that you have a **Recordset**, you need to send it to the client by saving it as XML to the ASP **Response** object. Add the following code to the bottom of XMLResponse.asp:</span></span>

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

<span data-ttu-id="5be8d-107">Observe que o objeto de **resposta** do ASP é especificado como destino para o método **Recordset** [Salvar](save-method-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="5be8d-107">Notice that the ASP **Response** object is specified as the destination for the **Recordset** [Save](save-method-ado.md) method.</span></span> <span data-ttu-id="5be8d-108">O destino do método **Save** pode ser qualquer objeto que ofereça suporte à interface **IStream**, como um objeto [Stream](stream-object-ado.md) ADO ou um nome de arquivo que inclui o caminho completo no qual o **Recordset** deve ser salvo.</span><span class="sxs-lookup"><span data-stu-id="5be8d-108">The destination of the **Save** method can be any object that supports the **IStream** interface, such as an ADO [Stream](stream-object-ado.md) object, or a file name that includes the complete path to which the **Recordset** is to be saved.</span></span>

<span data-ttu-id="5be8d-109">Salve e feche o arquivo XMLResponse.asp antes de ir para a próxima etapa.</span><span class="sxs-lookup"><span data-stu-id="5be8d-109">Save and close XMLResponse.asp before going to the next step.</span></span> <span data-ttu-id="5be8d-110">Também copiar o arquivo adovbs de c:\\Program Files\\arquivos comuns\\sistema\\pasta Ado na mesma pasta onde está o arquivo XMLResponse.asp.</span><span class="sxs-lookup"><span data-stu-id="5be8d-110">Also copy the adovbs.inc file from C:\\Program Files\\Common Files\\System\\Ado folder to the same folder where you have the XMLResponse.asp file.</span></span>

<span data-ttu-id="5be8d-111">**Próximo** [Etapa 4: receber os dados](step-4-receive-and-display-the-data.md)</span><span class="sxs-lookup"><span data-stu-id="5be8d-111">**Next** [Step 4: Receive the Data](step-4-receive-and-display-the-data.md)</span></span>

