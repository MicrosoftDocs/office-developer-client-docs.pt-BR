---
title: Copiar propriedades MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a52f4bcd-6e17-4623-a469-53be1f2758b1
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: ae8e553cf2e19ae1ba06ca09aad84eae9f7d1238
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415044"
---
# <a name="copying-mapi-properties"></a><span data-ttu-id="b9021-103">Copiar propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="b9021-103">Copying MAPI Properties</span></span>

  
  
<span data-ttu-id="b9021-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b9021-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b9021-105">Os clientes e provedores de serviços podem copiar uma ou mais propriedades de um objeto com os seguintes métodos e funções de API do **IMAPIProp** :</span><span class="sxs-lookup"><span data-stu-id="b9021-105">Clients and service providers can copy one or more of an object's properties with the following **IMAPIProp** methods and API functions:</span></span> 
  
- <span data-ttu-id="b9021-106">O método [IMAPIProp:: CopyTo](imapiprop-copyto.md) copia Todas as propriedades de um objeto para outro objeto, opcionalmente excluindo as propriedades selecionadas.</span><span class="sxs-lookup"><span data-stu-id="b9021-106">The [IMAPIProp::CopyTo](imapiprop-copyto.md) method copies all of an object's properties to another object, optionally excluding selected properties.</span></span> <span data-ttu-id="b9021-107">**CopyTo** é usado para copiar ou mover qualquer tipo de objeto.</span><span class="sxs-lookup"><span data-stu-id="b9021-107">**CopyTo** is used for copying or moving any type of object.</span></span> 
    
- <span data-ttu-id="b9021-108">O método [IMAPIProp:: CopyProps](imapiprop-copyprops.md) copia as propriedades selecionadas de um objeto.</span><span class="sxs-lookup"><span data-stu-id="b9021-108">The [IMAPIProp::CopyProps](imapiprop-copyprops.md) method copies selected properties of an object.</span></span> <span data-ttu-id="b9021-109">**CopyProps** é usado principalmente com mensagens.</span><span class="sxs-lookup"><span data-stu-id="b9021-109">**CopyProps** is used mainly with messages.</span></span> <span data-ttu-id="b9021-110">Quando um cliente cria uma cópia encaminhada de uma mensagem ou uma resposta, **CopyProps** as alças de cópia das propriedades apropriadas da mensagem original.</span><span class="sxs-lookup"><span data-stu-id="b9021-110">When a client creates a forwarded copy of a message or a reply, **CopyProps** handles copying the appropriate properties from the original message.</span></span> 
    
- <span data-ttu-id="b9021-111">A função [PropCopyMore](propcopymore.md) copia um valor de propriedade única de um local para outro.</span><span class="sxs-lookup"><span data-stu-id="b9021-111">The [PropCopyMore](propcopymore.md) function copies a single property value from one location to another.</span></span> <span data-ttu-id="b9021-112">Use **PropCopyMore** com cuidado.</span><span class="sxs-lookup"><span data-stu-id="b9021-112">Use **PropCopyMore** with caution.</span></span> <span data-ttu-id="b9021-113">É possível: ao copiar um valor por vez, para alocar vários blocos pequenos de memória e fazer com que a memória seja fragmentada.</span><span class="sxs-lookup"><span data-stu-id="b9021-113">It is possible — when copying one value at a time — to allocate many small blocks of memory and cause memory to fragment.</span></span> 
    
- <span data-ttu-id="b9021-114">A função [ScCopyProps](sccopyprops.md) copia valores de propriedade em massa.</span><span class="sxs-lookup"><span data-stu-id="b9021-114">The [ScCopyProps](sccopyprops.md) function copies property values in bulk.</span></span> <span data-ttu-id="b9021-115">**ScCopyProps** pode copiar valores de propriedade que foram criados a partir de blocos de memória não conjuntos.</span><span class="sxs-lookup"><span data-stu-id="b9021-115">**ScCopyProps** can copy property values that have been built from disjointed blocks of memory.</span></span> <span data-ttu-id="b9021-116">Ele retorna uma nova matriz de propriedade.</span><span class="sxs-lookup"><span data-stu-id="b9021-116">It returns a new property array.</span></span> 
    
- <span data-ttu-id="b9021-117">Se a matriz de propriedades retornada por **ScCopyProps** for armazenada no disco, use a função [ScRelocProps](screlocprops.md) para ajustar os ponteiros.</span><span class="sxs-lookup"><span data-stu-id="b9021-117">If the property array returned by **ScCopyProps** is to be stored on disk, use the [ScRelocProps](screlocprops.md) function to adjust the pointers.</span></span> <span data-ttu-id="b9021-118">**ScRelocProps** deve ser chamado duas vezes; uma vez para ajustar os endereços antes de gravar a operação de dados e, em seguida, novamente durante a operação de leitura.</span><span class="sxs-lookup"><span data-stu-id="b9021-118">**ScRelocProps** should be called twice; once to adjust the addresses before writing the data operation and then again during the read operation.</span></span> <span data-ttu-id="b9021-119">A função **ScRelocProps** pressupõe que a matriz de valor da propriedade foi originalmente alocada em uma única alocação.</span><span class="sxs-lookup"><span data-stu-id="b9021-119">The **ScRelocProps** function assumes that the property value array was originally allocated in a single allocation.</span></span> 
    
<span data-ttu-id="b9021-120">As funções da API descritas na lista anterior copiam Propriedades na memória, em vez de um objeto para outro objeto.</span><span class="sxs-lookup"><span data-stu-id="b9021-120">The API functions described in the preceding list copy properties in memory rather than from one object to another object.</span></span> <span data-ttu-id="b9021-121">Essas funções têm suporte no momento, mas podem não ser suportadas em uma versão futura.</span><span class="sxs-lookup"><span data-stu-id="b9021-121">These functions are presently supported, but might not be supported in a future release.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="b9021-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="b9021-122">See also</span></span>



[<span data-ttu-id="b9021-123">Visão geral da propriedade MAPI</span><span class="sxs-lookup"><span data-stu-id="b9021-123">MAPI Property Overview</span></span>](mapi-property-overview.md)

