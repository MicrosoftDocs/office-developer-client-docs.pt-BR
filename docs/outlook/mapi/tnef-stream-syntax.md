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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423024"
---
# <a name="tnef-stream-syntax"></a><span data-ttu-id="fbfe5-103">Sintaxe de fluxo TNEF</span><span class="sxs-lookup"><span data-stu-id="fbfe5-103">TNEF Stream Syntax</span></span>

  
  
<span data-ttu-id="fbfe5-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fbfe5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fbfe5-105">Este tópico apresenta uma Bakus-Nauer como a descrição da sintaxe de fluxo TNEF.</span><span class="sxs-lookup"><span data-stu-id="fbfe5-105">This topic presents a Bakus-Nauer like description of the TNEF stream syntax.</span></span> <span data-ttu-id="fbfe5-106">Nesta descrição, os elementos não modernos que têm uma definição posterior estão em itálico.</span><span class="sxs-lookup"><span data-stu-id="fbfe5-106">In this description, nonterminal elements that have a further definition are in italics.</span></span> <span data-ttu-id="fbfe5-107">Constantes e itens literais estão em negrito.</span><span class="sxs-lookup"><span data-stu-id="fbfe5-107">Constants and literal items are in bold.</span></span> <span data-ttu-id="fbfe5-108">Sequências de elementos são listadas em ordem em uma única linha.</span><span class="sxs-lookup"><span data-stu-id="fbfe5-108">Sequences of elements are listed in order on a single line.</span></span> <span data-ttu-id="fbfe5-109">For example, the  _Stream_ item consists of the constant **TNEF_SIGNATURE**, followed by a  _Key_, followed by an  _Object_.</span><span class="sxs-lookup"><span data-stu-id="fbfe5-109">For example, the  _Stream_ item consists of the constant **TNEF_SIGNATURE**, followed by a  _Key_, followed by an  _Object_.</span></span> <span data-ttu-id="fbfe5-110">Quando um item tem mais de uma implementação possível, as alternativas são listadas em linhas consecutivas.</span><span class="sxs-lookup"><span data-stu-id="fbfe5-110">When an item has more than one possible implementation, the alternatives are listed on consecutive lines.</span></span> <span data-ttu-id="fbfe5-111">Por exemplo, um  _objeto_ pode consistir em um  _Message_Seq_, um  _Message_Seq_ seguido por um  _Attach_Seq_ ou apenas um  _Attach_Seq_.</span><span class="sxs-lookup"><span data-stu-id="fbfe5-111">For example, an  _Object_ can consist of a  _Message_Seq_, a  _Message_Seq_ followed by an  _Attach_Seq_, or just an  _Attach_Seq_.</span></span>
  
 <span data-ttu-id="fbfe5-112">_TNEF_Stream:_</span><span class="sxs-lookup"><span data-stu-id="fbfe5-112">_TNEF_Stream:_</span></span>
  
> <span data-ttu-id="fbfe5-113">**TNEF_SIGNATURE** _chave do_ _objeto_</span><span class="sxs-lookup"><span data-stu-id="fbfe5-113">**TNEF_SIGNATURE** _Key_ _Object_</span></span>
    
 <span data-ttu-id="fbfe5-114">_Chave:_</span><span class="sxs-lookup"><span data-stu-id="fbfe5-114">_Key:_</span></span>
  
> <span data-ttu-id="fbfe5-115">um inteiro não assinado de 16 bits diferente de zero</span><span class="sxs-lookup"><span data-stu-id="fbfe5-115">a nonzero 16-bit unsigned integer</span></span>
    
<span data-ttu-id="fbfe5-116">Os transporte habilitados para TNEF geram esse valor antes de usar a implementação do TNEF para gerar um fluxo TNEF.</span><span class="sxs-lookup"><span data-stu-id="fbfe5-116">TNEF enabled transports generate this value before using the TNEF implementation to generate a TNEF stream.</span></span>
  
 <span data-ttu-id="fbfe5-117">_Objeto:_</span><span class="sxs-lookup"><span data-stu-id="fbfe5-117">_Object:_</span></span>
  
>  <span data-ttu-id="fbfe5-118">_Message_Seq Message_Seq Attach_Seq Attach_Seq_</span><span class="sxs-lookup"><span data-stu-id="fbfe5-118">_Message_Seq Message_Seq Attach_Seq Attach_Seq_</span></span>
    
 <span data-ttu-id="fbfe5-119">_Message_Seq:_</span><span class="sxs-lookup"><span data-stu-id="fbfe5-119">_Message_Seq:_</span></span>
  
>  <span data-ttu-id="fbfe5-120">_attTnefVersion attTnefVersion Msg_Attribute_Seq attTnefVersion attMessageClass attTnefVersion attMessageClass Msg_Attribute_Seq attMessageClass attMessageClass Msg_Attribute_Seq Msg_Attribute_Seq_</span><span class="sxs-lookup"><span data-stu-id="fbfe5-120">_attTnefVersion attTnefVersion Msg_Attribute_Seq attTnefVersion attMessageClass attTnefVersion attMessageClass Msg_Attribute_Seq attMessageClass attMessageClass Msg_Attribute_Seq Msg_Attribute_Seq_</span></span>
    
 <span data-ttu-id="fbfe5-121">_attTnefVersion:_</span><span class="sxs-lookup"><span data-stu-id="fbfe5-121">_attTnefVersion:_</span></span>
  
> <span data-ttu-id="fbfe5-122">**LVL_MESSAGE tamanho de attTnefVersion (ULONG)** 0x00010000 **verificação**</span><span class="sxs-lookup"><span data-stu-id="fbfe5-122">**LVL_MESSAGE attTnefVersion sizeof(ULONG)** **0x00010000** checksum</span></span> 
    
 <span data-ttu-id="fbfe5-123">_attMessageClass:_</span><span class="sxs-lookup"><span data-stu-id="fbfe5-123">_attMessageClass:_</span></span>
  
> <span data-ttu-id="fbfe5-124">**LVL_MESSAGE attMessageClass** _msg_class_length msg_class_ verificação</span><span class="sxs-lookup"><span data-stu-id="fbfe5-124">**LVL_MESSAGE attMessageClass** _msg_class_length msg_class_ checksum</span></span> 
    
 <span data-ttu-id="fbfe5-125">_Msg_Attribute_Seq:_</span><span class="sxs-lookup"><span data-stu-id="fbfe5-125">_Msg_Attribute_Seq:_</span></span>
  
>  <span data-ttu-id="fbfe5-126">_Msg_Attribute Msg_Attribute Msg_Attribute_Seq_</span><span class="sxs-lookup"><span data-stu-id="fbfe5-126">_Msg_Attribute Msg_Attribute Msg_Attribute_Seq_</span></span>
    
 <span data-ttu-id="fbfe5-127">_Msg_Attribute:_</span><span class="sxs-lookup"><span data-stu-id="fbfe5-127">_Msg_Attribute:_</span></span>
  
> <span data-ttu-id="fbfe5-128">**LVL_MESSAGE** verificação atributo-ID atributo-length attribute-data</span><span class="sxs-lookup"><span data-stu-id="fbfe5-128">**LVL_MESSAGE** attribute-ID attribute-length attribute-data checksum</span></span> 
    
<span data-ttu-id="fbfe5-129">Attribute-ID é um dos identificadores de atributo TNEF, como **attSubject**.</span><span class="sxs-lookup"><span data-stu-id="fbfe5-129">Attribute-ID is one of the TNEF attribute identifiers, such as **attSubject**.</span></span> <span data-ttu-id="fbfe5-130">Comprimento do atributo é o comprimento em bytes dos dados do atributo.</span><span class="sxs-lookup"><span data-stu-id="fbfe5-130">Attribute-length is the length in bytes of the attribute data.</span></span> <span data-ttu-id="fbfe5-131">Dados de atributo são os dados associados ao atributo.</span><span class="sxs-lookup"><span data-stu-id="fbfe5-131">Attribute-data is the data associated with the attribute.</span></span>
  
 <span data-ttu-id="fbfe5-132">_Attach_Seq:_</span><span class="sxs-lookup"><span data-stu-id="fbfe5-132">_Attach_Seq:_</span></span>
  
>  <span data-ttu-id="fbfe5-133">_attRenddata attRenddata Att_Attribute_Seq_</span><span class="sxs-lookup"><span data-stu-id="fbfe5-133">_attRenddata attRenddata Att_Attribute_Seq_</span></span>
    
 <span data-ttu-id="fbfe5-134">_attRenddata:_</span><span class="sxs-lookup"><span data-stu-id="fbfe5-134">_attRenddata:_</span></span>
  
> <span data-ttu-id="fbfe5-135">**LVL_ATTACHMENT verificação de renddata attRenddata** **sizeof (RENDDATA)**</span><span class="sxs-lookup"><span data-stu-id="fbfe5-135">**LVL_ATTACHMENT attRenddata** **sizeof(RENDDATA)** renddata checksum</span></span> 
    
<span data-ttu-id="fbfe5-136">Os renddata são os dados associados à estrutura **RENDDATA** que contém as informações de renderização do anexo correspondente.</span><span class="sxs-lookup"><span data-stu-id="fbfe5-136">Renddata is the data associated with the **RENDDATA** structure that contains the rendering information for the corresponding attachment.</span></span> <span data-ttu-id="fbfe5-137">A **estrutura RENDDATA** é definida no TNEF. Arquivo de header H.</span><span class="sxs-lookup"><span data-stu-id="fbfe5-137">The **RENDDATA** structure is defined in the TNEF.H header file.</span></span> 
  
 <span data-ttu-id="fbfe5-138">_Att_Attribute_Seq:_</span><span class="sxs-lookup"><span data-stu-id="fbfe5-138">_Att_Attribute_Seq:_</span></span>
  
>  <span data-ttu-id="fbfe5-139">_Att_Attribute Att_Attribute Att_Attribute_Seq_</span><span class="sxs-lookup"><span data-stu-id="fbfe5-139">_Att_Attribute Att_Attribute Att_Attribute_Seq_</span></span>
    
 <span data-ttu-id="fbfe5-140">_Att_Attribute:_</span><span class="sxs-lookup"><span data-stu-id="fbfe5-140">_Att_Attribute:_</span></span>
  
> <span data-ttu-id="fbfe5-141">**LVL_ATTACHMENT** verificação atributo-ID atributo-length attribute-data</span><span class="sxs-lookup"><span data-stu-id="fbfe5-141">**LVL_ATTACHMENT** attribute-ID attribute-length attribute-data checksum</span></span> 
    
<span data-ttu-id="fbfe5-142">Attribute-ID, attribute-length, and attribute-data have the same meanings as for the Msg_Attribute item.</span><span class="sxs-lookup"><span data-stu-id="fbfe5-142">Attribute-ID, attribute-length, and attribute-data have the same meanings as for the Msg_Attribute item.</span></span>
  

