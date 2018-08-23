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
ms.openlocfilehash: 704707b34fb4532f0e60636df31edbae1a939f35
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22565743"
---
# <a name="attmessagestatus"></a><span data-ttu-id="3508e-103">attMessageStatus</span><span class="sxs-lookup"><span data-stu-id="3508e-103">attMessageStatus</span></span>

  
  
<span data-ttu-id="3508e-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3508e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3508e-105">Sinalizadores de mensagem MAPI são mapeadas para TNEF sinalizadores para preservar a compatibilidade com versões anteriores.</span><span class="sxs-lookup"><span data-stu-id="3508e-105">MAPI message flags are mapped to TNEF flags to preserve backward compatibility.</span></span> <span data-ttu-id="3508e-106">Todos os sinalizadores são agrupados e codificados em um único byte.</span><span class="sxs-lookup"><span data-stu-id="3508e-106">All the flags are grouped together and encoded in a single byte.</span></span> <span data-ttu-id="3508e-107">Os mapeamentos são:</span><span class="sxs-lookup"><span data-stu-id="3508e-107">The mappings are as follows:</span></span>
  
|<span data-ttu-id="3508e-108">**Sinalizadores de mensagem MAPI**</span><span class="sxs-lookup"><span data-stu-id="3508e-108">**MAPI message flags**</span></span>|<span data-ttu-id="3508e-109">**Sinalizadores TNEF**</span><span class="sxs-lookup"><span data-stu-id="3508e-109">**TNEF flags**</span></span>|
|:-----|:-----|
|<span data-ttu-id="3508e-110">MSGFLAG_READ</span><span class="sxs-lookup"><span data-stu-id="3508e-110">MSGFLAG_READ</span></span>  <br/> |<span data-ttu-id="3508e-111">fmsRead</span><span class="sxs-lookup"><span data-stu-id="3508e-111">fmsRead</span></span>  <br/> |
|<span data-ttu-id="3508e-112">MSGFLAG_UNMODIFED</span><span class="sxs-lookup"><span data-stu-id="3508e-112">MSGFLAG_UNMODIFED</span></span>  <br/> |<span data-ttu-id="3508e-113">~ fmsModified</span><span class="sxs-lookup"><span data-stu-id="3508e-113">~fmsModified</span></span>  <br/> |
|<span data-ttu-id="3508e-114">MSGFLAG_SUBMIT</span><span class="sxs-lookup"><span data-stu-id="3508e-114">MSGFLAG_SUBMIT</span></span>  <br/> |<span data-ttu-id="3508e-115">fmsSubmitted</span><span class="sxs-lookup"><span data-stu-id="3508e-115">fmsSubmitted</span></span>  <br/> |
|<span data-ttu-id="3508e-116">MSGFLAG_HASATTACH</span><span class="sxs-lookup"><span data-stu-id="3508e-116">MSGFLAG_HASATTACH</span></span>  <br/> |<span data-ttu-id="3508e-117">fmsHasAttach</span><span class="sxs-lookup"><span data-stu-id="3508e-117">fmsHasAttach</span></span>  <br/> |
|<span data-ttu-id="3508e-118">MSGFLAG_UNSENT</span><span class="sxs-lookup"><span data-stu-id="3508e-118">MSGFLAG_UNSENT</span></span>  <br/> |<span data-ttu-id="3508e-119">fmsLocal</span><span class="sxs-lookup"><span data-stu-id="3508e-119">fmsLocal</span></span>  <br/> |
   
<span data-ttu-id="3508e-120">Esses sinalizadores são definidos no TNEF. Arquivo de cabeçalho H.</span><span class="sxs-lookup"><span data-stu-id="3508e-120">These flags are defined in the TNEF.H header file.</span></span>
  

