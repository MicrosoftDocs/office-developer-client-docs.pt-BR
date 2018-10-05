---
title: Propriedade canônica PidLidTaskActualEffort
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTaskActualEffort
api_type:
- COM
ms.assetid: 8e9a9432-bf50-4333-82ec-fba19dff8006
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 7eb51396f4575a8f8f9ce15aff84eb894773e979
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25382579"
---
# <a name="pidlidtaskactualeffort-canonical-property"></a><span data-ttu-id="640ab-103">Propriedade canônica PidLidTaskActualEffort</span><span class="sxs-lookup"><span data-stu-id="640ab-103">PidLidTaskActualEffort Canonical Property</span></span>

  
  
<span data-ttu-id="640ab-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="640ab-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="640ab-105">Indica o número de minutos que o usuário realizou uma tarefa.</span><span class="sxs-lookup"><span data-stu-id="640ab-105">Indicates the number of minutes that the user performed a task.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="640ab-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="640ab-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="640ab-107">dispidTaskActualEffort</span><span class="sxs-lookup"><span data-stu-id="640ab-107">dispidTaskActualEffort</span></span>  <br/> |
|<span data-ttu-id="640ab-108">Propriedade definida:</span><span class="sxs-lookup"><span data-stu-id="640ab-108">Property set:</span></span>  <br/> |<span data-ttu-id="640ab-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="640ab-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="640ab-110">ID de longo (LID):</span><span class="sxs-lookup"><span data-stu-id="640ab-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="640ab-111">0x00008110</span><span class="sxs-lookup"><span data-stu-id="640ab-111">0x00008110</span></span>  <br/> |
|<span data-ttu-id="640ab-112">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="640ab-112">Data type:</span></span>  <br/> |<span data-ttu-id="640ab-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="640ab-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="640ab-114">Área:</span><span class="sxs-lookup"><span data-stu-id="640ab-114">Area:</span></span>  <br/> |<span data-ttu-id="640ab-115">Task</span><span class="sxs-lookup"><span data-stu-id="640ab-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="640ab-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="640ab-116">Remarks</span></span>

<span data-ttu-id="640ab-117">O valor deve ser maior ou igual a 0 e menor que 0x5AE980DF (1,525,252,319), onde o 480 minutos igual a um dia e 2400 minutos igual uma semana (oito horas em um dia de trabalho e cinco dias em uma semana de trabalho).</span><span class="sxs-lookup"><span data-stu-id="640ab-117">The value must be greater than or equal to 0 and less than 0x5AE980DF (1,525,252,319), where 480 minutes equal one day and 2400 minutes equal one week (eight hours in a work day and five days in a work week).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="640ab-118">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="640ab-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="640ab-119">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="640ab-119">Protocol specifications</span></span>

<span data-ttu-id="640ab-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="640ab-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="640ab-121">Fornece referências relacionados especificações de protocolo do Exchange Server e as definições de conjunto de propriedades.</span><span class="sxs-lookup"><span data-stu-id="640ab-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="640ab-122">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="640ab-122">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="640ab-123">Especifica as propriedades e operações que são permitidas para contato e objetos de lista de distribuição pessoal.</span><span class="sxs-lookup"><span data-stu-id="640ab-123">Specifies the properties and operations that are permissible for contact and personal distribution list objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="640ab-124">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="640ab-124">Header files</span></span>

<span data-ttu-id="640ab-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="640ab-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="640ab-126">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="640ab-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="640ab-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="640ab-127">See also</span></span>



[<span data-ttu-id="640ab-128">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="640ab-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="640ab-129">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="640ab-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="640ab-130">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="640ab-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="640ab-131">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="640ab-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

