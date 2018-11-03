---
title: Mantendo Recordsets hierárquicos
TOCTitle: Persisting hierarchical Recordsets
ms:assetid: 28f48d4a-1c32-7b60-cd65-51fb87c5380e
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249048(v=office.15)
ms:contentKeyID: 48543872
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 55f005818ef8fa44a2ee59542aa220f4d71eb687
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/03/2018
ms.locfileid: "25944981"
---
# <a name="persisting-hierarchical-recordsets"></a><span data-ttu-id="4a227-102">Mantendo Recordsets hierárquicos</span><span class="sxs-lookup"><span data-stu-id="4a227-102">Persisting hierarchical Recordsets</span></span>

<span data-ttu-id="4a227-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="4a227-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="4a227-p101">Você pode salvar um **Recordset** hierárquico em um arquivo tanto no formato ADTG quanto XML, chamando o método [Save](save-method-ado.md). Contudo, duas limitações se aplicam ao salvar **Recordset**s hierárquicos no formato XML: você não pode salvar em XML se o **Recordset** hierárquico contiver atualizações pendentes e nem salvar um **Recordset** hierárquico parametrizado.</span><span class="sxs-lookup"><span data-stu-id="4a227-p101">You can save a hierarchical **Recordset** to a file in either ADTG or XML format by calling the [Save](save-method-ado.md) method. However, two limitations apply when saving hierarchical **Recordset**s in XML format: You cannot save in XML if the hierarchical **Recordset** contains pending updates, and you cannot save a parameterized hierarchical **Recordset**.</span></span>

<span data-ttu-id="4a227-106">Para obter mais informações sobre o provedor de Forma de dados, consulte [Microsoft Data Shaping Service para OLE DB](microsoft-data-shaping-service-for-ole-db-ado-service-provider.md) (ADO) e o Serviço de forma de dados para OLE DB (OLE DB).</span><span class="sxs-lookup"><span data-stu-id="4a227-106">For more information about the Data Shaping provider, see [Microsoft Data Shaping Service for OLE DB](microsoft-data-shaping-service-for-ole-db-ado-service-provider.md) (ADO) and The Data Shaping Service for OLE DB(OLE DB).</span></span>

