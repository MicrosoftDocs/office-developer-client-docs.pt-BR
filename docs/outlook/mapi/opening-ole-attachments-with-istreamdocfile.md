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
ms.openlocfilehash: 33e5b9e0112f562b192400498764a10682d006a6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19768194"
---
# <a name="opening-ole-attachments-with-istreamdocfile"></a><span data-ttu-id="ff53c-103">Abertura de anexos OLE com IStreamDocfile</span><span class="sxs-lookup"><span data-stu-id="ff53c-103">Opening OLE attachments with IStreamDocfile</span></span>

<span data-ttu-id="ff53c-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="ff53c-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="ff53c-105">Ao abrir um anexo do objeto OLE, use a interface de **IStreamDocfile** ao invés [IStream](http://msdn.microsoft.com/en-us/library/windows/desktop/aa380034%28v=vs.85%29.aspx) ou [IStorage](http://msdn.microsoft.com/en-us/library/windows/desktop/aa380015%28v=vs.85%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="ff53c-105">When opening an OLE object attachment, use the **IStreamDocfile** interface rather than [IStream](http://msdn.microsoft.com/en-us/library/windows/desktop/aa380034%28v=vs.85%29.aspx) or [IStorage](http://msdn.microsoft.com/en-us/library/windows/desktop/aa380015%28v=vs.85%29.aspx).</span></span> 

<span data-ttu-id="ff53c-106">**IStreamDocfile** fornece acesso direto ao objeto usando armazenamento estruturado, eliminando a necessidade de realizar uma operação de cópia e reduz a sobrecarga.</span><span class="sxs-lookup"><span data-stu-id="ff53c-106">**IStreamDocfile** provides direct access to the object using structured storage, eliminating the need to perform a copy operation and reducing overhead.</span></span> <span data-ttu-id="ff53c-107">**IStreamDocfile** é uma implementação específica da **IStream** com o conteúdo do stream garantido a ser formatado como armazenamento estruturado.</span><span class="sxs-lookup"><span data-stu-id="ff53c-107">**IStreamDocfile** is a specific implementation of **IStream** with the content of the stream guaranteed to be formatted as structured storage.</span></span> <span data-ttu-id="ff53c-108">**IStreamDocfile** é implementado por provedores de armazenamento de mensagem.</span><span class="sxs-lookup"><span data-stu-id="ff53c-108">**IStreamDocfile** is implemented by message store providers.</span></span> 
  

