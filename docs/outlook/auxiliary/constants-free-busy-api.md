---
title: Constantes (API do serviço de disponibilidade)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: ff756bf1-9395-5e50-4f55-1eb0365a84ed
description: Este tópico contém definições constantes, identificadores de classe e identificadores de interface para a API de disponibilidade.
ms.openlocfilehash: 13578617eaab45e7194d7a0d4d6995ef925e7f20
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431530"
---
# <a name="constants-freebusy-api"></a><span data-ttu-id="07461-103">Constantes (API do serviço de disponibilidade)</span><span class="sxs-lookup"><span data-stu-id="07461-103">Constants (Free/busy API)</span></span>

<span data-ttu-id="07461-104">Este tópico contém definições constantes, identificadores de classe e identificadores de interface para a API de disponibilidade.</span><span class="sxs-lookup"><span data-stu-id="07461-104">This topic contains constant definitions, class identifiers, and interface identifiers for the Free/Busy API.</span></span>
  
## <a name="constants"></a><span data-ttu-id="07461-105">Constantes</span><span class="sxs-lookup"><span data-stu-id="07461-105">Constants</span></span>

|<span data-ttu-id="07461-106">**Constante**</span><span class="sxs-lookup"><span data-stu-id="07461-106">**Constant**</span></span>|<span data-ttu-id="07461-107">**Definição**</span><span class="sxs-lookup"><span data-stu-id="07461-107">**Definition**</span></span>|
|:-----|:-----|
|<span data-ttu-id="07461-108">E_NOTIMPL</span><span class="sxs-lookup"><span data-stu-id="07461-108">E_NOTIMPL</span></span>  <br/> | <span data-ttu-id="07461-109">*Conforme definido no arquivo de cabeçalho do Microsoft Windows Software Development Kit (SDK). h.*</span><span class="sxs-lookup"><span data-stu-id="07461-109">*As defined in the Microsoft Windows Software Development Kit (SDK) header file winerror.h.*</span></span>  <br/> |
|<span data-ttu-id="07461-110">E_OUTOFMEMORY</span><span class="sxs-lookup"><span data-stu-id="07461-110">E_OUTOFMEMORY</span></span>  <br/> | <span data-ttu-id="07461-111">*Conforme definido no arquivo de cabeçalho do Windows SDK Winerror. h.*</span><span class="sxs-lookup"><span data-stu-id="07461-111">*As defined in the Windows SDK header file winerror.h.*</span></span>  <br/> |
|<span data-ttu-id="07461-112">S_FALSE</span><span class="sxs-lookup"><span data-stu-id="07461-112">S_FALSE</span></span>  <br/> | <span data-ttu-id="07461-113">*Conforme definido no arquivo de cabeçalho do Windows SDK Winerror. h.*</span><span class="sxs-lookup"><span data-stu-id="07461-113">*As defined in the Windows SDK header file winerror.h.*</span></span>  <br/> |
|<span data-ttu-id="07461-114">S_OK</span><span class="sxs-lookup"><span data-stu-id="07461-114">S_OK</span></span>  <br/> | <span data-ttu-id="07461-115">*Conforme definido no arquivo de cabeçalho do Windows SDK Winerror. h.*</span><span class="sxs-lookup"><span data-stu-id="07461-115">*As defined in the Windows SDK header file winerror.h.*</span></span>  <br/> |
   
## <a name="interface-identifiers"></a><span data-ttu-id="07461-116">Identificadores de interface</span><span class="sxs-lookup"><span data-stu-id="07461-116">Interface identifiers</span></span>

<span data-ttu-id="07461-117">Para os seguintes identificadores de interface, suponha que a macro DEFINE_GUID definida no arquivo de cabeçalho do Windows SDK guiddef. h para associar o nome simbólico GUID a seu valor.</span><span class="sxs-lookup"><span data-stu-id="07461-117">For the following interface identifiers, assume the DEFINE_GUID macro defined in the Windows SDK header file guiddef.h to associate the GUID symbolic name with its value.</span></span>
  
<span data-ttu-id="07461-118">{00067064-0000-0000-C000-000000000046}</span><span class="sxs-lookup"><span data-stu-id="07461-118">//{00067064-0000-0000-C000-000000000046}</span></span>
  
<span data-ttu-id="07461-119">DEFINE_GUID (IID_IEnumFBBlock, 0x00067064, 0x0, 0x0, 0xC0, 0x0, 0x0, 0x0, 0x0, 0x0, 0x0, 0x46);</span><span class="sxs-lookup"><span data-stu-id="07461-119">DEFINE_GUID(IID_IEnumFBBlock, 0x00067064, 0x0, 0x0, 0xc0, 0x0, 0x0, 0x0, 0x0, 0x0, 0x0, 0x46);</span></span>
  
<span data-ttu-id="07461-120">{00067066-0000-0000-C000-000000000046}</span><span class="sxs-lookup"><span data-stu-id="07461-120">//{00067066-0000-0000-C000-000000000046}</span></span>
  
<span data-ttu-id="07461-121">DEFINE_GUID (IID_IFreeBusyData, 0x00067066, 0x0, 0x0, 0xC0, 0x0, 0x0, 0x0, 0x0, 0x0, 0x0, 0x46);</span><span class="sxs-lookup"><span data-stu-id="07461-121">DEFINE_GUID(IID_IFreeBusyData, 0x00067066, 0x0, 0x0, 0xc0, 0x0, 0x0, 0x0, 0x0, 0x0, 0x0, 0x46);</span></span>
  
<span data-ttu-id="07461-122">{00067067-0000-0000-C000-000000000046}</span><span class="sxs-lookup"><span data-stu-id="07461-122">//{00067067-0000-0000-C000-000000000046}</span></span>
  
<span data-ttu-id="07461-123">DEFINE_GUID (IID_IFreeBusySupport, 0x00067067, 0x0, 0x0, 0xC0, 0x0, 0x0, 0x0, 0x0, 0x0, 0x0, 0x46);</span><span class="sxs-lookup"><span data-stu-id="07461-123">DEFINE_GUID(IID_IFreeBusySupport, 0x00067067, 0x0, 0x0, 0xc0, 0x0, 0x0, 0x0, 0x0, 0x0, 0x0, 0x46);</span></span>
  

