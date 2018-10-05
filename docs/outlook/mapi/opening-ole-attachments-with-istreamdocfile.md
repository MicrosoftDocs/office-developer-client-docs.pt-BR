---
title: Abertura de anexos OLE com IStreamDocfile
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: f91df63c-ff6d-4c63-a665-5bcfdabe7e0e
description: 'Modificado pela última vez: 06 de julho de 2012'
ms.openlocfilehash: 2de13be34e8d81f88bfba872dda6e5534eb431bd
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25386548"
---
# <a name="opening-ole-attachments-with-istreamdocfile"></a><span data-ttu-id="b123e-103">Abertura de anexos OLE com IStreamDocfile</span><span class="sxs-lookup"><span data-stu-id="b123e-103">Opening OLE attachments with IStreamDocfile</span></span>

<span data-ttu-id="b123e-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b123e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b123e-105">Ao abrir um anexo do objeto OLE, use a interface de **IStreamDocfile** ao invés [IStream](https://msdn.microsoft.com/library/windows/desktop/aa380034%28v=vs.85%29.aspx) ou [IStorage](https://msdn.microsoft.com/library/windows/desktop/aa380015%28v=vs.85%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="b123e-105">When opening an OLE object attachment, use the **IStreamDocfile** interface rather than [IStream](https://msdn.microsoft.com/library/windows/desktop/aa380034%28v=vs.85%29.aspx) or [IStorage](https://msdn.microsoft.com/library/windows/desktop/aa380015%28v=vs.85%29.aspx).</span></span> 

<span data-ttu-id="b123e-106">**IStreamDocfile** fornece acesso direto ao objeto usando armazenamento estruturado, eliminando a necessidade de realizar uma operação de cópia e reduz a sobrecarga.</span><span class="sxs-lookup"><span data-stu-id="b123e-106">**IStreamDocfile** provides direct access to the object using structured storage, eliminating the need to perform a copy operation and reducing overhead.</span></span> <span data-ttu-id="b123e-107">**IStreamDocfile** é uma implementação específica da **IStream** com o conteúdo do stream garantido a ser formatado como armazenamento estruturado.</span><span class="sxs-lookup"><span data-stu-id="b123e-107">**IStreamDocfile** is a specific implementation of **IStream** with the content of the stream guaranteed to be formatted as structured storage.</span></span> <span data-ttu-id="b123e-108">**IStreamDocfile** é implementado por provedores de armazenamento de mensagem.</span><span class="sxs-lookup"><span data-stu-id="b123e-108">**IStreamDocfile** is implemented by message store providers.</span></span> 
  

