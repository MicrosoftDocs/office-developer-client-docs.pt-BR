---
title: attFrom
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 2d405268-bb33-4863-be38-2d17e8fc956e
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 496bd5439b9f004d3b13d2d73b31b5cac3f9eec9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432412"
---
# <a name="attfrom"></a><span data-ttu-id="68988-103">attFrom</span><span class="sxs-lookup"><span data-stu-id="68988-103">attFrom</span></span>

<span data-ttu-id="68988-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="68988-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="68988-105">O atributo **attFrom** é codificado como uma estrutura **TRP** que codifica o nome para exibição e o endereço de email do remetente, seguido pelo nome de exibição e endereço do remetente, seguido por qualquer preenchimento necessário.</span><span class="sxs-lookup"><span data-stu-id="68988-105">The **attFrom** attribute is encoded as a **TRP** structure which encodes the display name and email address of the sender, followed by the display name and address of the sender, followed by any necessary padding.</span></span> <span data-ttu-id="68988-106">O formato para **attFrom** é o seguinte:</span><span class="sxs-lookup"><span data-stu-id="68988-106">The format for **attFrom** is as follows:</span></span> 
  
<span data-ttu-id="68988-107">**attFrom**: _preenchimento TRP-structure_ sender-display-name _ sender-address _</span><span class="sxs-lookup"><span data-stu-id="68988-107">**attFrom**: _TRP-structure_ sender-display-name  _ sender-address _ padding</span></span> 
    
<span data-ttu-id="68988-108">O sender-display-name é uma cadeia de caracteres terminada em nulo que é preenchimento com um caractere nulo adicional, se necessário, para atingir um limite de 2 byte.</span><span class="sxs-lookup"><span data-stu-id="68988-108">The sender-display-name is a null-terminated string that is padded with an additional null character, if necessary, to reach a 2-byte boundary.</span></span> <span data-ttu-id="68988-109">O preenchimento no final da codificação **attFrom** consiste no número de caracteres nulos necessários para atingir um limite de **tamanho (TRP).**</span><span class="sxs-lookup"><span data-stu-id="68988-109">The padding at the end of the **attFrom** encoding consists of as many null characters as needed to reach a **sizeof(TRP)** boundary.</span></span> 
  
<span data-ttu-id="68988-110">_TRP-structure:_ **trpidOneOff** cbgrtrp cch cb</span><span class="sxs-lookup"><span data-stu-id="68988-110">_TRP-structure:_ **trpidOneOff** cbgrtrp cch cb</span></span> 
    
<span data-ttu-id="68988-111">Para o item **attFrom,** a estrutura **TRP** é sempre uma codificação única, portanto, o trpid fora do campo de estrutura **TRP** é **sempre trpidOneOff**.</span><span class="sxs-lookup"><span data-stu-id="68988-111">For the **attFrom** item, the **TRP**-structure is always a one-off encoding, so the trpid off the **TRP**-structure field is always **trpidOneOff**.</span></span> <span data-ttu-id="68988-112">Os itens cbgrtrp, cch e cb correspondem aos campos restantes da **estrutura TRP.**</span><span class="sxs-lookup"><span data-stu-id="68988-112">The cbgrtrp, cch, and cb items correspond to the remaining fields of the **TRP** structure.</span></span> 
  
<span data-ttu-id="68988-113">O campo cbgrtrp é calculado como a soma de **(sizeof(TRP) \* 2),** o comprimento do sender-display-name terminada por nulo com seu preenchimento e o comprimento do endereço de remetente encerrado nulo.</span><span class="sxs-lookup"><span data-stu-id="68988-113">The cbgrtrp field is calculated as the sum of **(sizeof(TRP) \*2)**, the length of the null-terminated sender-display-name with its padding, and the length of the null-terminated sender-address.</span></span>
  
<span data-ttu-id="68988-114">O campo cch é calculado como o comprimento do nome de exibição terminada em nulo com seu preenchimento.</span><span class="sxs-lookup"><span data-stu-id="68988-114">The cch field is calculated as the length of the null-terminated display-name with its padding.</span></span>
  
<span data-ttu-id="68988-115">O campo cb é calculado como o comprimento do endereço de remetente encerrado nulo.</span><span class="sxs-lookup"><span data-stu-id="68988-115">The cb field is calculated as the length of the null-terminated sender-address.</span></span>
  
<span data-ttu-id="68988-116">_sender-address:_ address-type **:** address **'\0'**</span><span class="sxs-lookup"><span data-stu-id="68988-116">_sender-address:_ address-type **:** address **'\0'**</span></span>
    
<span data-ttu-id="68988-117">O endereço do remetente é uma cadeia de caracteres composta de quatro partes, o tipo de endereço, dois-pontos literais (:), o próprio endereço e um caractere nulo de terminação.</span><span class="sxs-lookup"><span data-stu-id="68988-117">The sender-address is a string that is composed of four parts, the address-type, a literal colon (:), the address itself, and a terminating null character.</span></span> <span data-ttu-id="68988-118">Por exemplo, a cadeia `fax:1-909-555-1234\0` de caracteres seria um valor de endereço de remetente legal.</span><span class="sxs-lookup"><span data-stu-id="68988-118">For example, the string `fax:1-909-555-1234\0` would be a legal sender-address value.</span></span>
  

