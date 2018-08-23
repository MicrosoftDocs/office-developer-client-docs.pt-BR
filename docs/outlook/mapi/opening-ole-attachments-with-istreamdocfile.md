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
ms.openlocfilehash: 1e11d9f663384f00e7fd867802ef63afe1dd7e9e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592735"
---
# <a name="opening-ole-attachments-with-istreamdocfile"></a><span data-ttu-id="30ac7-103">Abertura de anexos OLE com IStreamDocfile</span><span class="sxs-lookup"><span data-stu-id="30ac7-103">Opening OLE attachments with IStreamDocfile</span></span>

<span data-ttu-id="30ac7-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="30ac7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="30ac7-105">Ao abrir um anexo do objeto OLE, use a interface de **IStreamDocfile** ao invés [IStream](http://msdn.microsoft.com/en-us/library/windows/desktop/aa380034%28v=vs.85%29.aspx) ou [IStorage](http://msdn.microsoft.com/en-us/library/windows/desktop/aa380015%28v=vs.85%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="30ac7-105">When opening an OLE object attachment, use the **IStreamDocfile** interface rather than [IStream](http://msdn.microsoft.com/en-us/library/windows/desktop/aa380034%28v=vs.85%29.aspx) or [IStorage](http://msdn.microsoft.com/en-us/library/windows/desktop/aa380015%28v=vs.85%29.aspx).</span></span> 

<span data-ttu-id="30ac7-106">**IStreamDocfile** fornece acesso direto ao objeto usando armazenamento estruturado, eliminando a necessidade de realizar uma operação de cópia e reduz a sobrecarga.</span><span class="sxs-lookup"><span data-stu-id="30ac7-106">**IStreamDocfile** provides direct access to the object using structured storage, eliminating the need to perform a copy operation and reducing overhead.</span></span> <span data-ttu-id="30ac7-107">**IStreamDocfile** é uma implementação específica da **IStream** com o conteúdo do stream garantido a ser formatado como armazenamento estruturado.</span><span class="sxs-lookup"><span data-stu-id="30ac7-107">**IStreamDocfile** is a specific implementation of **IStream** with the content of the stream guaranteed to be formatted as structured storage.</span></span> <span data-ttu-id="30ac7-108">**IStreamDocfile** é implementado por provedores de armazenamento de mensagem.</span><span class="sxs-lookup"><span data-stu-id="30ac7-108">**IStreamDocfile** is implemented by message store providers.</span></span> 
  

