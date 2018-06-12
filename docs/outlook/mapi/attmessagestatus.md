---
title: attMessageStatus
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 8f55470a-65b3-4210-a7d2-9031cb17ca80
description: '�ltima altera��o: segunda-feira, 9 de mar�o de 2015'
ms.openlocfilehash: 158e4db4b0f80b80385e85c8afa16fa515dc61b1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766213"
---
# <a name="attmessagestatus"></a><span data-ttu-id="25af2-103">attMessageStatus</span><span class="sxs-lookup"><span data-stu-id="25af2-103">attMessageStatus</span></span>

  
  
<span data-ttu-id="25af2-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="25af2-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="25af2-105">Sinalizadores de mensagem MAPI são mapeadas para TNEF sinalizadores para preservar a compatibilidade com versões anteriores.</span><span class="sxs-lookup"><span data-stu-id="25af2-105">MAPI message flags are mapped to TNEF flags to preserve backward compatibility.</span></span> <span data-ttu-id="25af2-106">Todos os sinalizadores são agrupados e codificados em um único byte.</span><span class="sxs-lookup"><span data-stu-id="25af2-106">All the flags are grouped together and encoded in a single byte.</span></span> <span data-ttu-id="25af2-107">Os mapeamentos são:</span><span class="sxs-lookup"><span data-stu-id="25af2-107">The mappings are as follows:</span></span>
  
|<span data-ttu-id="25af2-108">**Sinalizadores de mensagem MAPI**</span><span class="sxs-lookup"><span data-stu-id="25af2-108">**MAPI message flags**</span></span>|<span data-ttu-id="25af2-109">**Sinalizadores TNEF**</span><span class="sxs-lookup"><span data-stu-id="25af2-109">**TNEF flags**</span></span>|
|:-----|:-----|
|<span data-ttu-id="25af2-110">MSGFLAG_READ</span><span class="sxs-lookup"><span data-stu-id="25af2-110">MSGFLAG_READ</span></span>  <br/> |<span data-ttu-id="25af2-111">fmsRead</span><span class="sxs-lookup"><span data-stu-id="25af2-111">fmsRead</span></span>  <br/> |
|<span data-ttu-id="25af2-112">MSGFLAG_UNMODIFED</span><span class="sxs-lookup"><span data-stu-id="25af2-112">MSGFLAG_UNMODIFED</span></span>  <br/> |<span data-ttu-id="25af2-113">~ fmsModified</span><span class="sxs-lookup"><span data-stu-id="25af2-113">~fmsModified</span></span>  <br/> |
|<span data-ttu-id="25af2-114">MSGFLAG_SUBMIT</span><span class="sxs-lookup"><span data-stu-id="25af2-114">MSGFLAG_SUBMIT</span></span>  <br/> |<span data-ttu-id="25af2-115">fmsSubmitted</span><span class="sxs-lookup"><span data-stu-id="25af2-115">fmsSubmitted</span></span>  <br/> |
|<span data-ttu-id="25af2-116">MSGFLAG_HASATTACH</span><span class="sxs-lookup"><span data-stu-id="25af2-116">MSGFLAG_HASATTACH</span></span>  <br/> |<span data-ttu-id="25af2-117">fmsHasAttach</span><span class="sxs-lookup"><span data-stu-id="25af2-117">fmsHasAttach</span></span>  <br/> |
|<span data-ttu-id="25af2-118">MSGFLAG_UNSENT</span><span class="sxs-lookup"><span data-stu-id="25af2-118">MSGFLAG_UNSENT</span></span>  <br/> |<span data-ttu-id="25af2-119">fmsLocal</span><span class="sxs-lookup"><span data-stu-id="25af2-119">fmsLocal</span></span>  <br/> |
   
<span data-ttu-id="25af2-120">Esses sinalizadores são definidos no TNEF. Arquivo de cabeçalho H.</span><span class="sxs-lookup"><span data-stu-id="25af2-120">These flags are defined in the TNEF.H header file.</span></span>
  

