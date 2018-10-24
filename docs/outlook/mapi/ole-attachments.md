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
ms.openlocfilehash: ccd4a77e74a4a4cbdfcd8474d4cc00d0d0516839
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22584636"
---
# <a name="ole-attachments"></a><span data-ttu-id="17870-103">Anexos OLE</span><span class="sxs-lookup"><span data-stu-id="17870-103">OLE Attachments</span></span>

  
  
<span data-ttu-id="17870-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="17870-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="17870-105">Anexos que sejam objetos OLE são codificados como objetos stream de OLE 1 para compatibilidade com versões anteriores.</span><span class="sxs-lookup"><span data-stu-id="17870-105">Attachments that are OLE objects are encoded as OLE 1 stream objects for backward compatibility.</span></span> <span data-ttu-id="17870-106">Se o objeto original é realmente um objeto OLE 2 **IStorage** , o objeto deve ser convertido para um fluxo de OLE 1.</span><span class="sxs-lookup"><span data-stu-id="17870-106">If the original object is really an OLE 2 **IStorage** object, then the object must be converted to an OLE 1 stream.</span></span> <span data-ttu-id="17870-107">Essa conversão é realizada usando a função **OleConvertIStorageToOLESTREAM** , que é parte das bibliotecas Win32 OLE.</span><span class="sxs-lookup"><span data-stu-id="17870-107">This conversion is performed using the **OleConvertIStorageToOLESTREAM** function, which is part of the Win32 OLE libraries.</span></span> 
  

