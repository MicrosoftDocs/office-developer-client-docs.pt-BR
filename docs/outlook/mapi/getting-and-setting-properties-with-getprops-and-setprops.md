---
title: Obter e definir propriedades com GetProps e SetProps
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 309d2b3d-dc71-4222-b293-4bfc467b5429
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 7d11f69c6da8560f5879ebc38498d852486bed8b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32299395"
---
# <a name="getting-and-setting-properties-with-getprops-and-setprops"></a><span data-ttu-id="73eb9-103">Obter e definir propriedades com GetProps e SetProps</span><span class="sxs-lookup"><span data-stu-id="73eb9-103">Getting and setting properties with GetProps and SetProps</span></span>
 
<span data-ttu-id="73eb9-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="73eb9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="73eb9-105">Sempre que possível, tente recuperar ou modificar uma propriedade com os métodos [IMAPIProp::GetProps](imapiprop-getprops.md) e [IMAPIProp::SetProps.](imapiprop-setprops.md)</span><span class="sxs-lookup"><span data-stu-id="73eb9-105">Whenever possible, try to retrieve or modify a property with the [IMAPIProp::GetProps](imapiprop-getprops.md) and [IMAPIProp::SetProps](imapiprop-setprops.md) methods.</span></span> <span data-ttu-id="73eb9-106">A menos que a propriedade com a que você está trabalhando seja muito grande, esses métodos devem ser adequados.</span><span class="sxs-lookup"><span data-stu-id="73eb9-106">Unless the property you are working with is very large, these methods should be adequate.</span></span> <span data-ttu-id="73eb9-107">A outra alternativa é ler ou gravar em um fluxo com a interface [IStream.](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="73eb9-107">The other alternative is to read from or write to a stream with the [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) interface.</span></span> <span data-ttu-id="73eb9-108">Os fluxos podem lidar com propriedades muito grandes com êxito, mas são um esvaziamento maior dos recursos porque exigem as bibliotecas COM.</span><span class="sxs-lookup"><span data-stu-id="73eb9-108">Streams can handle very large properties successfully, but they are a greater drain on resources because they require the COM libraries.</span></span> <span data-ttu-id="73eb9-109">Use a interface **IStream** somente depois que sua chamada para **IMAPIProp::GetProps** ou **IMAPIProp::SetProps falhar.**</span><span class="sxs-lookup"><span data-stu-id="73eb9-109">Use the **IStream** interface only after your call to **IMAPIProp::GetProps** or **IMAPIProp::SetProps** fails.</span></span> 
  

