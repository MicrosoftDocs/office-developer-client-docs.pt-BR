---
title: IFreeBusySupportLoadFreeBusyData
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f0baa310-7a53-07ee-0a7d-33dd1fb465c2
description: Retorna, para cada usuário específico, uma interface para enumerar blocos de disponibilidade de dados em um intervalo de tempo.
ms.openlocfilehash: e55f902117a20bfefaa5d9a2f3a067cb78ec86cb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411229"
---
# <a name="ifreebusysupportloadfreebusydata"></a><span data-ttu-id="67410-103">IFreeBusySupport::LoadFreeBusyData</span><span class="sxs-lookup"><span data-stu-id="67410-103">IFreeBusySupport::LoadFreeBusyData</span></span>

<span data-ttu-id="67410-104">Retorna, para cada usuário específico, uma interface para enumerar blocos de disponibilidade de dados em um intervalo de tempo.</span><span class="sxs-lookup"><span data-stu-id="67410-104">Returns, for each specified user, an interface for enumerating free/busy blocks of data within a time range.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="67410-105">Informações rápidas</span><span class="sxs-lookup"><span data-stu-id="67410-105">Quick info</span></span>

<span data-ttu-id="67410-106">Consulte [IFreeBusySupport](ifreebusysupport.md).</span><span class="sxs-lookup"><span data-stu-id="67410-106">See [IFreeBusySupport](ifreebusysupport.md).</span></span>
  
```cpp
HRESULT LoadFreeBusyData( 
    ULONG cMax,  
    FBUser *rgfbuser, 
    IFreeBusyData **prgfbdata,  
    HRESULT *phrStatus, 
    ULONG *pcRead 
);
```

## <a name="parameters"></a><span data-ttu-id="67410-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="67410-107">Parameters</span></span>

<span data-ttu-id="67410-108">_cMax_</span><span class="sxs-lookup"><span data-stu-id="67410-108">_cMax_</span></span>
  
> <span data-ttu-id="67410-109">no O número de interfaces [IFreeBusyData](ifreebusydata.md) a serem retornadas.</span><span class="sxs-lookup"><span data-stu-id="67410-109">[in] The number of [IFreeBusyData](ifreebusydata.md) interfaces to return.</span></span> 
    
<span data-ttu-id="67410-110">_rgfbuser_</span><span class="sxs-lookup"><span data-stu-id="67410-110">_rgfbuser_</span></span>
  
> <span data-ttu-id="67410-111">no A matriz de usuários de disponibilidade para os quais recuperar dados.</span><span class="sxs-lookup"><span data-stu-id="67410-111">[in] The array of free/busy users to retrieve data for.</span></span>
    
<span data-ttu-id="67410-112">_prgfbdata_</span><span class="sxs-lookup"><span data-stu-id="67410-112">_prgfbdata_</span></span>
  
> <span data-ttu-id="67410-113">no bota A matriz de interfaces **IFreeBusyData** que correspondem à matriz _Rgfbuser_ de estruturas [FBUser](fbuser.md) .</span><span class="sxs-lookup"><span data-stu-id="67410-113">[in][out] The array of **IFreeBusyData** interfaces that correspond to the  _rgfbuser_ array of [FBUser](fbuser.md) structures.</span></span> 
    
   > [!NOTE]
   > <span data-ttu-id="67410-114">Essa matriz de ponteiros é alocada pelo chamador e liberada pelo chamador.</span><span class="sxs-lookup"><span data-stu-id="67410-114">This array of pointers is allocated by the caller and freed by the caller.</span></span> <span data-ttu-id="67410-115">As interfaces reais apontadas são lançadas quando o chamador é feito com elas.</span><span class="sxs-lookup"><span data-stu-id="67410-115">The actual interfaces pointed to are released when the caller is done with them.</span></span> 
  
<span data-ttu-id="67410-116">_phrStatus_</span><span class="sxs-lookup"><span data-stu-id="67410-116">_phrStatus_</span></span>
  
> <span data-ttu-id="67410-117">bota A matriz de resultados **HRESULT** para recuperar cada interface **IFreeBusyData** correspondente.</span><span class="sxs-lookup"><span data-stu-id="67410-117">[out] The array of **HRESULT** results for retrieving each corresponding **IFreeBusyData** interface.</span></span> <span data-ttu-id="67410-118">O valor pode ser nulo.</span><span class="sxs-lookup"><span data-stu-id="67410-118">The value may be NULL.</span></span> <span data-ttu-id="67410-119">Um resultado é definido como S_OK se _prgfbdata_ correspondente for válido.</span><span class="sxs-lookup"><span data-stu-id="67410-119">A result is set to S_OK if corresponding  _prgfbdata_ is valid.</span></span> 
    
<span data-ttu-id="67410-120">_pcRead_</span><span class="sxs-lookup"><span data-stu-id="67410-120">_pcRead_</span></span>
  
>  <span data-ttu-id="67410-121">bota O número real de usuários para os quais uma interface **IFreeBusyData** foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="67410-121">[out] The actual number of users for which an **IFreeBusyData** interface has been found.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="67410-122">Valores de retorno</span><span class="sxs-lookup"><span data-stu-id="67410-122">Return values</span></span>

<span data-ttu-id="67410-123">S_OK se a chamada foi bem-sucedida. Caso contrário, um código de erro.</span><span class="sxs-lookup"><span data-stu-id="67410-123">S_OK if the call succeeded; otherwise, an error code.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="67410-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="67410-124">See also</span></span>

- [<span data-ttu-id="67410-125">Constantes (API do serviço de disponibilidade)</span><span class="sxs-lookup"><span data-stu-id="67410-125">Constants (Free/busy API)</span></span>](constants-free-busy-api.md)

