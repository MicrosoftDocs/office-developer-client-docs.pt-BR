---
title: Iniciar OLE para MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 53b65299-69f8-4fc0-8d9b-f666e814aaac
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 87310916f4a54b308f0599ec5c1a4a3bfe83c376
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25388410"
---
# <a name="initializing-ole-for-mapi"></a><span data-ttu-id="d09d6-103">Iniciar OLE para MAPI</span><span class="sxs-lookup"><span data-stu-id="d09d6-103">Initializing OLE for MAPI</span></span>

  
  
<span data-ttu-id="d09d6-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d09d6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d09d6-105">Se você usar também o OLE, chame a função OLE [OleInitialize](https://msdn.microsoft.com/library/ms690134%28v=VS.85%29.aspx) para inicializar as bibliotecas OLE.</span><span class="sxs-lookup"><span data-stu-id="d09d6-105">If you also use OLE, call the OLE function [OleInitialize](https://msdn.microsoft.com/library/ms690134%28v=VS.85%29.aspx) to initialize the OLE libraries.</span></span> <span data-ttu-id="d09d6-106">**OleInitialize** inicializa dados globais para a sessão e prepara as bibliotecas OLE aceite as chamadas.</span><span class="sxs-lookup"><span data-stu-id="d09d6-106">**OleInitialize** initializes global data for the session and prepares the OLE libraries to accept calls.</span></span> <span data-ttu-id="d09d6-107">Para obter informações sobre a chamada **OleInitialize**, consulte o SDK do Windows.</span><span class="sxs-lookup"><span data-stu-id="d09d6-107">For information about calling **OleInitialize**, see the Windows SDK.</span></span>
  

