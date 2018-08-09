---
title: IFreeBusyDataGetFBPublishRange
manager: soliver
ms.date: 09/23/2016
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 1a8bbe0c-17d1-9349-4c63-f257faf4edda
description: Obtém um intervalo de tempo predefinido para uma enumeração de blocos de informações de disponibilidade de dados para um usuário.
ms.openlocfilehash: 2a322a43da38a0b902789f4c83baaabd769154c7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765829"
---
# <a name="ifreebusydatagetfbpublishrange"></a><span data-ttu-id="d73ea-103">IFreeBusyData::GetFBPublishRange</span><span class="sxs-lookup"><span data-stu-id="d73ea-103">IFreeBusyData::GetFBPublishRange</span></span>

<span data-ttu-id="d73ea-104">Obtém um intervalo de tempo predefinido para uma enumeração de blocos de informações de disponibilidade de dados para um usuário.</span><span class="sxs-lookup"><span data-stu-id="d73ea-104">Gets a preset time range for an enumeration of free/busy blocks of data for a user.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="d73ea-105">Informações rápidas</span><span class="sxs-lookup"><span data-stu-id="d73ea-105">Quick info</span></span>

<span data-ttu-id="d73ea-106">Consulte [IFreeBusyData](ifreebusydata.md).</span><span class="sxs-lookup"><span data-stu-id="d73ea-106">See [IFreeBusyData](ifreebusydata.md).</span></span>
  
```cpp
HRESULT GetFBPublishRange( 
     LONG *prtmStart,  
     LONG *prtmEnd 
);

```

## <a name="parameters"></a><span data-ttu-id="d73ea-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d73ea-107">Parameters</span></span>

<span data-ttu-id="d73ea-108">_prtmStart_</span><span class="sxs-lookup"><span data-stu-id="d73ea-108">_prtmStart_</span></span>
  
> <span data-ttu-id="d73ea-109">[out] Um valor de tempo relativo para o início das informações de livre/ocupado.</span><span class="sxs-lookup"><span data-stu-id="d73ea-109">[out] A relative time value for the start of free/busy information.</span></span> <span data-ttu-id="d73ea-110">Esse valor é o número de minutos desde 1 de janeiro de 1601.</span><span class="sxs-lookup"><span data-stu-id="d73ea-110">This value is the number of minutes since January 1, 1601.</span></span>
    
<span data-ttu-id="d73ea-111">_prtmEnd_</span><span class="sxs-lookup"><span data-stu-id="d73ea-111">_prtmEnd_</span></span>
  
> <span data-ttu-id="d73ea-112">[out] Um valor de tempo relativo para o fim das informações de livre/ocupado.</span><span class="sxs-lookup"><span data-stu-id="d73ea-112">[out] A relative time value for the end of free/busy information.</span></span> <span data-ttu-id="d73ea-113">Esse valor é o número de minutos desde 1 de janeiro de 1601.</span><span class="sxs-lookup"><span data-stu-id="d73ea-113">This value is the number of minutes since January 1, 1601.</span></span>
    
## <a name="return-values"></a><span data-ttu-id="d73ea-114">Valores de retorno</span><span class="sxs-lookup"><span data-stu-id="d73ea-114">Return values</span></span>

<span data-ttu-id="d73ea-115">S_OK se a chamada foi bem-sucedida; Caso contrário, um código de erro.</span><span class="sxs-lookup"><span data-stu-id="d73ea-115">S_OK if the call succeeded; otherwise, an error code.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="d73ea-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="d73ea-116">Remarks</span></span>

<span data-ttu-id="d73ea-117">Um provedor de livre/ocupado chama [IFreeBusyData::EnumBlocks](ifreebusydata-enumblocks.md) ou [IFreeBusyData::SetFBRange](ifreebusydata-setfbrange.md) para definir o intervalo de tempo para uma enumeração.</span><span class="sxs-lookup"><span data-stu-id="d73ea-117">A free/busy provider calls [IFreeBusyData::EnumBlocks](ifreebusydata-enumblocks.md) or [IFreeBusyData::SetFBRange](ifreebusydata-setfbrange.md) to set the time range for an enumeration.</span></span> <span data-ttu-id="d73ea-118">Se não tiver sido chamado [IFreeBusyData::EnumBlocks](ifreebusydata-enumblocks.md) ou [IFreeBusyData::SetFBRange](ifreebusydata-setfbrange.md) , os valores padrão para **prtmStart** e **prtmEnd** devem ser definidos entre 1º de abril de 1601 00:00:00Z e 31 de agosto de 4500 11:59:59Z respectivamente.</span><span class="sxs-lookup"><span data-stu-id="d73ea-118">If either [IFreeBusyData::EnumBlocks](ifreebusydata-enumblocks.md) or [IFreeBusyData::SetFBRange](ifreebusydata-setfbrange.md) has not been called, the default values for **prtmStart** and **prtmEnd** must be set between April 1st, 1601 00:00:00Z and August 31, 4500 11:59:59Z respectively.</span></span> <span data-ttu-id="d73ea-119">Além disso, você não deve definir a hora de início para ser maior do que a hora de término.</span><span class="sxs-lookup"><span data-stu-id="d73ea-119">Additionally, you should not set the start time to be greater than the end time.</span></span> 
  
<span data-ttu-id="d73ea-120">**IFreeBusyData::GetFBPublishRange** deve retornar que os valores armazenados em cache para o intervalo de tempo definido pela chamada mais recente para **IFreeBusyData::EnumBlocks** ou **IFreeBusyData::SetFBRange**.</span><span class="sxs-lookup"><span data-stu-id="d73ea-120">**IFreeBusyData::GetFBPublishRange** must return the cached values for the time range set by the most recent call for **IFreeBusyData::EnumBlocks** or **IFreeBusyData::SetFBRange**.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="d73ea-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="d73ea-121">See also</span></span>

- [<span data-ttu-id="d73ea-122">Usar o tempo relativo para acessar dados de disponibilidade</span><span class="sxs-lookup"><span data-stu-id="d73ea-122">Use relative time to access free/busy data</span></span>](how-to-use-relative-time-to-access-free-busy-data.md)
- [<span data-ttu-id="d73ea-123">IFreeBusyData::EnumBlocks</span><span class="sxs-lookup"><span data-stu-id="d73ea-123">IFreeBusyData::EnumBlocks</span></span>](ifreebusydata-enumblocks.md)
- [<span data-ttu-id="d73ea-124">IFreeBusyData::SetFBRange</span><span class="sxs-lookup"><span data-stu-id="d73ea-124">IFreeBusyData::SetFBRange</span></span>](ifreebusydata-setfbrange.md)

