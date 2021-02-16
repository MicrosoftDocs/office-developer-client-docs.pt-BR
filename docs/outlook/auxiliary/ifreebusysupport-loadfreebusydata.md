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
# <a name="ifreebusysupportloadfreebusydata"></a><span data-ttu-id="2c0f2-103">IFreeBusySupport::LoadFreeBusyData</span><span class="sxs-lookup"><span data-stu-id="2c0f2-103">IFreeBusySupport::LoadFreeBusyData</span></span>

<span data-ttu-id="2c0f2-104">Retorna, para cada usuário específico, uma interface para enumerar blocos de disponibilidade de dados em um intervalo de tempo.</span><span class="sxs-lookup"><span data-stu-id="2c0f2-104">Returns, for each specified user, an interface for enumerating free/busy blocks of data within a time range.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="2c0f2-105">Informações rápidas</span><span class="sxs-lookup"><span data-stu-id="2c0f2-105">Quick info</span></span>

<span data-ttu-id="2c0f2-106">Consulte [IFreeBusySupport](ifreebusysupport.md).</span><span class="sxs-lookup"><span data-stu-id="2c0f2-106">See [IFreeBusySupport](ifreebusysupport.md).</span></span>
  
```cpp
HRESULT LoadFreeBusyData( 
    ULONG cMax,  
    FBUser *rgfbuser, 
    IFreeBusyData **prgfbdata,  
    HRESULT *phrStatus, 
    ULONG *pcRead 
);
```

## <a name="parameters"></a><span data-ttu-id="2c0f2-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2c0f2-107">Parameters</span></span>

<span data-ttu-id="2c0f2-108">_cMax_</span><span class="sxs-lookup"><span data-stu-id="2c0f2-108">_cMax_</span></span>
  
> <span data-ttu-id="2c0f2-109">[in] O número de interfaces [IFreeBusyData](ifreebusydata.md) a retornar.</span><span class="sxs-lookup"><span data-stu-id="2c0f2-109">[in] The number of [IFreeBusyData](ifreebusydata.md) interfaces to return.</span></span> 
    
<span data-ttu-id="2c0f2-110">_rgfbuser_</span><span class="sxs-lookup"><span data-stu-id="2c0f2-110">_rgfbuser_</span></span>
  
> <span data-ttu-id="2c0f2-111">[in] A matriz de usuários de livre/ocupado para recuperar dados.</span><span class="sxs-lookup"><span data-stu-id="2c0f2-111">[in] The array of free/busy users to retrieve data for.</span></span>
    
<span data-ttu-id="2c0f2-112">_prgfbdata_</span><span class="sxs-lookup"><span data-stu-id="2c0f2-112">_prgfbdata_</span></span>
  
> <span data-ttu-id="2c0f2-113">[in] [out] A matriz de interfaces **IFreeBusyData** que correspondem à matriz _rgfbuser_ de [estruturas FBUser.](fbuser.md)</span><span class="sxs-lookup"><span data-stu-id="2c0f2-113">[in][out] The array of **IFreeBusyData** interfaces that correspond to the  _rgfbuser_ array of [FBUser](fbuser.md) structures.</span></span> 
    
   > [!NOTE]
   > <span data-ttu-id="2c0f2-114">Essa matriz de ponteiros é alocada pelo chamador e liberada pelo chamador.</span><span class="sxs-lookup"><span data-stu-id="2c0f2-114">This array of pointers is allocated by the caller and freed by the caller.</span></span> <span data-ttu-id="2c0f2-115">As interfaces reais apontadas são liberadas quando o chamador é feito com eles.</span><span class="sxs-lookup"><span data-stu-id="2c0f2-115">The actual interfaces pointed to are released when the caller is done with them.</span></span> 
  
<span data-ttu-id="2c0f2-116">_phrStatus_</span><span class="sxs-lookup"><span data-stu-id="2c0f2-116">_phrStatus_</span></span>
  
> <span data-ttu-id="2c0f2-117">[out] A matriz de **resultados HRESULT** para recuperar cada interface **IFreeBusyData** correspondente.</span><span class="sxs-lookup"><span data-stu-id="2c0f2-117">[out] The array of **HRESULT** results for retrieving each corresponding **IFreeBusyData** interface.</span></span> <span data-ttu-id="2c0f2-118">O valor pode ser NULL.</span><span class="sxs-lookup"><span data-stu-id="2c0f2-118">The value may be NULL.</span></span> <span data-ttu-id="2c0f2-119">Um resultado será definido como S_OK se  _prgfbdata correspondente_ for válido.</span><span class="sxs-lookup"><span data-stu-id="2c0f2-119">A result is set to S_OK if corresponding  _prgfbdata_ is valid.</span></span> 
    
<span data-ttu-id="2c0f2-120">_pcRead_</span><span class="sxs-lookup"><span data-stu-id="2c0f2-120">_pcRead_</span></span>
  
>  <span data-ttu-id="2c0f2-121">[out] O número real de usuários para os quais uma interface **IFreeBusyData** foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="2c0f2-121">[out] The actual number of users for which an **IFreeBusyData** interface has been found.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="2c0f2-122">Valores de retorno</span><span class="sxs-lookup"><span data-stu-id="2c0f2-122">Return values</span></span>

<span data-ttu-id="2c0f2-123">S_OK se a chamada foi bem-sucedida. Caso contrário, um código de erro.</span><span class="sxs-lookup"><span data-stu-id="2c0f2-123">S_OK if the call succeeded; otherwise, an error code.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="2c0f2-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="2c0f2-124">See also</span></span>

- [<span data-ttu-id="2c0f2-125">Constantes (API do serviço de disponibilidade)</span><span class="sxs-lookup"><span data-stu-id="2c0f2-125">Constants (Free/busy API)</span></span>](constants-free-busy-api.md)

