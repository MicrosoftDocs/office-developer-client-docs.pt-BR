---
title: Obtendo e configurando propriedades com GetProps e SetProps
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 309d2b3d-dc71-4222-b293-4bfc467b5429
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 7d11f69c6da8560f5879ebc38498d852486bed8b
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25395004"
---
# <a name="getting-and-setting-properties-with-getprops-and-setprops"></a><span data-ttu-id="1733e-103">Obtendo e configurando propriedades com GetProps e SetProps</span><span class="sxs-lookup"><span data-stu-id="1733e-103">Getting and setting properties with GetProps and SetProps</span></span>
 
<span data-ttu-id="1733e-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1733e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1733e-105">Sempre que possível, tente recuperar ou modificar uma propriedade com os métodos [IMAPIProp::GetProps](imapiprop-getprops.md) e [IMAPIProp::SetProps](imapiprop-setprops.md) .</span><span class="sxs-lookup"><span data-stu-id="1733e-105">Whenever possible, try to retrieve or modify a property with the [IMAPIProp::GetProps](imapiprop-getprops.md) and [IMAPIProp::SetProps](imapiprop-setprops.md) methods.</span></span> <span data-ttu-id="1733e-106">A menos que a propriedade que você estiver trabalhando com for muito grande, esses métodos devem ser adequados.</span><span class="sxs-lookup"><span data-stu-id="1733e-106">Unless the property you are working with is very large, these methods should be adequate.</span></span> <span data-ttu-id="1733e-107">A outra alternativa é ler ou gravar em um stream com a interface [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="1733e-107">The other alternative is to read from or write to a stream with the [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) interface.</span></span> <span data-ttu-id="1733e-108">Fluxos podem manipular as propriedades muito grandes com êxito, mas são um maior consumo de recursos porque eles exigem as bibliotecas de COM.</span><span class="sxs-lookup"><span data-stu-id="1733e-108">Streams can handle very large properties successfully, but they are a greater drain on resources because they require the COM libraries.</span></span> <span data-ttu-id="1733e-109">Use a interface **IStream** somente depois que a chamada para **IMAPIProp::GetProps** ou **IMAPIProp::SetProps** falha.</span><span class="sxs-lookup"><span data-stu-id="1733e-109">Use the **IStream** interface only after your call to **IMAPIProp::GetProps** or **IMAPIProp::SetProps** fails.</span></span> 
  

