---
title: Objeto DataSpace (RDS)
TOCTitle: DataSpace object (RDS)
ms:assetid: 7db181d5-422b-49fe-b6af-a20f5da520ff
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249527(v=office.15)
ms:contentKeyID: 48545862
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: f77617d4ddfb0160b8a418f55582a380067fde70
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294460"
---
# <a name="dataspace-object-rds"></a><span data-ttu-id="07fbf-102">Objeto DataSpace (RDS)</span><span class="sxs-lookup"><span data-stu-id="07fbf-102">DataSpace object (RDS)</span></span>

<span data-ttu-id="07fbf-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="07fbf-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="07fbf-104">Cria proxies do cliente para personalizar os objetos corporativos localizados na camada intermediária.</span><span class="sxs-lookup"><span data-stu-id="07fbf-104">Creates client-side proxies to custom business objects located on the middle tier.</span></span>

## <a name="remarks"></a><span data-ttu-id="07fbf-105">Comentários</span><span class="sxs-lookup"><span data-stu-id="07fbf-105">Remarks</span></span>

<span data-ttu-id="07fbf-p101">O RDS precisa de proxies do objeto, de modo que o componente do cliente possa comunicar os objetos corporativos localizados na camada intermediária. Os proxies facilitam a compactação, a descompactação e o transporte (a disposição) dos dados [Recordset](recordset-object-ado.md) do aplicativo por meio do processo ou dos limites da máquina.</span><span class="sxs-lookup"><span data-stu-id="07fbf-p101">Remote Data Service needs business object proxies so that client-side component can communicate with business objects located on the middle tier. Proxies facilitate the packaging, unpackaging, and transport (marshaling) of the application's [Recordset](recordset-object-ado.md) data across process or machine boundaries.</span></span>

<span data-ttu-id="07fbf-p102">O RDS usa o método **CreateObject** do objeto [RDS.DataSpace](createobject-method-rds.md) para criar os proxies do objeto corporativo. O proxy do objeto corporativo será criado dinamicamente assim que for criada uma instância da contraparte do objeto corporativo da camada intermediária. O RDS oferece suporte aos seguintes protocolos: HTTP, HTTPS (HTTP Secure Sockets), DCOM, e em processo (os componentes do cliente e o objeto corporativo residem no mesmo computador).</span><span class="sxs-lookup"><span data-stu-id="07fbf-p102">Remote Data Service uses the **RDS.DataSpace** object's [CreateObject](createobject-method-rds.md) method to create business object proxies. The business object proxy is dynamically created whenever an instance of its middle-tier business object counterpart is created. Remote Data Service supports the following protocols: HTTP, HTTPS (HTTP Secure Sockets), DCOM, and in-process (client components and the business object reside on the same computer).</span></span>

> [!NOTE]
> <span data-ttu-id="07fbf-p103">[!OBSERVAçãO] O RDS se comportará de uma maneira "sem estado" quando o objeto **RDS.DataSpace** usar os protocolos HTTP ou HTTPS, ou seja, qualquer informação interna sobre a solicitação do cliente será descartada depois que o servidor retornar a resposta.</span><span class="sxs-lookup"><span data-stu-id="07fbf-p103">RDS behaves in a "stateless" manner when the **RDS.DataSpace** object uses the HTTP or HTTPS protocols. That is, any internal information about a client request is discarded after the server returns a response.</span></span>

<span data-ttu-id="07fbf-p104">Embora o objeto corporativo pareça existir durante a vida útil do proxy do objeto corporativo, na verdade, esse objeto existe somente até que uma resposta seja enviada para uma solicitação. Quando uma solicitação for emitida (ou seja, o método for chamado no objeto corporativo), o proxy abrirá uma nova conexão com o servidor e este criará uma nova instância do objeto corporativo. Depois que o objeto corporativo responder à solicitação, o servidor destruirá o objeto corporativo e fechará a conexão.</span><span class="sxs-lookup"><span data-stu-id="07fbf-p104">Although the business object appears to exist for the lifetime of the business object proxy, the business object actually exists only until a response is sent to a request. When a request is issued (that is, a method is invoked on the business object), the proxy opens a new connection to the server and the server creates a new instance of the business object. After the business object responds to the request, the server destroys the business object and closes the connection.</span></span>

<span data-ttu-id="07fbf-p105">Esse comportamento significa que não é possível passar dados de uma solicitação para outra usando a propriedade ou a variável do objeto corporativo. Use algum outro mecanismo, como um arquivo ou um argumento de método, para permanecer com os dados no estado.</span><span class="sxs-lookup"><span data-stu-id="07fbf-p105">This behavior means you cannot pass data from one request to another using a business object property or variable. You must employ some other mechanism, such as a file or a method argument, to persist state data.</span></span>

<span data-ttu-id="07fbf-118">A ID de classe do objeto **RDS.DataSpace** é BD96C556-65A3-11D0-983A-00C04FC29E36.</span><span class="sxs-lookup"><span data-stu-id="07fbf-118">The class ID for the **RDS.DataSpace** object is BD96C556-65A3-11D0-983A-00C04FC29E36.</span></span>

