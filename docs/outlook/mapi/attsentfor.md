---
title: attSentFor
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: aa8c8d64-d2a0-4cdf-a8aa-21c8d0a0a3fc
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: b292e65ddabcbe052832687a3dcf01658de5e379
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22567472"
---
# <a name="attsentfor"></a><span data-ttu-id="dbc08-103">attSentFor</span><span class="sxs-lookup"><span data-stu-id="dbc08-103">attSentFor</span></span>

  
  
<span data-ttu-id="dbc08-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="dbc08-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="dbc08-105">O atributo **attSentFor** é codificado como cadeias de caracteres contadas apresentados ponta a ponta.</span><span class="sxs-lookup"><span data-stu-id="dbc08-105">The **attSentFor** attribute is encoded as counted strings laid end-to-end.</span></span> <span data-ttu-id="dbc08-106">O formato **attSentFor** é da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="dbc08-106">The format for **attSentFor** is as follows:</span></span> 
  
 <span data-ttu-id="dbc08-107">**attSentFor**:</span><span class="sxs-lookup"><span data-stu-id="dbc08-107">**attSentFor**:</span></span> 
  
> <span data-ttu-id="dbc08-108">nome para exibição do comprimento do nome de exibição endereço-comprimento _endereço de email_</span><span class="sxs-lookup"><span data-stu-id="dbc08-108">display-name-length display-name address-length  _email-address_</span></span>
    
 <span data-ttu-id="dbc08-109">_endereço de email_</span><span class="sxs-lookup"><span data-stu-id="dbc08-109">_email-address_</span></span>
  
> <span data-ttu-id="dbc08-110">endereço do tipo **:**</span><span class="sxs-lookup"><span data-stu-id="dbc08-110">type **:** address</span></span> 
    
<span data-ttu-id="dbc08-111">Ao contrário de outro comprimento valores, o comprimento do nome de exibição e endereço comprimento são valores de 16 bits não assinados, em vez de inteiros longos não assinados.</span><span class="sxs-lookup"><span data-stu-id="dbc08-111">Unlike other length values, the display-name-length and address-length are unsigned 16-bit values instead of unsigned long integers.</span></span> <span data-ttu-id="dbc08-112">Eles ainda incluem abortar caracteres null, no entanto.</span><span class="sxs-lookup"><span data-stu-id="dbc08-112">They still include terminating null characters, however.</span></span> <span data-ttu-id="dbc08-113">As cadeias de caracteres de tipo e endereço na entrada de _endereço de email_ são separadas por um caractere de dois-pontos (:) literal, como "smtp:joe@nowhere.com".</span><span class="sxs-lookup"><span data-stu-id="dbc08-113">The type and address strings in the  _email-address_ entry are separated by a literal colon (:) character, such as "smtp:joe@nowhere.com".</span></span> <span data-ttu-id="dbc08-114">Somente a sequência de endereço do tipo combinada **:** é terminada em nulo.</span><span class="sxs-lookup"><span data-stu-id="dbc08-114">Only the combined type **:** address string is null-terminated.</span></span>
  

