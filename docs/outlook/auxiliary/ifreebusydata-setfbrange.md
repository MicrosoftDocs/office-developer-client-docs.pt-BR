---
title: IFreeBusyDataSetFBRange
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4e7147ea-0eb0-324a-80d8-4f0eef654c32
description: Define o intervalo de tempo para uma enumeração de blocos de informações de disponibilidade de dados para um usuário.
ms.openlocfilehash: 84a25a2dd43f594caa075d90e4f183086452184a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765847"
---
# <a name="ifreebusydatasetfbrange"></a><span data-ttu-id="a3732-103">IFreeBusyData::SetFBRange</span><span class="sxs-lookup"><span data-stu-id="a3732-103">IFreeBusyData::SetFBRange</span></span>

<span data-ttu-id="a3732-104">Define o intervalo de tempo para uma enumeração de blocos de informações de disponibilidade de dados para um usuário.</span><span class="sxs-lookup"><span data-stu-id="a3732-104">Sets the range of time for an enumeration of free/busy blocks of data for a user.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="a3732-105">Informações rápidas</span><span class="sxs-lookup"><span data-stu-id="a3732-105">Quick info</span></span>

<span data-ttu-id="a3732-106">Consulte [IFreeBusyData](ifreebusydata.md).</span><span class="sxs-lookup"><span data-stu-id="a3732-106">See [IFreeBusyData](ifreebusydata.md).</span></span>
  
```cpp
HRESULT SetFBRange(
     LONG rtmStart,
     LONG rtmEnd
);
```

## <a name="parameters"></a><span data-ttu-id="a3732-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a3732-107">Parameters</span></span>

<span data-ttu-id="a3732-108">_rtmStart_</span><span class="sxs-lookup"><span data-stu-id="a3732-108">_rtmStart_</span></span>
  
> <span data-ttu-id="a3732-109">[in] Um valor de tempo relativo para o início das informações de livre/ocupado.</span><span class="sxs-lookup"><span data-stu-id="a3732-109">[in] A relative time value for the start of free/busy information.</span></span> <span data-ttu-id="a3732-110">Esse valor é o número de minutos desde 1 de janeiro de 1601.</span><span class="sxs-lookup"><span data-stu-id="a3732-110">This value is the number of minutes since January 1, 1601.</span></span>
    
<span data-ttu-id="a3732-111">_rtmEnd_</span><span class="sxs-lookup"><span data-stu-id="a3732-111">_rtmEnd_</span></span>
  
> <span data-ttu-id="a3732-112">[in] Um valor de tempo relativo para o fim das informações de livre/ocupado.</span><span class="sxs-lookup"><span data-stu-id="a3732-112">[in] A relative time value for the end of free/busy information.</span></span> <span data-ttu-id="a3732-113">Esse valor é o número de minutos desde 1 de janeiro de 1601.</span><span class="sxs-lookup"><span data-stu-id="a3732-113">This value is the number of minutes since January 1, 1601.</span></span>
    
## <a name="return-values"></a><span data-ttu-id="a3732-114">Valores de retorno</span><span class="sxs-lookup"><span data-stu-id="a3732-114">Return values</span></span>

<span data-ttu-id="a3732-115">S_OK se a chamada foi bem-sucedida; Caso contrário, um código de erro.</span><span class="sxs-lookup"><span data-stu-id="a3732-115">S_OK if the call succeeded; otherwise, an error code.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="a3732-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="a3732-116">Remarks</span></span>

<span data-ttu-id="a3732-117">Este método é usado para indicar o intervalo de tempo de itens de calendário para o qual recuperar detalhes.</span><span class="sxs-lookup"><span data-stu-id="a3732-117">This method is used to indicate the time range of calendar items for which to retrieve details.</span></span> <span data-ttu-id="a3732-118">Os valores de *ftmStart* e *ftmEnd* são armazenados em cache e retornados em uma chamada subsequente de [IFreeBusyData::GetFBPublishRange](ifreebusydata-getfbpublishrange.md).</span><span class="sxs-lookup"><span data-stu-id="a3732-118">The values of  *ftmStart*  and  *ftmEnd*  are cached and returned in a subsequent call of [IFreeBusyData::GetFBPublishRange](ifreebusydata-getfbpublishrange.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="a3732-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="a3732-119">See also</span></span>

- [<span data-ttu-id="a3732-120">IFreeBusyData::EnumBlocks</span><span class="sxs-lookup"><span data-stu-id="a3732-120">IFreeBusyData::EnumBlocks</span></span>](ifreebusydata-enumblocks.md)
- [<span data-ttu-id="a3732-121">IFreeBusyData::GetFBPublishRange</span><span class="sxs-lookup"><span data-stu-id="a3732-121">IFreeBusyData::GetFBPublishRange</span></span>](ifreebusydata-getfbpublishrange.md)
- [<span data-ttu-id="a3732-122">Usar o tempo relativo para acessar dados de disponibilidade</span><span class="sxs-lookup"><span data-stu-id="a3732-122">Use relative time to access free/busy data</span></span>](how-to-use-relative-time-to-access-free-busy-data.md)

