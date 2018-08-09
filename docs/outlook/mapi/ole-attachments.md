---
title: Anexos OLE
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: febb6a5e-7c40-4f21-806e-7f827d1c37cf
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: b95b83ad7eedff577e4c36365c9e451f4b458173
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19768160"
---
# <a name="ole-attachments"></a><span data-ttu-id="ad2ed-103">Anexos OLE</span><span class="sxs-lookup"><span data-stu-id="ad2ed-103">OLE Attachments</span></span>

  
  
<span data-ttu-id="ad2ed-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="ad2ed-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="ad2ed-105">Anexos que sejam objetos OLE são codificados como objetos stream de OLE 1 para compatibilidade com versões anteriores.</span><span class="sxs-lookup"><span data-stu-id="ad2ed-105">Attachments that are OLE objects are encoded as OLE 1 stream objects for backward compatibility.</span></span> <span data-ttu-id="ad2ed-106">Se o objeto original é realmente um objeto OLE 2 **IStorage** , o objeto deve ser convertido para um fluxo de OLE 1.</span><span class="sxs-lookup"><span data-stu-id="ad2ed-106">If the original object is really an OLE 2 **IStorage** object, then the object must be converted to an OLE 1 stream.</span></span> <span data-ttu-id="ad2ed-107">Essa conversão é realizada usando a função **OleConvertIStorageToOLESTREAM** , que é parte das bibliotecas Win32 OLE.</span><span class="sxs-lookup"><span data-stu-id="ad2ed-107">This conversion is performed using the **OleConvertIStorageToOLESTREAM** function, which is part of the Win32 OLE libraries.</span></span> 
  

