---
title: Desconectando e reconectando o Recordset
TOCTitle: Disconnecting and Reconnecting the Recordset
ms:assetid: d608d95d-9a4e-17a1-107a-b88b77f3774c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250077(v=office.15)
ms:contentKeyID: 48547975
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 90435606bb0b3059f5769c12fe7cf3cac0c8f9f3
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25465274"
---
# <a name="disconnecting-and-reconnecting-the-recordset"></a><span data-ttu-id="d343a-102">Desconectando e reconectando o Recordset</span><span class="sxs-lookup"><span data-stu-id="d343a-102">Disconnecting and Reconnecting the Recordset</span></span>


<span data-ttu-id="d343a-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="d343a-103">**Applies to**: Access 2013 | Office 2013</span></span>

## <a name="disconnecting-and-reconnecting-the-recordset"></a><span data-ttu-id="d343a-104">Desconectando e reconectando o Recordset</span><span class="sxs-lookup"><span data-stu-id="d343a-104">Disconnecting and Reconnecting the Recordset</span></span>

<span data-ttu-id="d343a-p101">Um dos recursos mais eficientes encontrados no ADO é a capacidade de abrir um **Recordset** no cliente a partir de uma fonte de dados e, em seguida, *desconectar* o **Recordset** dessa fonte. Uma vez desconectado o **Recordset**, a conexão com a fonte de dados poderá ser fechada, liberando assim os recursos no servidor usado para mantê-lo. Você pode continuar a exibir e editar os dados no **Recordset** enquanto ele estiver desconectado e reconectar-se posteriormente à fonte de dados para enviar suas atualizações no modo em lotes.</span><span class="sxs-lookup"><span data-stu-id="d343a-p101">One of the most powerful features found in ADO is the capability to open a client-side **Recordset** from a data source and then *disconnect* the **Recordset** from the data source. Once the **Recordset** has been disconnected, the connection to the data source can be closed, thereby releasing the resources on the server used to maintain it. You can continue to view and edit the data in the **Recordset** while it is disconnected and later reconnect to the data source and send your updates in batch mode.</span></span>

<span data-ttu-id="d343a-p102">Para desconectar um **Recordset**, abra-o com o local de cursor **adUseClient** e defina a propriedade **ActiveConnection** como *Nothing*. (os usuários de C++ devem definir **ActiveConnection** como NULL para se desconectar.)</span><span class="sxs-lookup"><span data-stu-id="d343a-p102">To disconnect a **Recordset**, open it with a cursor location of **adUseClient**, and then set the **ActiveConnection** property equal to *Nothing*. (C++ users should set the **ActiveConnection** equal to NULL to disconnect.)</span></span>

<span data-ttu-id="d343a-110">Usaremos um **Recordset** desconectado posteriormente neste capítulo quando abordarmos a persistência do **Recordset** para lidar com um cenário em que é necessário haver dados em um **Recordset** disponíveis para um aplicativo enquanto o computador cliente não está conectado a uma rede.</span><span class="sxs-lookup"><span data-stu-id="d343a-110">We will use a disconnected **Recordset** later in this chapter when we discuss **Recordset** persistence to address a scenario in which we need to have the data in a **Recordset** available to an application while the client computer is not connected to a network.</span></span>

