---
title: attOwner
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 3c6a4050-fd97-42ce-abb1-118254b367bd
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 0cb40c3c644618bdf65a2c90a91580a5be8fc88c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766211"
---
# <a name="attowner"></a><span data-ttu-id="f60d6-103">attOwner</span><span class="sxs-lookup"><span data-stu-id="f60d6-103">attOwner</span></span>

  
  
<span data-ttu-id="f60d6-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="f60d6-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="f60d6-105">O atributo **attOwner** é codificado como cadeias de caracteres contadas apresentados ponta a ponta.</span><span class="sxs-lookup"><span data-stu-id="f60d6-105">The **attOwner** attribute is encoded as counted strings laid end-to-end.</span></span> <span data-ttu-id="f60d6-106">O formato **attOwner** é da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="f60d6-106">The format for **attOwner** is as follows:</span></span> 
  
 <span data-ttu-id="f60d6-107">**attOwner**:</span><span class="sxs-lookup"><span data-stu-id="f60d6-107">**attOwner**:</span></span> 
  
> <span data-ttu-id="f60d6-108">nome para exibição do comprimento do nome de exibição endereço-comprimento _endereço de email_</span><span class="sxs-lookup"><span data-stu-id="f60d6-108">display-name-length display-name address-length  _email-address_</span></span>
    
 <span data-ttu-id="f60d6-109">_endereço de email_</span><span class="sxs-lookup"><span data-stu-id="f60d6-109">_email-address_</span></span>
  
> <span data-ttu-id="f60d6-110">endereço do tipo **:**</span><span class="sxs-lookup"><span data-stu-id="f60d6-110">type **:** address</span></span> 
    
<span data-ttu-id="f60d6-111">Ao contrário de outro comprimento valores, o comprimento do nome de exibição e endereço comprimento são valores de 16 bits não assinados, em vez de inteiros longos não assinados.</span><span class="sxs-lookup"><span data-stu-id="f60d6-111">Unlike other length values, the display-name-length and address-length are unsigned 16-bit values instead of unsigned long integers.</span></span> <span data-ttu-id="f60d6-112">Eles ainda incluem abortar caracteres null, no entanto.</span><span class="sxs-lookup"><span data-stu-id="f60d6-112">They still include terminating null characters, however.</span></span> <span data-ttu-id="f60d6-113">As cadeias de caracteres de tipo e endereço na entrada de _endereço de email_ são separadas por um caractere de dois-pontos (:) literal, como "smtp:joe@nowhere.com".</span><span class="sxs-lookup"><span data-stu-id="f60d6-113">The type and address strings in the  _email-address_ entry are separated by a literal colon (:) character, such as "smtp:joe@nowhere.com".</span></span> <span data-ttu-id="f60d6-114">Somente a sequência de endereço do tipo combinada **:** é terminada em nulo.</span><span class="sxs-lookup"><span data-stu-id="f60d6-114">Only the combined type **:** address string is null-terminated.</span></span>
  
<span data-ttu-id="f60d6-115">O mapeamento das propriedades MAPI para o atributo **attOwner** é dependente a classe de mensagem da mensagem que está sendo codificada.</span><span class="sxs-lookup"><span data-stu-id="f60d6-115">The mapping of MAPI properties to the **attOwner** attribute is dependent on the message class of the message being encoded.</span></span> 
  

