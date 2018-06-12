---
title: IFreeBusySupportLoadFreeBusyData
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f0baa310-7a53-07ee-0a7d-33dd1fb465c2
description: Retorna, para cada usuário especificado, uma interface para enumerar os blocos de informações de disponibilidade de dados dentro de um intervalo de tempo.
ms.openlocfilehash: 9af5a40da9f0a831de7346b44cee9ca004c02300
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765832"
---
# <a name="ifreebusysupportloadfreebusydata"></a><span data-ttu-id="31453-103">IFreeBusySupport::LoadFreeBusyData</span><span class="sxs-lookup"><span data-stu-id="31453-103">IFreeBusySupport::LoadFreeBusyData</span></span>

<span data-ttu-id="31453-104">Retorna, para cada usuário especificado, uma interface para enumerar os blocos de informações de disponibilidade de dados dentro de um intervalo de tempo.</span><span class="sxs-lookup"><span data-stu-id="31453-104">Returns, for each specified user, an interface for enumerating free/busy blocks of data within a time range.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="31453-105">Informações rápidas</span><span class="sxs-lookup"><span data-stu-id="31453-105">Quick info</span></span>

<span data-ttu-id="31453-106">Consulte [IFreeBusySupport](ifreebusysupport.md).</span><span class="sxs-lookup"><span data-stu-id="31453-106">See [IFreeBusySupport](ifreebusysupport.md).</span></span>
  
```cpp
HRESULT LoadFreeBusyData( 
    ULONG cMax,  
    FBUser *rgfbuser, 
    IFreeBusyData **prgfbdata,  
    HRESULT *phrStatus, 
    ULONG *pcRead 
);
```

## <a name="parameters"></a><span data-ttu-id="31453-107">Par�metros</span><span class="sxs-lookup"><span data-stu-id="31453-107">Parameters</span></span>

<span data-ttu-id="31453-108">_cMax_</span><span class="sxs-lookup"><span data-stu-id="31453-108">_cMax_</span></span>
  
> <span data-ttu-id="31453-109">[in] O número de interfaces de [IFreeBusyData](ifreebusydata.md) para retornar.</span><span class="sxs-lookup"><span data-stu-id="31453-109">[in] The number of [IFreeBusyData](ifreebusydata.md) interfaces to return.</span></span> 
    
<span data-ttu-id="31453-110">_rgfbuser_</span><span class="sxs-lookup"><span data-stu-id="31453-110">_rgfbuser_</span></span>
  
> <span data-ttu-id="31453-111">[in] A matriz de usuários de livre/ocupado para recuperar dados para.</span><span class="sxs-lookup"><span data-stu-id="31453-111">[in] The array of free/busy users to retrieve data for.</span></span>
    
<span data-ttu-id="31453-112">_prgfbdata_</span><span class="sxs-lookup"><span data-stu-id="31453-112">_prgfbdata_</span></span>
  
> <span data-ttu-id="31453-113">[in] [out] A matriz de interfaces de **IFreeBusyData** que correspondem à matriz _rgfbuser_ de estruturas de [FBUser](fbuser.md) .</span><span class="sxs-lookup"><span data-stu-id="31453-113">[in][out] The array of **IFreeBusyData** interfaces that correspond to the  _rgfbuser_ array of [FBUser](fbuser.md) structures.</span></span> 
    
   > [!NOTE]
   > <span data-ttu-id="31453-114">Essa matriz de ponteiros é alocada pelo chamador e liberada pelo chamador.</span><span class="sxs-lookup"><span data-stu-id="31453-114">This array of pointers is allocated by the caller and freed by the caller.</span></span> <span data-ttu-id="31453-115">As interfaces reais apontadas para sejam liberadas quando o chamador é feito com eles.</span><span class="sxs-lookup"><span data-stu-id="31453-115">The actual interfaces pointed to are released when the caller is done with them.</span></span> 
  
<span data-ttu-id="31453-116">_phrStatus_</span><span class="sxs-lookup"><span data-stu-id="31453-116">_phrStatus_</span></span>
  
> <span data-ttu-id="31453-117">[out] A matriz de resultados **HRESULT** para recuperação de cada interface **IFreeBusyData** correspondente.</span><span class="sxs-lookup"><span data-stu-id="31453-117">[out] The array of **HRESULT** results for retrieving each corresponding **IFreeBusyData** interface.</span></span> <span data-ttu-id="31453-118">O valor pode ser NULL.</span><span class="sxs-lookup"><span data-stu-id="31453-118">The value may be NULL.</span></span> <span data-ttu-id="31453-119">Um resultado é definido como S_OK se correspondente _prgfbdata_ é válida.</span><span class="sxs-lookup"><span data-stu-id="31453-119">A result is set to S_OK if corresponding  _prgfbdata_ is valid.</span></span> 
    
<span data-ttu-id="31453-120">_pcRead_</span><span class="sxs-lookup"><span data-stu-id="31453-120">_pcRead_</span></span>
  
>  <span data-ttu-id="31453-121">[out] O número real de usuários para o qual uma interface **IFreeBusyData** foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="31453-121">[out] The actual number of users for which an **IFreeBusyData** interface has been found.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="31453-122">Valores de retorno</span><span class="sxs-lookup"><span data-stu-id="31453-122">Return values</span></span>

<span data-ttu-id="31453-123">S_OK se a chamada foi bem-sucedida; Caso contrário, um código de erro.</span><span class="sxs-lookup"><span data-stu-id="31453-123">S_OK if the call succeeded; otherwise, an error code.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="31453-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="31453-124">See also</span></span>

- [<span data-ttu-id="31453-125">Constantes (API de livre/ocupado)</span><span class="sxs-lookup"><span data-stu-id="31453-125">Constants (Free/busy API)</span></span>](constants-free-busy-api.md)

