---
title: IFreeBusyDataSetFBRange
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4e7147ea-0eb0-324a-80d8-4f0eef654c32
description: Define o intervalo de tempo para uma enumeração de blocos de disponibilidade de dados de um usuário.
ms.openlocfilehash: 4647453acb0e530521aa808f7f017e3e311644bb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421659"
---
# <a name="ifreebusydatasetfbrange"></a><span data-ttu-id="db6c1-103">IFreeBusyData::SetFBRange</span><span class="sxs-lookup"><span data-stu-id="db6c1-103">IFreeBusyData::SetFBRange</span></span>

<span data-ttu-id="db6c1-104">Define o intervalo de tempo para uma enumeração de blocos de disponibilidade de dados de um usuário.</span><span class="sxs-lookup"><span data-stu-id="db6c1-104">Sets the range of time for an enumeration of free/busy blocks of data for a user.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="db6c1-105">Informações rápidas</span><span class="sxs-lookup"><span data-stu-id="db6c1-105">Quick info</span></span>

<span data-ttu-id="db6c1-106">Confira [IFreeBusyData](ifreebusydata.md).</span><span class="sxs-lookup"><span data-stu-id="db6c1-106">See [IFreeBusyData](ifreebusydata.md).</span></span>
  
```cpp
HRESULT SetFBRange(
     LONG rtmStart,
     LONG rtmEnd
);
```

## <a name="parameters"></a><span data-ttu-id="db6c1-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="db6c1-107">Parameters</span></span>

<span data-ttu-id="db6c1-108">_rtmStart_</span><span class="sxs-lookup"><span data-stu-id="db6c1-108">_rtmStart_</span></span>
  
> <span data-ttu-id="db6c1-109">[in] Um valor de tempo relativo para o início das informações de livre/ocupado.</span><span class="sxs-lookup"><span data-stu-id="db6c1-109">[in] A relative time value for the start of free/busy information.</span></span> <span data-ttu-id="db6c1-110">Esse valor é o número de minutos desde 1º de janeiro de 1601.</span><span class="sxs-lookup"><span data-stu-id="db6c1-110">This value is the number of minutes since January 1, 1601.</span></span>
    
<span data-ttu-id="db6c1-111">_rtmEnd_</span><span class="sxs-lookup"><span data-stu-id="db6c1-111">_rtmEnd_</span></span>
  
> <span data-ttu-id="db6c1-112">[in] Um valor de tempo relativo para o final das informações de livre/ocupado.</span><span class="sxs-lookup"><span data-stu-id="db6c1-112">[in] A relative time value for the end of free/busy information.</span></span> <span data-ttu-id="db6c1-113">Esse valor é o número de minutos desde 1º de janeiro de 1601.</span><span class="sxs-lookup"><span data-stu-id="db6c1-113">This value is the number of minutes since January 1, 1601.</span></span>
    
## <a name="return-values"></a><span data-ttu-id="db6c1-114">Valores de retorno</span><span class="sxs-lookup"><span data-stu-id="db6c1-114">Return values</span></span>

<span data-ttu-id="db6c1-115">S_OK se a chamada for bem-sucedida; caso contrário, um código de erro.</span><span class="sxs-lookup"><span data-stu-id="db6c1-115">S_OK if the call succeeded; otherwise, an error code.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="db6c1-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="db6c1-116">Remarks</span></span>

<span data-ttu-id="db6c1-117">Esse método é usado para indicar o intervalo de tempo de itens de calendário para os quais recuperar detalhes.</span><span class="sxs-lookup"><span data-stu-id="db6c1-117">This method is used to indicate the time range of calendar items for which to retrieve details.</span></span> <span data-ttu-id="db6c1-118">Os valores de  *ftmStart*  e  *ftmEnd*  são armazenados em cache e retornados em uma chamada subsequente de [IFreeBusyData::GetFBPublishRange](ifreebusydata-getfbpublishrange.md).</span><span class="sxs-lookup"><span data-stu-id="db6c1-118">The values of  *ftmStart*  and  *ftmEnd*  are cached and returned in a subsequent call of [IFreeBusyData::GetFBPublishRange](ifreebusydata-getfbpublishrange.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="db6c1-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="db6c1-119">See also</span></span>

- [<span data-ttu-id="db6c1-120">IFreeBusyData::EnumBlocks</span><span class="sxs-lookup"><span data-stu-id="db6c1-120">IFreeBusyData::EnumBlocks</span></span>](ifreebusydata-enumblocks.md)
- [<span data-ttu-id="db6c1-121">IFreeBusyData::GetFBPublishRange</span><span class="sxs-lookup"><span data-stu-id="db6c1-121">IFreeBusyData::GetFBPublishRange</span></span>](ifreebusydata-getfbpublishrange.md)
- [<span data-ttu-id="db6c1-122">Usar o tempo relativo para acessar dados de disponibilidade</span><span class="sxs-lookup"><span data-stu-id="db6c1-122">Use relative time to access free/busy data</span></span>](how-to-use-relative-time-to-access-free-busy-data.md)

