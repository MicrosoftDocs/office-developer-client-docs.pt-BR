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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317714"
---
# <a name="constants-freebusy-api"></a><span data-ttu-id="e804d-103">Constantes (API do serviço de disponibilidade)</span><span class="sxs-lookup"><span data-stu-id="e804d-103">Constants (Free/busy API)</span></span>

<span data-ttu-id="e804d-104">Este tópico contém definições constantes, identificadores de classe e identificadores de interface para a API de disponibilidade.</span><span class="sxs-lookup"><span data-stu-id="e804d-104">This topic contains constant definitions, class identifiers, and interface identifiers for the Free/Busy API.</span></span>
  
## <a name="constants"></a><span data-ttu-id="e804d-105">Constantes</span><span class="sxs-lookup"><span data-stu-id="e804d-105">Constants</span></span>

|<span data-ttu-id="e804d-106">**Constante**</span><span class="sxs-lookup"><span data-stu-id="e804d-106">**Constant**</span></span>|<span data-ttu-id="e804d-107">**Definição**</span><span class="sxs-lookup"><span data-stu-id="e804d-107">**Definition**</span></span>|
|:-----|:-----|
|<span data-ttu-id="e804d-108">E_NOTIMPL</span><span class="sxs-lookup"><span data-stu-id="e804d-108">E_NOTIMPL</span></span>  <br/> | <span data-ttu-id="e804d-109">*Conforme definido no arquivo de cabeçalho do Microsoft Windows Software Development Kit (SDK). h.*</span><span class="sxs-lookup"><span data-stu-id="e804d-109">*As defined in the Microsoft Windows Software Development Kit (SDK) header file winerror.h.*</span></span>  <br/> |
|<span data-ttu-id="e804d-110">E_OUTOFMEMORY</span><span class="sxs-lookup"><span data-stu-id="e804d-110">E_OUTOFMEMORY</span></span>  <br/> | <span data-ttu-id="e804d-111">*Conforme definido no arquivo de cabeçalho do Windows SDK Winerror. h.*</span><span class="sxs-lookup"><span data-stu-id="e804d-111">*As defined in the Windows SDK header file winerror.h.*</span></span>  <br/> |
|<span data-ttu-id="e804d-112">S_FALSE</span><span class="sxs-lookup"><span data-stu-id="e804d-112">S_FALSE</span></span>  <br/> | <span data-ttu-id="e804d-113">*Conforme definido no arquivo de cabeçalho do Windows SDK Winerror. h.*</span><span class="sxs-lookup"><span data-stu-id="e804d-113">*As defined in the Windows SDK header file winerror.h.*</span></span>  <br/> |
|<span data-ttu-id="e804d-114">S_OK</span><span class="sxs-lookup"><span data-stu-id="e804d-114">S_OK</span></span>  <br/> | <span data-ttu-id="e804d-115">*Conforme definido no arquivo de cabeçalho do Windows SDK Winerror. h.*</span><span class="sxs-lookup"><span data-stu-id="e804d-115">*As defined in the Windows SDK header file winerror.h.*</span></span>  <br/> |
   
## <a name="interface-identifiers"></a><span data-ttu-id="e804d-116">Identificadores de interface</span><span class="sxs-lookup"><span data-stu-id="e804d-116">Interface identifiers</span></span>

<span data-ttu-id="e804d-117">Para os seguintes identificadores de interface, suponha que a macro DEFINE_GUID definida no arquivo de cabeçalho do Windows SDK guiddef. h para associar o nome simbólico GUID a seu valor.</span><span class="sxs-lookup"><span data-stu-id="e804d-117">For the following interface identifiers, assume the DEFINE_GUID macro defined in the Windows SDK header file guiddef.h to associate the GUID symbolic name with its value.</span></span>
  
<span data-ttu-id="e804d-118">{00067064-0000-0000-C000-000000000046}</span><span class="sxs-lookup"><span data-stu-id="e804d-118">//{00067064-0000-0000-C000-000000000046}</span></span>
  
<span data-ttu-id="e804d-119">DEFINE_GUID (IID_IEnumFBBlock, 0x00067064, 0x0, 0x0, 0xC0, 0x0, 0x0, 0x0, 0x0, 0x0, 0x0, 0x46);</span><span class="sxs-lookup"><span data-stu-id="e804d-119">DEFINE_GUID(IID_IEnumFBBlock, 0x00067064, 0x0, 0x0, 0xc0, 0x0, 0x0, 0x0, 0x0, 0x0, 0x0, 0x46);</span></span>
  
<span data-ttu-id="e804d-120">{00067066-0000-0000-C000-000000000046}</span><span class="sxs-lookup"><span data-stu-id="e804d-120">//{00067066-0000-0000-C000-000000000046}</span></span>
  
<span data-ttu-id="e804d-121">DEFINE_GUID (IID_IFreeBusyData, 0x00067066, 0x0, 0x0, 0xC0, 0x0, 0x0, 0x0, 0x0, 0x0, 0x0, 0x46);</span><span class="sxs-lookup"><span data-stu-id="e804d-121">DEFINE_GUID(IID_IFreeBusyData, 0x00067066, 0x0, 0x0, 0xc0, 0x0, 0x0, 0x0, 0x0, 0x0, 0x0, 0x46);</span></span>
  
<span data-ttu-id="e804d-122">{00067067-0000-0000-C000-000000000046}</span><span class="sxs-lookup"><span data-stu-id="e804d-122">//{00067067-0000-0000-C000-000000000046}</span></span>
  
<span data-ttu-id="e804d-123">DEFINE_GUID (IID_IFreeBusySupport, 0x00067067, 0x0, 0x0, 0xC0, 0x0, 0x0, 0x0, 0x0, 0x0, 0x0, 0x46);</span><span class="sxs-lookup"><span data-stu-id="e804d-123">DEFINE_GUID(IID_IFreeBusySupport, 0x00067067, 0x0, 0x0, 0xc0, 0x0, 0x0, 0x0, 0x0, 0x0, 0x0, 0x46);</span></span>
  

