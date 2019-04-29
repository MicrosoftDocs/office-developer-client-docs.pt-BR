---
title: Anexos OLE
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: febb6a5e-7c40-4f21-806e-7f827d1c37cf
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: fb716ce014ec3c4b21ce2b021c1a9f6f291d511c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417144"
---
# <a name="ole-attachments"></a><span data-ttu-id="e467c-103">Anexos OLE</span><span class="sxs-lookup"><span data-stu-id="e467c-103">OLE Attachments</span></span>

  
  
<span data-ttu-id="e467c-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e467c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e467c-105">Anexos que são objetos OLE são codificados como objetos Stream de OLE 1 para compatibilidade com versões anteriores.</span><span class="sxs-lookup"><span data-stu-id="e467c-105">Attachments that are OLE objects are encoded as OLE 1 stream objects for backward compatibility.</span></span> <span data-ttu-id="e467c-106">Se o objeto original for realmente um objeto **ISTORAGE** OLE 2, o objeto deverá ser convertido em um fluxo OLE 1.</span><span class="sxs-lookup"><span data-stu-id="e467c-106">If the original object is really an OLE 2 **IStorage** object, then the object must be converted to an OLE 1 stream.</span></span> <span data-ttu-id="e467c-107">Essa conversão é realizada usando a função **OleConvertIStorageToOLESTREAM** , que faz parte das bibliotecas OLE do Win32.</span><span class="sxs-lookup"><span data-stu-id="e467c-107">This conversion is performed using the **OleConvertIStorageToOLESTREAM** function, which is part of the Win32 OLE libraries.</span></span> 
  

