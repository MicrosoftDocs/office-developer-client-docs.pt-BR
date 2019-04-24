---
title: attSentFor
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: aa8c8d64-d2a0-4cdf-a8aa-21c8d0a0a3fc
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: f961348e7be474202273aa97a2922566ef40c3a5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32318113"
---
# <a name="attsentfor"></a><span data-ttu-id="ff620-103">attSentFor</span><span class="sxs-lookup"><span data-stu-id="ff620-103">attSentFor</span></span>

  
  
<span data-ttu-id="ff620-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ff620-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ff620-105">O atributo **attSentFor** é codificado como cadeias de caracteres contadas de ponta a ponta.</span><span class="sxs-lookup"><span data-stu-id="ff620-105">The **attSentFor** attribute is encoded as counted strings laid end-to-end.</span></span> <span data-ttu-id="ff620-106">O formato de **attSentFor** é o seguinte:</span><span class="sxs-lookup"><span data-stu-id="ff620-106">The format for **attSentFor** is as follows:</span></span> 
  
 <span data-ttu-id="ff620-107">**attSentFor**:</span><span class="sxs-lookup"><span data-stu-id="ff620-107">**attSentFor**:</span></span> 
  
> <span data-ttu-id="ff620-108">display-name-Name de nome de exibição endereço de _email-endereço_</span><span class="sxs-lookup"><span data-stu-id="ff620-108">display-name-length display-name address-length  _email-address_</span></span>
    
 <span data-ttu-id="ff620-109">_email-endereço_</span><span class="sxs-lookup"><span data-stu-id="ff620-109">_email-address_</span></span>
  
> <span data-ttu-id="ff620-110">tipo **:** endereço</span><span class="sxs-lookup"><span data-stu-id="ff620-110">type **:** address</span></span> 
    
<span data-ttu-id="ff620-111">Diferentemente de outros valores de comprimento, o nome de exibição e comprimento de endereço são valores de 16 bits não assinados em vez de inteiros longos não assinados.</span><span class="sxs-lookup"><span data-stu-id="ff620-111">Unlike other length values, the display-name-length and address-length are unsigned 16-bit values instead of unsigned long integers.</span></span> <span data-ttu-id="ff620-112">No entanto, eles ainda incluem o encerramento de caracteres nulos.</span><span class="sxs-lookup"><span data-stu-id="ff620-112">They still include terminating null characters, however.</span></span> <span data-ttu-id="ff620-113">As cadeias de caracteres de tipo e endereço na entrada de _endereço de email_ são separadas por um caractere de dois-pontos literal (:) caractere, como "SMTP:Joe@nowhere.com".</span><span class="sxs-lookup"><span data-stu-id="ff620-113">The type and address strings in the  _email-address_ entry are separated by a literal colon (:) character, such as "smtp:joe@nowhere.com".</span></span> <span data-ttu-id="ff620-114">Somente o tipo combinado **:** cadeia de caracteres de endereço é terminada em nulo.</span><span class="sxs-lookup"><span data-stu-id="ff620-114">Only the combined type **:** address string is null-terminated.</span></span>
  

