---
title: Abrir anexos OLE com IStreamDocfile
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: f91df63c-ff6d-4c63-a665-5bcfdabe7e0e
description: 'Última modificação: 06 de julho de 2012'
ms.openlocfilehash: 2de13be34e8d81f88bfba872dda6e5534eb431bd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326226"
---
# <a name="opening-ole-attachments-with-istreamdocfile"></a><span data-ttu-id="86712-103">Abrir anexos OLE com IStreamDocfile</span><span class="sxs-lookup"><span data-stu-id="86712-103">Opening OLE attachments with IStreamDocfile</span></span>

<span data-ttu-id="86712-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="86712-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="86712-105">Ao abrir um anexo de objeto OLE, use a interface **IStreamDocfile** , em vez de [IStream](https://msdn.microsoft.com/library/windows/desktop/aa380034%28v=vs.85%29.aspx) ou [IStorage](https://msdn.microsoft.com/library/windows/desktop/aa380015%28v=vs.85%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="86712-105">When opening an OLE object attachment, use the **IStreamDocfile** interface rather than [IStream](https://msdn.microsoft.com/library/windows/desktop/aa380034%28v=vs.85%29.aspx) or [IStorage](https://msdn.microsoft.com/library/windows/desktop/aa380015%28v=vs.85%29.aspx).</span></span> 

<span data-ttu-id="86712-106">O **IStreamDocfile** fornece acesso direto ao objeto usando o armazenamento estruturado, eliminando a necessidade de executar uma operação de cópia e reduzindo a sobrecarga.</span><span class="sxs-lookup"><span data-stu-id="86712-106">**IStreamDocfile** provides direct access to the object using structured storage, eliminating the need to perform a copy operation and reducing overhead.</span></span> <span data-ttu-id="86712-107">**IStreamDocfile** é uma implementação específica de **IStream** com o conteúdo do Stream garantido para ser formatado como armazenamento estruturado.</span><span class="sxs-lookup"><span data-stu-id="86712-107">**IStreamDocfile** is a specific implementation of **IStream** with the content of the stream guaranteed to be formatted as structured storage.</span></span> <span data-ttu-id="86712-108">O **IStreamDocfile** é implementado por provedores de repositório de mensagens.</span><span class="sxs-lookup"><span data-stu-id="86712-108">**IStreamDocfile** is implemented by message store providers.</span></span> 
  

