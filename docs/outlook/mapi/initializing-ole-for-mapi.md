---
title: Iniciar OLE para MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 53b65299-69f8-4fc0-8d9b-f666e814aaac
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 87310916f4a54b308f0599ec5c1a4a3bfe83c376
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317224"
---
# <a name="initializing-ole-for-mapi"></a><span data-ttu-id="aa5e9-103">Iniciar OLE para MAPI</span><span class="sxs-lookup"><span data-stu-id="aa5e9-103">Initializing OLE for MAPI</span></span>

  
  
<span data-ttu-id="aa5e9-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="aa5e9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="aa5e9-105">Se você também usar OLE, chame a função [OLE OleInitialize](https://msdn.microsoft.com/library/ms690134%28v=VS.85%29.aspx) para inicializar as bibliotecas OLE.</span><span class="sxs-lookup"><span data-stu-id="aa5e9-105">If you also use OLE, call the OLE function [OleInitialize](https://msdn.microsoft.com/library/ms690134%28v=VS.85%29.aspx) to initialize the OLE libraries.</span></span> <span data-ttu-id="aa5e9-106">**OleInitialize inicializa** dados globais para a sessão e prepara as bibliotecas OLE para aceitar chamadas.</span><span class="sxs-lookup"><span data-stu-id="aa5e9-106">**OleInitialize** initializes global data for the session and prepares the OLE libraries to accept calls.</span></span> <span data-ttu-id="aa5e9-107">Para obter informações sobre como **chamar OleInitialize,** consulte o SDK do Windows.</span><span class="sxs-lookup"><span data-stu-id="aa5e9-107">For information about calling **OleInitialize**, see the Windows SDK.</span></span>
  

