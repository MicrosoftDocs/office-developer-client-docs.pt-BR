---
title: Microsoft Cursor Service for OLE DB
TOCTitle: The Microsoft Cursor Service for OLE DB
ms:assetid: 31861eef-9860-c884-3c60-9794def7be78
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249088(v=office.15)
ms:contentKeyID: 48544057
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 9db5617eecff862ad941a4160c4b92bfa09d4c2d
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25885917"
---
# <a name="the-microsoft-cursor-service-for-ole-db"></a><span data-ttu-id="39b64-102">Microsoft Cursor Service for OLE DB</span><span class="sxs-lookup"><span data-stu-id="39b64-102">The Microsoft Cursor Service for OLE DB</span></span>


<span data-ttu-id="39b64-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="39b64-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="39b64-p101">Ao selecionar um cursor do cliente ou definir a propriedade **CursorLocation** como **adUseClient**, você está chamando o Microsoft Cursor Service for OLE DB. Também é possível ver referências ao "Mecanismo de cursor do cliente", que é essencialmente a mesma coisa no contexto do ADO. Esse serviço suplementa as funções de suporte ao cursor dos provedores de dados. Como resultado, pode-se observar uma funcionalidade relativamente uniforme de todos os provedores de dados.</span><span class="sxs-lookup"><span data-stu-id="39b64-p101">When you select a client-side cursor, or set the **CursorLocation** property to **adUseClient**, you are invoking the Microsoft Cursor Service for OLE DB. You might also see references to the "Client Cursor Engine", which is essentially the same thing in the context of ADO. This service supplements the cursor-support functions of data providers. As a result, you can perceive relatively uniform functionality from all data providers.</span></span>

<span data-ttu-id="39b64-p102">O Serviço de cursor para OLE DB disponibiliza as propriedades dinâmicas e aprimora o comportamento de certos métodos. Por exemplo, a propriedade dinâmica **Optimize** permite a criação de índices temporários para facilitar determinadas operações, como o método **Find**.</span><span class="sxs-lookup"><span data-stu-id="39b64-p102">The Cursor Service for OLE DB makes dynamic properties available and enhances the behavior of certain methods. For example, the **Optimize** dynamic property enables the creation of temporary indexes to facilitate certain operations, such as the **Find** method.</span></span>

<span data-ttu-id="39b64-p103">O Serviço de cursor habilita o suporte para atualização em lotes em todos os casos. Além disso, ele simula tipos de cursores com mais recursos, como os cursores dinâmicos, quando um provedor de dados só pode fornecer cursores com menos recursos como os estáticos.</span><span class="sxs-lookup"><span data-stu-id="39b64-p103">The Cursor Service enables support for batch updating in all cases. It also simulates more capable cursor types, such as dynamic cursors, when a data provider can only supply less capable cursors, such as static cursors.</span></span>

