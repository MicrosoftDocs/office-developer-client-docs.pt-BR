---
title: attMessageStatus
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 8f55470a-65b3-4210-a7d2-9031cb17ca80
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: d4dc72309ff090317b2353cab0b4fc2c5be41181
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430312"
---
# <a name="attmessagestatus"></a><span data-ttu-id="b70b1-103">attMessageStatus</span><span class="sxs-lookup"><span data-stu-id="b70b1-103">attMessageStatus</span></span>

  
  
<span data-ttu-id="b70b1-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b70b1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b70b1-105">Sinalizadores de mensagem MAPI são mapeados para sinalizadores TNEF para preservar a compatibilidade com compatibilidade.</span><span class="sxs-lookup"><span data-stu-id="b70b1-105">MAPI message flags are mapped to TNEF flags to preserve backward compatibility.</span></span> <span data-ttu-id="b70b1-106">Todos os sinalizadores são agrupados e codificados em um único byte.</span><span class="sxs-lookup"><span data-stu-id="b70b1-106">All the flags are grouped together and encoded in a single byte.</span></span> <span data-ttu-id="b70b1-107">Os mapeamentos são os seguinte:</span><span class="sxs-lookup"><span data-stu-id="b70b1-107">The mappings are as follows:</span></span>
  
|<span data-ttu-id="b70b1-108">**Sinalizadores de mensagem MAPI**</span><span class="sxs-lookup"><span data-stu-id="b70b1-108">**MAPI message flags**</span></span>|<span data-ttu-id="b70b1-109">**Sinalizadores TNEF**</span><span class="sxs-lookup"><span data-stu-id="b70b1-109">**TNEF flags**</span></span>|
|:-----|:-----|
|<span data-ttu-id="b70b1-110">MSGFLAG_READ</span><span class="sxs-lookup"><span data-stu-id="b70b1-110">MSGFLAG_READ</span></span>  <br/> |<span data-ttu-id="b70b1-111">fmsRead</span><span class="sxs-lookup"><span data-stu-id="b70b1-111">fmsRead</span></span>  <br/> |
|<span data-ttu-id="b70b1-112">MSGFLAG_UNMODIFED</span><span class="sxs-lookup"><span data-stu-id="b70b1-112">MSGFLAG_UNMODIFED</span></span>  <br/> |<span data-ttu-id="b70b1-113">~fmsModified</span><span class="sxs-lookup"><span data-stu-id="b70b1-113">~fmsModified</span></span>  <br/> |
|<span data-ttu-id="b70b1-114">MSGFLAG_SUBMIT</span><span class="sxs-lookup"><span data-stu-id="b70b1-114">MSGFLAG_SUBMIT</span></span>  <br/> |<span data-ttu-id="b70b1-115">fmsSubmitted</span><span class="sxs-lookup"><span data-stu-id="b70b1-115">fmsSubmitted</span></span>  <br/> |
|<span data-ttu-id="b70b1-116">MSGFLAG_HASATTACH</span><span class="sxs-lookup"><span data-stu-id="b70b1-116">MSGFLAG_HASATTACH</span></span>  <br/> |<span data-ttu-id="b70b1-117">fmsHasAttach</span><span class="sxs-lookup"><span data-stu-id="b70b1-117">fmsHasAttach</span></span>  <br/> |
|<span data-ttu-id="b70b1-118">MSGFLAG_UNSENT</span><span class="sxs-lookup"><span data-stu-id="b70b1-118">MSGFLAG_UNSENT</span></span>  <br/> |<span data-ttu-id="b70b1-119">fmsLocal</span><span class="sxs-lookup"><span data-stu-id="b70b1-119">fmsLocal</span></span>  <br/> |
   
<span data-ttu-id="b70b1-120">Esses sinalizadores são definidos no TNEF. Arquivo de header H.</span><span class="sxs-lookup"><span data-stu-id="b70b1-120">These flags are defined in the TNEF.H header file.</span></span>
  

