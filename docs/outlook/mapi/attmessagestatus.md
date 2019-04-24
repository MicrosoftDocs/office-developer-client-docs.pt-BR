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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32318203"
---
# <a name="attmessagestatus"></a><span data-ttu-id="a59a1-103">attMessageStatus</span><span class="sxs-lookup"><span data-stu-id="a59a1-103">attMessageStatus</span></span>

  
  
<span data-ttu-id="a59a1-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a59a1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a59a1-105">Os sinalizadores de mensagem MAPI são mapeados para sinalizadores TNEF para preservar a compatibilidade com versões anteriores.</span><span class="sxs-lookup"><span data-stu-id="a59a1-105">MAPI message flags are mapped to TNEF flags to preserve backward compatibility.</span></span> <span data-ttu-id="a59a1-106">Todos os sinalizadores são agrupados e codificados em um único byte.</span><span class="sxs-lookup"><span data-stu-id="a59a1-106">All the flags are grouped together and encoded in a single byte.</span></span> <span data-ttu-id="a59a1-107">Os mapeamentos são os seguintes:</span><span class="sxs-lookup"><span data-stu-id="a59a1-107">The mappings are as follows:</span></span>
  
|<span data-ttu-id="a59a1-108">**Sinalizadores de mensagens MAPI**</span><span class="sxs-lookup"><span data-stu-id="a59a1-108">**MAPI message flags**</span></span>|<span data-ttu-id="a59a1-109">**Sinalizadores TNEF**</span><span class="sxs-lookup"><span data-stu-id="a59a1-109">**TNEF flags**</span></span>|
|:-----|:-----|
|<span data-ttu-id="a59a1-110">MSGFLAG_READ</span><span class="sxs-lookup"><span data-stu-id="a59a1-110">MSGFLAG_READ</span></span>  <br/> |<span data-ttu-id="a59a1-111">fmsRead</span><span class="sxs-lookup"><span data-stu-id="a59a1-111">fmsRead</span></span>  <br/> |
|<span data-ttu-id="a59a1-112">MSGFLAG_UNMODIFED</span><span class="sxs-lookup"><span data-stu-id="a59a1-112">MSGFLAG_UNMODIFED</span></span>  <br/> |<span data-ttu-id="a59a1-113">~ fmsModified</span><span class="sxs-lookup"><span data-stu-id="a59a1-113">~fmsModified</span></span>  <br/> |
|<span data-ttu-id="a59a1-114">MSGFLAG_SUBMIT</span><span class="sxs-lookup"><span data-stu-id="a59a1-114">MSGFLAG_SUBMIT</span></span>  <br/> |<span data-ttu-id="a59a1-115">fmsSubmitted</span><span class="sxs-lookup"><span data-stu-id="a59a1-115">fmsSubmitted</span></span>  <br/> |
|<span data-ttu-id="a59a1-116">MSGFLAG_HASATTACH</span><span class="sxs-lookup"><span data-stu-id="a59a1-116">MSGFLAG_HASATTACH</span></span>  <br/> |<span data-ttu-id="a59a1-117">fmsHasAttach</span><span class="sxs-lookup"><span data-stu-id="a59a1-117">fmsHasAttach</span></span>  <br/> |
|<span data-ttu-id="a59a1-118">MSGFLAG_UNSENT</span><span class="sxs-lookup"><span data-stu-id="a59a1-118">MSGFLAG_UNSENT</span></span>  <br/> |<span data-ttu-id="a59a1-119">fmsLocal</span><span class="sxs-lookup"><span data-stu-id="a59a1-119">fmsLocal</span></span>  <br/> |
   
<span data-ttu-id="a59a1-120">Esses sinalizadores são definidos no TNEF. Arquivo de cabeçalho H.</span><span class="sxs-lookup"><span data-stu-id="a59a1-120">These flags are defined in the TNEF.H header file.</span></span>
  

