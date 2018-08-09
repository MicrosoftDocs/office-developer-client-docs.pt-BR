---
title: IFreeBusyDataEnumBlocks
manager: soliver
ms.date: 02/18/2016
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 0cd5a5ae-118f-c7da-4eda-e97590fc39d4
description: Obtém uma interface que enumera blocos de informações de disponibilidade de dados de um usuário em um intervalo de tempo especificado.
ms.openlocfilehash: ab377b1029296b6b4bac68d7169dcf7b8dcd8b87
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765834"
---
# <a name="ifreebusydataenumblocks"></a><span data-ttu-id="5dde0-103">IFreeBusyData::EnumBlocks</span><span class="sxs-lookup"><span data-stu-id="5dde0-103">IFreeBusyData::EnumBlocks</span></span>

<span data-ttu-id="5dde0-104">Obtém uma interface que enumera blocos de informações de disponibilidade de dados de um usuário em um intervalo de tempo especificado.</span><span class="sxs-lookup"><span data-stu-id="5dde0-104">Gets an interface that enumerates free/busy blocks of data for a user within a specified time range.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="5dde0-105">Informações rápidas</span><span class="sxs-lookup"><span data-stu-id="5dde0-105">Quick info</span></span>

<span data-ttu-id="5dde0-106">Consulte [IFreeBusyData](ifreebusydata.md).</span><span class="sxs-lookup"><span data-stu-id="5dde0-106">See [IFreeBusyData](ifreebusydata.md).</span></span>
  
```cpp
HRESULT EnumBlocks( 
     IEnumFBBlock **ppenumfb,  
     FILETIME ftmStart, 
     FILETIME ftmEnd 
);

```

## <a name="parameters"></a><span data-ttu-id="5dde0-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5dde0-107">Parameters</span></span>

<span data-ttu-id="5dde0-108">_ppenumfb_</span><span class="sxs-lookup"><span data-stu-id="5dde0-108">_ppenumfb_</span></span>
  
> <span data-ttu-id="5dde0-109">[out] Uma interface para enumerar os blocos de livre/ocupado.</span><span class="sxs-lookup"><span data-stu-id="5dde0-109">[out] An interface to enumerate free/busy blocks.</span></span>
    
<span data-ttu-id="5dde0-110">_ftmStart_</span><span class="sxs-lookup"><span data-stu-id="5dde0-110">_ftmStart_</span></span>
  
> <span data-ttu-id="5dde0-111">[in] A hora de início para a enumeração.</span><span class="sxs-lookup"><span data-stu-id="5dde0-111">[in] The start time for the enumeration.</span></span> <span data-ttu-id="5dde0-112">Ele é expresso em [FILETIME](http://msdn.microsoft.com/library/ 4af8e79a-697e-44a1-8576-fdc57726e9ef.aspx).</span><span class="sxs-lookup"><span data-stu-id="5dde0-112">It is expressed in [FILETIME](http://msdn.microsoft.com/library/ 4af8e79a-697e-44a1-8576-fdc57726e9ef.aspx).</span></span>
    
<span data-ttu-id="5dde0-113">_ftmEnd_</span><span class="sxs-lookup"><span data-stu-id="5dde0-113">_ftmEnd_</span></span>
  
> <span data-ttu-id="5dde0-114">[in] A hora de término para a enumeração.</span><span class="sxs-lookup"><span data-stu-id="5dde0-114">[in] The end time for the enumeration.</span></span> <span data-ttu-id="5dde0-115">Ele é expresso em **FILETIME**.</span><span class="sxs-lookup"><span data-stu-id="5dde0-115">It is expressed in **FILETIME**.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="5dde0-116">Valores de retorno</span><span class="sxs-lookup"><span data-stu-id="5dde0-116">Return values</span></span>

<span data-ttu-id="5dde0-117">S_OK se a chamada foi bem-sucedida; Caso contrário, um código de erro.</span><span class="sxs-lookup"><span data-stu-id="5dde0-117">S_OK if the call succeeded; otherwise, an error code.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="5dde0-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="5dde0-118">Remarks</span></span>

<span data-ttu-id="5dde0-119">Este método é usado para indicar o intervalo de tempo de itens de calendário para o qual recuperar detalhes.</span><span class="sxs-lookup"><span data-stu-id="5dde0-119">This method is used to indicate the time range of calendar items for which to retrieve details.</span></span> <span data-ttu-id="5dde0-120">Os valores de *ftmStart* e *ftmEnd* são armazenados em cache e retornados em uma chamada subsequente de [IFreeBusyData::GetFBPublishRange](ifreebusydata-getfbpublishrange.md).</span><span class="sxs-lookup"><span data-stu-id="5dde0-120">The values of  *ftmStart* and *ftmEnd* are cached and returned in a subsequent call of [IFreeBusyData::GetFBPublishRange](ifreebusydata-getfbpublishrange.md).</span></span>
  
<span data-ttu-id="5dde0-121">Um provedor de livre/ocupado também subsequentemente pode usar a interface de [IEnumFBBlock](ienumfbblock.md) retornada para acessar a enumeração.</span><span class="sxs-lookup"><span data-stu-id="5dde0-121">A free/busy provider can also subsequently use the returned [IEnumFBBlock](ienumfbblock.md) interface to access the enumeration.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="5dde0-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="5dde0-122">See also</span></span>

- [<span data-ttu-id="5dde0-123">IEnumFBBlock</span><span class="sxs-lookup"><span data-stu-id="5dde0-123">IEnumFBBlock</span></span>](ienumfbblock.md)
- [<span data-ttu-id="5dde0-124">IFreeBusyData::GetFBPublishRange</span><span class="sxs-lookup"><span data-stu-id="5dde0-124">IFreeBusyData::GetFBPublishRange</span></span>](ifreebusydata-getfbpublishrange.md)
- [<span data-ttu-id="5dde0-125">IFreeBusyData::SetFBRange</span><span class="sxs-lookup"><span data-stu-id="5dde0-125">IFreeBusyData::SetFBRange</span></span>](ifreebusydata-setfbrange.md)
- [<span data-ttu-id="5dde0-126">Usar o tempo relativo para acessar dados de disponibilidade</span><span class="sxs-lookup"><span data-stu-id="5dde0-126">Use relative time to access free/busy data</span></span>](how-to-use-relative-time-to-access-free-busy-data.md)

