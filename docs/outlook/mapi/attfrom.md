---
title: attFrom
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 2d405268-bb33-4863-be38-2d17e8fc956e
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 6460cd3ef0495a5494e03b4c7034e067cf8793b7
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22576061"
---
# <a name="attfrom"></a><span data-ttu-id="27715-103">attFrom</span><span class="sxs-lookup"><span data-stu-id="27715-103">attFrom</span></span>

<span data-ttu-id="27715-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="27715-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="27715-105">O atributo **attFrom** é codificado como uma estrutura **TRP** que codifica o exibição nome e endereço de email do remetente, seguido do nome para exibição e o endereço do remetente, seguido de qualquer preenchimento necessário.</span><span class="sxs-lookup"><span data-stu-id="27715-105">The **attFrom** attribute is encoded as a **TRP** structure which encodes the display name and email address of the sender, followed by the display name and address of the sender, followed by any necessary padding.</span></span> <span data-ttu-id="27715-106">O formato **attFrom** é da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="27715-106">The format for **attFrom** is as follows:</span></span> 
  
<span data-ttu-id="27715-107">**attFrom**: preenchimento de _ _TRP-estrutura_ _ do nome de exibição do remetente endereço do remetente</span><span class="sxs-lookup"><span data-stu-id="27715-107">**attFrom**: _TRP-structure_ sender-display-name  _ sender-address _ padding</span></span> 
    
<span data-ttu-id="27715-108">O remetente-exibição-name é uma cadeia de caracteres terminada em nulo que é preenchida com um caractere nulo adicional, se necessário, para atingir um limite de 2 bytes.</span><span class="sxs-lookup"><span data-stu-id="27715-108">The sender-display-name is a null-terminated string that is padded with an additional null character, if necessary, to reach a 2-byte boundary.</span></span> <span data-ttu-id="27715-109">O preenchimento no final da codificação **attFrom** consiste em quantos caracteres nulos conforme necessário para alcançar um limite de **sizeof(TRP)** .</span><span class="sxs-lookup"><span data-stu-id="27715-109">The padding at the end of the **attFrom** encoding consists of as many null characters as needed to reach a **sizeof(TRP)** boundary.</span></span> 
  
<span data-ttu-id="27715-110">_Estrutura de TRP:_ **trpidOneOff** cbgrtrp cch cb</span><span class="sxs-lookup"><span data-stu-id="27715-110">_TRP-structure:_ **trpidOneOff** cbgrtrp cch cb</span></span> 
    
<span data-ttu-id="27715-111">Para o item **attFrom** , o **TRP**-estrutura é sempre um únicos encoding, portanto o trpid desativa o **TRP**-campo estrutura é sempre **trpidOneOff**.</span><span class="sxs-lookup"><span data-stu-id="27715-111">For the **attFrom** item, the **TRP**-structure is always a one-off encoding, so the trpid off the **TRP**-structure field is always **trpidOneOff**.</span></span> <span data-ttu-id="27715-112">Os itens de cb, cch e cbgrtrp correspondem aos campos restantes da estrutura **TRP** .</span><span class="sxs-lookup"><span data-stu-id="27715-112">The cbgrtrp, cch, and cb items correspond to the remaining fields of the **TRP** structure.</span></span> 
  
<span data-ttu-id="27715-113">O campo cbgrtrp é calculado como a soma de **(sizeof(TRP) \*2)**, o comprimento do terminada em nulo remetente--nome para exibição com seu preenchimento e o comprimento do endereço de remetente terminada em nulo.</span><span class="sxs-lookup"><span data-stu-id="27715-113">The cbgrtrp field is calculated as the sum of **(sizeof(TRP) \*2)**, the length of the null-terminated sender-display-name with its padding, and the length of the null-terminated sender-address.</span></span>
  
<span data-ttu-id="27715-114">O campo cch é calculado como o comprimento do terminada em nulo-nome para exibição com seu preenchimento.</span><span class="sxs-lookup"><span data-stu-id="27715-114">The cch field is calculated as the length of the null-terminated display-name with its padding.</span></span>
  
<span data-ttu-id="27715-115">O campo cb é calculado como o comprimento do endereço de remetente terminada em nulo.</span><span class="sxs-lookup"><span data-stu-id="27715-115">The cb field is calculated as the length of the null-terminated sender-address.</span></span>
  
<span data-ttu-id="27715-116">_endereço do remetente:_ **:** de tipo de endereço **'\0'** de endereços</span><span class="sxs-lookup"><span data-stu-id="27715-116">_sender-address:_ address-type **:** address **'\0'**</span></span>
    
<span data-ttu-id="27715-117">O endereço do remetente é uma cadeia de caracteres que é composta de quatro partes, o tipo de endereço, dois pontos literal (:), o próprio endereço e um caractere nulo de terminação.</span><span class="sxs-lookup"><span data-stu-id="27715-117">The sender-address is a string that is composed of four parts, the address-type, a literal colon (:), the address itself, and a terminating null character.</span></span> <span data-ttu-id="27715-118">Por exemplo, a cadeia de caracteres `fax:1-909-555-1234\0` seria um valor de endereço de remetente legal.</span><span class="sxs-lookup"><span data-stu-id="27715-118">For example, the string `fax:1-909-555-1234\0` would be a legal sender-address value.</span></span>
  

