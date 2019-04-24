---
title: IFreeBusyDataGetFBPublishRange
manager: soliver
ms.date: 09/23/2016
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 1a8bbe0c-17d1-9349-4c63-f257faf4edda
description: Obtém um intervalo de tempo pré-definido para uma enumeração de blocos de disponibilidade de dados de um usuário.
ms.openlocfilehash: 26951ea6a885f8d0e5e6a2fb5bcf9a63069c7f44
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317525"
---
# <a name="ifreebusydatagetfbpublishrange"></a><span data-ttu-id="72218-103">IFreeBusyData::GetFBPublishRange</span><span class="sxs-lookup"><span data-stu-id="72218-103">IFreeBusyData::GetFBPublishRange</span></span>

<span data-ttu-id="72218-104">Obtém um intervalo de tempo pré-definido para uma enumeração de blocos de disponibilidade de dados de um usuário.</span><span class="sxs-lookup"><span data-stu-id="72218-104">Gets a preset time range for an enumeration of free/busy blocks of data for a user.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="72218-105">Informações rápidas</span><span class="sxs-lookup"><span data-stu-id="72218-105">Quick info</span></span>

<span data-ttu-id="72218-106">Confira [IFreeBusyData](ifreebusydata.md).</span><span class="sxs-lookup"><span data-stu-id="72218-106">See [IFreeBusyData](ifreebusydata.md).</span></span>
  
```cpp
HRESULT GetFBPublishRange( 
     LONG *prtmStart,  
     LONG *prtmEnd 
);

```

## <a name="parameters"></a><span data-ttu-id="72218-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="72218-107">Parameters</span></span>

<span data-ttu-id="72218-108">_prtmStart_</span><span class="sxs-lookup"><span data-stu-id="72218-108">_prtmStart_</span></span>
  
> <span data-ttu-id="72218-109">bota Um valor de tempo relativo para o início das informações de disponibilidade.</span><span class="sxs-lookup"><span data-stu-id="72218-109">[out] A relative time value for the start of free/busy information.</span></span> <span data-ttu-id="72218-110">Este valor é o número de minutos desde 1º de janeiro de 1601.</span><span class="sxs-lookup"><span data-stu-id="72218-110">This value is the number of minutes since January 1, 1601.</span></span>
    
<span data-ttu-id="72218-111">_prtmEnd_</span><span class="sxs-lookup"><span data-stu-id="72218-111">_prtmEnd_</span></span>
  
> <span data-ttu-id="72218-112">bota Um valor de tempo relativo para o final das informações de disponibilidade.</span><span class="sxs-lookup"><span data-stu-id="72218-112">[out] A relative time value for the end of free/busy information.</span></span> <span data-ttu-id="72218-113">Este valor é o número de minutos desde 1º de janeiro de 1601.</span><span class="sxs-lookup"><span data-stu-id="72218-113">This value is the number of minutes since January 1, 1601.</span></span>
    
## <a name="return-values"></a><span data-ttu-id="72218-114">Valores de retorno</span><span class="sxs-lookup"><span data-stu-id="72218-114">Return values</span></span>

<span data-ttu-id="72218-115">S_OK se a chamada for bem-sucedida; caso contrário, um código de erro.</span><span class="sxs-lookup"><span data-stu-id="72218-115">S_OK if the call succeeded; otherwise, an error code.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="72218-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="72218-116">Remarks</span></span>

<span data-ttu-id="72218-117">Um provedor de disponibilidade chama [IFreeBusyData:: EnumBlocks](ifreebusydata-enumblocks.md) ou [IFreeBusyData:: SetFBRange](ifreebusydata-setfbrange.md) para definir o intervalo de tempo para uma enumeração.</span><span class="sxs-lookup"><span data-stu-id="72218-117">A free/busy provider calls [IFreeBusyData::EnumBlocks](ifreebusydata-enumblocks.md) or [IFreeBusyData::SetFBRange](ifreebusydata-setfbrange.md) to set the time range for an enumeration.</span></span> <span data-ttu-id="72218-118">Se [IFreeBusyData:: EnumBlocks](ifreebusydata-enumblocks.md) ou [IFreeBusyData:: SetFBRange](ifreebusydata-setfbrange.md) não tiver sido chamado, os valores padrão para **prtmStart** e **PrtmEnd** deverão ser definidos entre 1º de abril de 1601 00:00: e 31 de agosto de 4500 11:59-00Z respectivamente.</span><span class="sxs-lookup"><span data-stu-id="72218-118">If either [IFreeBusyData::EnumBlocks](ifreebusydata-enumblocks.md) or [IFreeBusyData::SetFBRange](ifreebusydata-setfbrange.md) has not been called, the default values for **prtmStart** and **prtmEnd** must be set between April 1st, 1601 00:00:00Z and August 31, 4500 11:59:59Z respectively.</span></span> <span data-ttu-id="72218-119">Além disso, você não deve definir a hora de início como maior do que a hora de término.</span><span class="sxs-lookup"><span data-stu-id="72218-119">Additionally, you should not set the start time to be greater than the end time.</span></span> 
  
<span data-ttu-id="72218-120">**IFreeBusyData:: GetFBPublishRange** deve retornar os valores em cache para o intervalo de tempo definido pela chamada mais recente de **IFreeBusyData:: EnumBlocks** ou **IFreeBusyData:: SetFBRange**.</span><span class="sxs-lookup"><span data-stu-id="72218-120">**IFreeBusyData::GetFBPublishRange** must return the cached values for the time range set by the most recent call for **IFreeBusyData::EnumBlocks** or **IFreeBusyData::SetFBRange**.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="72218-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="72218-121">See also</span></span>

- [<span data-ttu-id="72218-122">Usar o tempo relativo para acessar dados de disponibilidade</span><span class="sxs-lookup"><span data-stu-id="72218-122">Use relative time to access free/busy data</span></span>](how-to-use-relative-time-to-access-free-busy-data.md)
- [<span data-ttu-id="72218-123">IFreeBusyData::EnumBlocks</span><span class="sxs-lookup"><span data-stu-id="72218-123">IFreeBusyData::EnumBlocks</span></span>](ifreebusydata-enumblocks.md)
- [<span data-ttu-id="72218-124">IFreeBusyData::SetFBRange</span><span class="sxs-lookup"><span data-stu-id="72218-124">IFreeBusyData::SetFBRange</span></span>](ifreebusydata-setfbrange.md)

