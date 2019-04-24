---
title: Sintaxe de fluxo TNEF
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 1353d494-c266-4715-afe7-14543a1bbe1b
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 12d2a92ff80897456707c7ab8af8f704605c85d0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339631"
---
# <a name="tnef-stream-syntax"></a><span data-ttu-id="3d464-103">Sintaxe de fluxo TNEF</span><span class="sxs-lookup"><span data-stu-id="3d464-103">TNEF Stream Syntax</span></span>

  
  
<span data-ttu-id="3d464-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3d464-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3d464-105">Este tópico apresenta um Bakus-Nauer como a descrição da sintaxe de fluxo TNEF.</span><span class="sxs-lookup"><span data-stu-id="3d464-105">This topic presents a Bakus-Nauer like description of the TNEF stream syntax.</span></span> <span data-ttu-id="3d464-106">Nesta descrição, os elementos não terminais que têm uma definição adicional estão em itálico.</span><span class="sxs-lookup"><span data-stu-id="3d464-106">In this description, nonterminal elements that have a further definition are in italics.</span></span> <span data-ttu-id="3d464-107">Constantes e itens literais estão em negrito.</span><span class="sxs-lookup"><span data-stu-id="3d464-107">Constants and literal items are in bold.</span></span> <span data-ttu-id="3d464-108">As sequências de elementos são listadas em ordem em uma única linha.</span><span class="sxs-lookup"><span data-stu-id="3d464-108">Sequences of elements are listed in order on a single line.</span></span> <span data-ttu-id="3d464-109">Por exemplo, o item _Stream_ consiste na constante **TNEF_SIGNATURE**, seguida por uma _chave_, seguida por um _objeto_.</span><span class="sxs-lookup"><span data-stu-id="3d464-109">For example, the  _Stream_ item consists of the constant **TNEF_SIGNATURE**, followed by a  _Key_, followed by an  _Object_.</span></span> <span data-ttu-id="3d464-110">Quando um item tem mais de uma implementação possível, as alternativas são listadas em linhas consecutivas.</span><span class="sxs-lookup"><span data-stu-id="3d464-110">When an item has more than one possible implementation, the alternatives are listed on consecutive lines.</span></span> <span data-ttu-id="3d464-111">Por exemplo, um _objeto_ pode consistir em um _Message_Seq_, um _Message_Seq_ seguido por um _Attach_Seq_ou apenas um _Attach_Seq_.</span><span class="sxs-lookup"><span data-stu-id="3d464-111">For example, an  _Object_ can consist of a  _Message_Seq_, a  _Message_Seq_ followed by an  _Attach_Seq_, or just an  _Attach_Seq_.</span></span>
  
 <span data-ttu-id="3d464-112">_TNEF_Stream:_</span><span class="sxs-lookup"><span data-stu-id="3d464-112">_TNEF_Stream:_</span></span>
  
> <span data-ttu-id="3d464-113">**TNEF_SIGNATURE** _Chave_ _Objeto_</span><span class="sxs-lookup"><span data-stu-id="3d464-113">**TNEF_SIGNATURE** _Key_ _Object_</span></span>
    
 <span data-ttu-id="3d464-114">_Chaves_</span><span class="sxs-lookup"><span data-stu-id="3d464-114">_Key:_</span></span>
  
> <span data-ttu-id="3d464-115">um inteiro não assinado de 16 bits diferente de zero</span><span class="sxs-lookup"><span data-stu-id="3d464-115">a nonzero 16-bit unsigned integer</span></span>
    
<span data-ttu-id="3d464-116">Os transportes habilitados para TNEF geram esse valor antes de usar a implementação TNEF para gerar um fluxo TNEF.</span><span class="sxs-lookup"><span data-stu-id="3d464-116">TNEF enabled transports generate this value before using the TNEF implementation to generate a TNEF stream.</span></span>
  
 <span data-ttu-id="3d464-117">_Objeções_</span><span class="sxs-lookup"><span data-stu-id="3d464-117">_Object:_</span></span>
  
>  <span data-ttu-id="3d464-118">_Message_Seq Message_Seq Attach_Seq Attach_Seq_</span><span class="sxs-lookup"><span data-stu-id="3d464-118">_Message_Seq Message_Seq Attach_Seq Attach_Seq_</span></span>
    
 <span data-ttu-id="3d464-119">_Message_Seq:_</span><span class="sxs-lookup"><span data-stu-id="3d464-119">_Message_Seq:_</span></span>
  
>  <span data-ttu-id="3d464-120">_attTnefVersion attTnefVersion Msg_Attribute_Seq attTnefVersion attMessageClass attTnefVersion attMessageClass Msg_Attribute_Seq attMessageClass attMessageClass Msg_Attribute_Seq Msg_Attribute_Seq_</span><span class="sxs-lookup"><span data-stu-id="3d464-120">_attTnefVersion attTnefVersion Msg_Attribute_Seq attTnefVersion attMessageClass attTnefVersion attMessageClass Msg_Attribute_Seq attMessageClass attMessageClass Msg_Attribute_Seq Msg_Attribute_Seq_</span></span>
    
 <span data-ttu-id="3d464-121">_attTnefVersion:_</span><span class="sxs-lookup"><span data-stu-id="3d464-121">_attTnefVersion:_</span></span>
  
> <span data-ttu-id="3d464-122">**LVL_MESSAGE attTnefVersion sizeof (ULong)** soma de verificação **0x00010000**</span><span class="sxs-lookup"><span data-stu-id="3d464-122">**LVL_MESSAGE attTnefVersion sizeof(ULONG)** **0x00010000** checksum</span></span> 
    
 <span data-ttu-id="3d464-123">_attMessageClass:_</span><span class="sxs-lookup"><span data-stu-id="3d464-123">_attMessageClass:_</span></span>
  
> <span data-ttu-id="3d464-124">**LVL_MESSAGE attMessageClass** _msg_class_length msg_class_ de soma de verificação</span><span class="sxs-lookup"><span data-stu-id="3d464-124">**LVL_MESSAGE attMessageClass** _msg_class_length msg_class_ checksum</span></span> 
    
 <span data-ttu-id="3d464-125">_Msg_Attribute_Seq:_</span><span class="sxs-lookup"><span data-stu-id="3d464-125">_Msg_Attribute_Seq:_</span></span>
  
>  <span data-ttu-id="3d464-126">_Msg_Attribute Msg_Attribute Msg_Attribute_Seq_</span><span class="sxs-lookup"><span data-stu-id="3d464-126">_Msg_Attribute Msg_Attribute Msg_Attribute_Seq_</span></span>
    
 <span data-ttu-id="3d464-127">_Msg_Attribute:_</span><span class="sxs-lookup"><span data-stu-id="3d464-127">_Msg_Attribute:_</span></span>
  
> <span data-ttu-id="3d464-128">Atributo **LVL_MESSAGE** -atributo de ID-soma de verificação de dados</span><span class="sxs-lookup"><span data-stu-id="3d464-128">**LVL_MESSAGE** attribute-ID attribute-length attribute-data checksum</span></span> 
    
<span data-ttu-id="3d464-129">Attribute-ID é um dos identificadores de atributo TNEF, como **attSubject**.</span><span class="sxs-lookup"><span data-stu-id="3d464-129">Attribute-ID is one of the TNEF attribute identifiers, such as **attSubject**.</span></span> <span data-ttu-id="3d464-130">Attribute-length é o tamanho em bytes dos dados de atributo.</span><span class="sxs-lookup"><span data-stu-id="3d464-130">Attribute-length is the length in bytes of the attribute data.</span></span> <span data-ttu-id="3d464-131">O atributo-data é os dados associados ao atributo.</span><span class="sxs-lookup"><span data-stu-id="3d464-131">Attribute-data is the data associated with the attribute.</span></span>
  
 <span data-ttu-id="3d464-132">_Attach_Seq:_</span><span class="sxs-lookup"><span data-stu-id="3d464-132">_Attach_Seq:_</span></span>
  
>  <span data-ttu-id="3d464-133">_attRenddata attRenddata Att_Attribute_Seq_</span><span class="sxs-lookup"><span data-stu-id="3d464-133">_attRenddata attRenddata Att_Attribute_Seq_</span></span>
    
 <span data-ttu-id="3d464-134">_attRenddata:_</span><span class="sxs-lookup"><span data-stu-id="3d464-134">_attRenddata:_</span></span>
  
> <span data-ttu-id="3d464-135">**LVL_ATTACHMENT attRenddata** RENDDATA **de soma de verificação de sizeof (RENDDATA)**</span><span class="sxs-lookup"><span data-stu-id="3d464-135">**LVL_ATTACHMENT attRenddata** **sizeof(RENDDATA)** renddata checksum</span></span> 
    
<span data-ttu-id="3d464-136">Renddata é os dados associados à estrutura **Renddata** que contém as informações de renderização para o anexo correspondente.</span><span class="sxs-lookup"><span data-stu-id="3d464-136">Renddata is the data associated with the **RENDDATA** structure that contains the rendering information for the corresponding attachment.</span></span> <span data-ttu-id="3d464-137">A estrutura **RENDDATA** é definida no TNEF. Arquivo de cabeçalho H.</span><span class="sxs-lookup"><span data-stu-id="3d464-137">The **RENDDATA** structure is defined in the TNEF.H header file.</span></span> 
  
 <span data-ttu-id="3d464-138">_Att_Attribute_Seq:_</span><span class="sxs-lookup"><span data-stu-id="3d464-138">_Att_Attribute_Seq:_</span></span>
  
>  <span data-ttu-id="3d464-139">_Att_Attribute Att_Attribute Att_Attribute_Seq_</span><span class="sxs-lookup"><span data-stu-id="3d464-139">_Att_Attribute Att_Attribute Att_Attribute_Seq_</span></span>
    
 <span data-ttu-id="3d464-140">_Att_Attribute:_</span><span class="sxs-lookup"><span data-stu-id="3d464-140">_Att_Attribute:_</span></span>
  
> <span data-ttu-id="3d464-141">Atributo **LVL_ATTACHMENT** -atributo de ID-soma de verificação de dados</span><span class="sxs-lookup"><span data-stu-id="3d464-141">**LVL_ATTACHMENT** attribute-ID attribute-length attribute-data checksum</span></span> 
    
<span data-ttu-id="3d464-142">O atributo-ID, o tamanho do atributo e o atributo-dados têm as mesmas médias para o item Msg_Attribute.</span><span class="sxs-lookup"><span data-stu-id="3d464-142">Attribute-ID, attribute-length, and attribute-data have the same meanings as for the Msg_Attribute item.</span></span>
  

