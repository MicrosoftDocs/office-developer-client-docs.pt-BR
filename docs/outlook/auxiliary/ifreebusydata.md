---
title: IFreeBusyData
manager: soliver
ms.date: 12/08/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c9a80ad3-6311-fe07-b6f7-9fd63424753b
ms.openlocfilehash: cd9d4dffd83e1995319b0f0d661435fedb78f28c
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25393205"
---
# <a name="ifreebusydata"></a><span data-ttu-id="c1d21-102">IFreeBusyData</span><span class="sxs-lookup"><span data-stu-id="c1d21-102">IFreeBusyData</span></span>

<span data-ttu-id="c1d21-103">Para um usuário específico, obtém e define um intervalo de tempo e retorna uma interface para enumerar blocos de disponibilidade de dados nesse intervalo de tempo.</span><span class="sxs-lookup"><span data-stu-id="c1d21-103">For a given user, gets and sets a time range and returns an interface for enumerating free/busy blocks of data within this time range.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="c1d21-104">Informações rápidas</span><span class="sxs-lookup"><span data-stu-id="c1d21-104">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c1d21-105">Herda de:</span><span class="sxs-lookup"><span data-stu-id="c1d21-105">Inherits from appleDeviceFeaturesConfigurationBase</span></span>  <br/> |[<span data-ttu-id="c1d21-106">IUnknown</span><span class="sxs-lookup"><span data-stu-id="c1d21-106">IUnknown</span></span>](https://msdn.microsoft.com/library/33f1d79a-33fc-4ce5-a372-e08bda378332%28Office.15%29.aspx) <br/> |
|<span data-ttu-id="c1d21-107">Fornecido por:</span><span class="sxs-lookup"><span data-stu-id="c1d21-107">Provided by:</span></span>  <br/> |<span data-ttu-id="c1d21-108">Provedor de disponibilidade</span><span class="sxs-lookup"><span data-stu-id="c1d21-108">Free/busy provider</span></span>  <br/> |
|<span data-ttu-id="c1d21-109">Identificador de interface:</span><span class="sxs-lookup"><span data-stu-id="c1d21-109">Interface identifier:</span></span>  <br/> |<span data-ttu-id="c1d21-110">IID_IFreeBusyData</span><span class="sxs-lookup"><span data-stu-id="c1d21-110">IID_IFreeBusyData</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="c1d21-111">Vtable order</span><span class="sxs-lookup"><span data-stu-id="c1d21-111">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="c1d21-112">Placeholder1</span><span class="sxs-lookup"><span data-stu-id="c1d21-112">IFreeBusySupport::Placeholder1</span></span>](ifreebusydata-placeholder1.md) <br/> | <span data-ttu-id="c1d21-113">*Esse membro é um espaço reservado e não tem suporte.*</span><span class="sxs-lookup"><span data-stu-id="c1d21-113">*This member is a placeholder and is not supported.*</span></span>  <br/> |
|[<span data-ttu-id="c1d21-114">EnumBlocks</span><span class="sxs-lookup"><span data-stu-id="c1d21-114">IFreeBusyData::EnumBlocks</span></span>](ifreebusydata-enumblocks.md) <br/> |<span data-ttu-id="c1d21-115">É uma interface que enumera blocos de disponibilidade de dados de um usuário em um intervalo de tempo específico.</span><span class="sxs-lookup"><span data-stu-id="c1d21-115">Gets an interface that enumerates free/busy blocks of data for a user within a specified time range.</span></span>  <br/> |
|[<span data-ttu-id="c1d21-116">Placeholder2</span><span class="sxs-lookup"><span data-stu-id="c1d21-116">IFreeBusySupport::Placeholder2</span></span>](ifreebusydata-placeholder2.md) <br/> | <span data-ttu-id="c1d21-117">*Esse membro é um espaço reservado e não tem suporte.*</span><span class="sxs-lookup"><span data-stu-id="c1d21-117">*This member is a placeholder and is not supported.*</span></span>  <br/> |
|[<span data-ttu-id="c1d21-118">Placeholder3</span><span class="sxs-lookup"><span data-stu-id="c1d21-118">IFreeBusySupport::Placeholder3</span></span>](ifreebusydata-placeholder3.md) <br/> | <span data-ttu-id="c1d21-119">*Esse membro é um espaço reservado e não tem suporte.*</span><span class="sxs-lookup"><span data-stu-id="c1d21-119">*This member is a placeholder and is not supported.*</span></span>  <br/> |
|[<span data-ttu-id="c1d21-120">Placeholder4</span><span class="sxs-lookup"><span data-stu-id="c1d21-120">IFreeBusySupport::Placeholder4</span></span>](ifreebusydata-placeholder4.md) <br/> | <span data-ttu-id="c1d21-121">*Esse membro é um espaço reservado e não tem suporte.*</span><span class="sxs-lookup"><span data-stu-id="c1d21-121">*This member is a placeholder and is not supported.*</span></span>  <br/> |
|[<span data-ttu-id="c1d21-122">Placeholder5</span><span class="sxs-lookup"><span data-stu-id="c1d21-122">IFreeBusySupport::Placeholder5</span></span>](ifreebusydata-placeholder5.md) <br/> | <span data-ttu-id="c1d21-123">*Esse membro é um espaço reservado e não tem suporte.*</span><span class="sxs-lookup"><span data-stu-id="c1d21-123">*This member is a placeholder and is not supported.*</span></span>  <br/> |
|[<span data-ttu-id="c1d21-124">SetFBRange</span><span class="sxs-lookup"><span data-stu-id="c1d21-124">IFreeBusyData::SetFBRange</span></span>](ifreebusydata-setfbrange.md) <br/> |<span data-ttu-id="c1d21-125">Define o intervalo de tempo para uma enumeração de blocos de disponibilidade de dados de um usuário.</span><span class="sxs-lookup"><span data-stu-id="c1d21-125">Sets the range of time for an enumeration of free/busy blocks of data for a user.</span></span>  <br/> |
|[<span data-ttu-id="c1d21-126">Placeholder6</span><span class="sxs-lookup"><span data-stu-id="c1d21-126">IFreeBusySupport::Placeholder6</span></span>](ifreebusydata-placeholder6.md) <br/> | <span data-ttu-id="c1d21-127">*Esse membro é um espaço reservado e não tem suporte.*</span><span class="sxs-lookup"><span data-stu-id="c1d21-127">*This member is a placeholder and is not supported.*</span></span>  <br/> |
|[<span data-ttu-id="c1d21-128">GetFBPublishRange</span><span class="sxs-lookup"><span data-stu-id="c1d21-128">IFreeBusyData::GetFBPublishRange</span></span>](ifreebusydata-getfbpublishrange.md) <br/> |<span data-ttu-id="c1d21-129">Obtém um intervalo de tempo pré-definido para uma enumeração de blocos de disponibilidade de dados de um usuário.</span><span class="sxs-lookup"><span data-stu-id="c1d21-129">Gets a preset time range for an enumeration of free/busy blocks of data for a user.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c1d21-130">Comentários</span><span class="sxs-lookup"><span data-stu-id="c1d21-130">Remarks</span></span>

<span data-ttu-id="c1d21-131">A maioria dos membros dessa interface consiste em espaços reservados para uso interno do Outlook e está sujeita a alterações.</span><span class="sxs-lookup"><span data-stu-id="c1d21-131">Most of the members in this interface are placeholders reserved for the internal use of Outlook and are subject to change.</span></span> <span data-ttu-id="c1d21-132">Os provedores de disponibilidade devem implementá-los apenas conforme especificado, retornando somente os valores de retorno especificados.</span><span class="sxs-lookup"><span data-stu-id="c1d21-132">Free/busy providers must implement them only as specified, returning only the specified return values.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="c1d21-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="c1d21-133">See also</span></span>

- [<span data-ttu-id="c1d21-134">Sobre a API do serviço de disponibilidade</span><span class="sxs-lookup"><span data-stu-id="c1d21-134">About the Free/Busy API</span></span>](about-the-free-busy-api.md)
- [<span data-ttu-id="c1d21-135">Constantes (API do serviço de disponibilidade)</span><span class="sxs-lookup"><span data-stu-id="c1d21-135">Constants (Free/busy API)</span></span>](constants-free-busy-api.md)

