---
title: IFreeBusyDataEnumBlocks
manager: soliver
ms.date: 02/18/2016
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 0cd5a5ae-118f-c7da-4eda-e97590fc39d4
description: É uma interface que enumera blocos de disponibilidade de dados de um usuário em um intervalo de tempo específico.
ms.openlocfilehash: 51a77b2f47166628db07259ef841e0d6173ee370
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317553"
---
# <a name="ifreebusydataenumblocks"></a><span data-ttu-id="3b4cf-103">IFreeBusyData::EnumBlocks</span><span class="sxs-lookup"><span data-stu-id="3b4cf-103">IFreeBusyData::EnumBlocks</span></span>

<span data-ttu-id="3b4cf-104">É uma interface que enumera blocos de disponibilidade de dados de um usuário em um intervalo de tempo específico.</span><span class="sxs-lookup"><span data-stu-id="3b4cf-104">Gets an interface that enumerates free/busy blocks of data for a user within a specified time range.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="3b4cf-105">Informações rápidas</span><span class="sxs-lookup"><span data-stu-id="3b4cf-105">Quick info</span></span>

<span data-ttu-id="3b4cf-106">Confira [IFreeBusyData](ifreebusydata.md).</span><span class="sxs-lookup"><span data-stu-id="3b4cf-106">See [IFreeBusyData](ifreebusydata.md).</span></span>
  
```cpp
HRESULT EnumBlocks( 
     IEnumFBBlock **ppenumfb,  
     FILETIME ftmStart, 
     FILETIME ftmEnd 
);

```

## <a name="parameters"></a><span data-ttu-id="3b4cf-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3b4cf-107">Parameters</span></span>

<span data-ttu-id="3b4cf-108">_ppenumfb_</span><span class="sxs-lookup"><span data-stu-id="3b4cf-108">_ppenumfb_</span></span>
  
> <span data-ttu-id="3b4cf-109">[out] Uma interface para enumerar blocos de disponibilidade.</span><span class="sxs-lookup"><span data-stu-id="3b4cf-109">[out] An interface to enumerate free/busy blocks.</span></span>
    
<span data-ttu-id="3b4cf-110">_ftmStart_</span><span class="sxs-lookup"><span data-stu-id="3b4cf-110">_ftmStart_</span></span>
  
> <span data-ttu-id="3b4cf-111">[in] A hora de início da enumeração.</span><span class="sxs-lookup"><span data-stu-id="3b4cf-111">[in] The start time for the enumeration.</span></span> <span data-ttu-id="3b4cf-112">É expressa em [FILETIME](https://msdn.microsoft.com/library/ 4af8e79a-697e-44a1-8576-fdc57726e9ef.aspx).</span><span class="sxs-lookup"><span data-stu-id="3b4cf-112">It is expressed in [FILETIME](https://msdn.microsoft.com/library/ 4af8e79a-697e-44a1-8576-fdc57726e9ef.aspx).</span></span>
    
<span data-ttu-id="3b4cf-113">_ftmEnd_</span><span class="sxs-lookup"><span data-stu-id="3b4cf-113">_ftmEnd_</span></span>
  
> <span data-ttu-id="3b4cf-114">[in] A hora de término da enumeração.</span><span class="sxs-lookup"><span data-stu-id="3b4cf-114">[in] The end time for the enumeration.</span></span> <span data-ttu-id="3b4cf-115">É expressa em **FILETIME**.</span><span class="sxs-lookup"><span data-stu-id="3b4cf-115">It is expressed in **FILETIME**.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="3b4cf-116">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="3b4cf-116">Return values</span></span>

<span data-ttu-id="3b4cf-117">S_OK se a chamada for bem-sucedida; caso contrário, um código de erro.</span><span class="sxs-lookup"><span data-stu-id="3b4cf-117">S_OK if the call succeeded; otherwise, an error code.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="3b4cf-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="3b4cf-118">Remarks</span></span>

<span data-ttu-id="3b4cf-119">Esse método é usado para indicar o intervalo de tempo de itens de calendário para os quais recuperar detalhes.</span><span class="sxs-lookup"><span data-stu-id="3b4cf-119">This method is used to indicate the time range of calendar items for which to retrieve details.</span></span> <span data-ttu-id="3b4cf-120">Os valores de *ftmStart* e *ftmEnd* são armazenados em cache e retornados em uma chamada subsequente de [IFreeBusyData::GetFBPublishRange](ifreebusydata-getfbpublishrange.md).</span><span class="sxs-lookup"><span data-stu-id="3b4cf-120">The values of  *ftmStart* and *ftmEnd* are cached and returned in a subsequent call of [IFreeBusyData::GetFBPublishRange](ifreebusydata-getfbpublishrange.md).</span></span>
  
<span data-ttu-id="3b4cf-121">Um provedor de disponibilidade posteriormente também pode usar a interface [IEnumFBBlock](ienumfbblock.md) retornada para acessar a enumeração.</span><span class="sxs-lookup"><span data-stu-id="3b4cf-121">A free/busy provider can also subsequently use the returned [IEnumFBBlock](ienumfbblock.md) interface to access the enumeration.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="3b4cf-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="3b4cf-122">See also</span></span>

- [<span data-ttu-id="3b4cf-123">IEnumFBBlock</span><span class="sxs-lookup"><span data-stu-id="3b4cf-123">IEnumFBBlock</span></span>](ienumfbblock.md)
- [<span data-ttu-id="3b4cf-124">IFreeBusyData::GetFBPublishRange</span><span class="sxs-lookup"><span data-stu-id="3b4cf-124">IFreeBusyData::GetFBPublishRange</span></span>](ifreebusydata-getfbpublishrange.md)
- [<span data-ttu-id="3b4cf-125">IFreeBusyData::SetFBRange</span><span class="sxs-lookup"><span data-stu-id="3b4cf-125">IFreeBusyData::SetFBRange</span></span>](ifreebusydata-setfbrange.md)
- [<span data-ttu-id="3b4cf-126">Usar o tempo relativo para acessar dados de disponibilidade</span><span class="sxs-lookup"><span data-stu-id="3b4cf-126">Use relative time to access free/busy data</span></span>](how-to-use-relative-time-to-access-free-busy-data.md)

